<script lang="ts">
    import { onMount } from 'svelte';
    import { initializeApp } from 'firebase/app';
    import { getFirestore, collection, addDoc, onSnapshot, deleteDoc, doc } from 'firebase/firestore';
    import { getAuth, signInWithEmailAndPassword } from 'firebase/auth';
    // import { toast } from "svelte-toastify";

    let isLoginModalOpen:Boolean;
    let isSigninModalOpen:Boolean;



    let email = '';
  let password = '';
  let FirstName= '';
  let lastName='';
  const firebaseConfig = {
  apiKey: 'AIzaSyA1i8kj58O97gtv4JmqvD7hm39iv0Snmv0',
  authDomain: 'ea-sport-clone.firebaseapp.com',
  projectId: 'ea-sport-clone',
  storageBucket: 'ea-sport-clone.appspot.com',
  messagingSenderId: 'YOUR_MESSAGING_SENDER_ID',
  appId: '12553903133'
};

  
    const app = initializeApp(firebaseConfig);
    const db = getFirestore(app);
    const auth = getAuth(app);
  
    let users: any[] = [];
  
    onMount(() => {
      const unsubscribe = onSnapshot(collection(db, 'users'), (snapshot) => {
        users = snapshot.docs.map((doc) => doc.data());
      });
  
      return unsubscribe;
    });
  
    async function addUser(newUser: { email: string; password: string ;FirstName :string; lastName:string }) {
    try {
      await addDoc(collection(db, 'users'), newUser);
      alert("sign up succesfully")
    } catch (error) {
      alert("error");
    }
  }
  
    // async function deleteUser(userId: string) {
    //   try {
    //     await deleteDoc(doc(db, 'users', userId));
    //   } catch (error) {
    //     console.error('Error deleting user:', error);
    //   }
    // }
    async function loginUser() {
    try {
      await signInWithEmailAndPassword(auth, email, password);
      alert('Login successful!');
    } catch (error) {
      alert('Login error: ');
    }
  }

  function loginOpenModal() {
    isLoginModalOpen = true;
  }
  function SigninOpenModal() {
    isSigninModalOpen = true;
  }

  function loginCloseModal() {
    isLoginModalOpen = false;
  }

  function signinCloseModal() {
    isSigninModalOpen = false;
  }
  </script>
  
  <button class="text-white mx-4" on:click="{SigninOpenModal}">Sign up</button>
  
  

  
  {#if isSigninModalOpen}
  <div class="modal">
    <div class="container w-[70%]">

      <div class="modal-content">
        <h2>Sign up</h2>
        <!-- Add user form -->
        <form class= on:submit|preventDefault>
          <input type="FirstName" placeholder="FirstName" bind:value="{FirstName}" required />
          <input type="lastName" placeholder="LastName" bind:value="{lastName}" required />
          <input type="email" placeholder="Email" bind:value="{email}" required />
          <input type="password" placeholder="Password" bind:value="{password}" required />
          <button class="p-4 bg-slate-400 mx-4" type="submit" on:click="{() => addUser({ email, password,FirstName,lastName })}">Sign Up</button>
          <button class="p-4 bg-red-400 mx-4" on:click="{signinCloseModal}">Close</button>
        </form>
      </div>
    </div>
  </div>
{/if}

<button class="text-white" on:click="{loginOpenModal}">Login</button>

{#if isLoginModalOpen}
  <div class="modal">
    <div class="containerw-[50%] ">
      <div class="modal-content">

        <h2 >Login</h2>
        <form on:submit|preventDefault>
          <input type="email" placeholder="Email" bind:value="{email}" required />
          <input type="password" placeholder="Password" bind:value="{password}" required />
          <button class="p-4 bg-slate-400 mx-4" type="submit" on:click="{loginUser}">Login</button>
          <button class="p-4 bg-red-400 mx-4" on:click="{loginCloseModal}">Close</button>
        </form>
      </div>
      </div>
  </div>
{/if}

<style>
  .modal {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .modal-content {
    background-color: #fff;
    padding: 20px;
    border-radius: 4px;
  }
</style>





