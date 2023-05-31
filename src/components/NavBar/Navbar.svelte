<script >
  let isDropdownOpen = false;

  function openDropdown() {
    isDropdownOpen = true;
  }

  function closeDropdown() {
    isDropdownOpen = false;
  }
</script>
  



<div class="container flex justify-start  items-center  max-w-full h-20">
    <div class="container flex items-center ml-4">
        <div class=" flex justify-center items-center flex-row-reverse  ">
            <img  src="/images/NavBar/dots.png" alt="" style="height: 25px; width: 24px;">
         </div>
         
        <div class="ml-8 mr-5  h-full">
            <img src="/images/NavBar/ea-logo.svg" alt="/">
        </div>  

  


    <div class=" container flex justify-start  justify-items-start">
      
     
      <div class="dropdown ml-5" on:mouseenter={openDropdown} on:mouseleave={closeDropdown}>
        <button class="dropdown-btn">Games</button>
        {#if isDropdownOpen}
          <div class="dropdown-content flex-row">
            <a href="/">BROWSE GAMES</a>
            <a href="/">Latest Games</a>
            <a href="/">Coming Soon</a>
            <a href="/">EA app Deals</a>
            <a href="/">Games Library</a>
            <a href="/">EA Originals</a>
            <a href="/">Free-To-Play</a>
          </div>
          
        {/if}
      </div>
       
      <div class="dropdown slide-in-top ml-5" on:mouseenter={openDropdown} on:mouseleave={closeDropdown}>
        <button class="dropdown-btn">More Experiences</button>
        {#if isDropdownOpen}
          <div class="dropdown-content">
            <a href="/">EA Play</a>
            <a href="/">The EA app</a>
            <a href="/">Competitive Gaming</a>
            <a href="/">EA Play Live</a>
            <a href="/">Playtesting</a>
          </div>
        {/if}
      </div>
      <div class="dropdown ml-5" on:mouseenter={openDropdown} on:mouseleave={closeDropdown}>
        <button class="dropdown-btn">About</button>
        {#if isDropdownOpen}
          <div class="dropdown-content">
            <a href="/">Company</a>
            <a href="/">EA Studios</a>
            <a href="/">Careers</a>
            <a href="/">Our Technology</a>
            <a href="/">EA Partners</a>
            <a href="/">News</a>
            <a href="/">Inside EA</a>
          </div>
        {/if}
      </div>
      <div class="dropdown ml-5" on:mouseenter={openDropdown} on:mouseleave={closeDropdown}>
        <button class="dropdown-btn">Commitments</button>
        {#if isDropdownOpen}
          <div class="dropdown-content">
            <a href="/">Positive Play</a>
            <a href="/">Inclusion & Diversity</a>
            <a href="/">Social Impact</a>
            <a href="/">People & Culture</a>
            <a href="/">Environment</a>
            <a href="/">Our Commitments</a>
          </div>
        {/if}
      </div>
      <div class="dropdown ml-5" on:mouseenter={openDropdown} on:mouseleave={closeDropdown}>
        <button class="dropdown-btn">Resources</button>
        {#if isDropdownOpen}
          <div class="dropdown-content">
            <a href="/">Help</a>
            <a href="/">Forums</a>
            <a href="/">Player and Parental Tools</a>
            <a href="/">Accessibility</a>
            <a href="/">Press</a>
            <a href="/">Investors</a>
          </div>
        {/if}
      </div>
</div>
</div>
          
</div>


<style>
   .dropdown {
    position: relative;
    display: inline-block;
  }

  .dropdown-btn {
  
    color: rgb(0, 0, 0);
    padding: 12px;
    font-size: 16px;
    border: none;
    cursor: pointer;
  }

  .dropdown-content {
    display: none;
    position: absolute;
    background-color: #f9f9f9;
    min-width: 160px;
    box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
    z-index: 1;
  }

  .dropdown-content a {
    color: black;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
  }

  .dropdown-content a:hover {
    background-color: #f1f1f1;
  }

  .dropdown:hover .dropdown-content {
    display: block;
  }
  .slide-in-top {
	-webkit-animation: slide-in-top 0.6s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
	        animation: slide-in-top 0.6s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
}
</style>