<script>
  import { onMount } from "svelte";
  let showDropdown = false;
  
  function toggleDropdown() {
      showDropdown = !showDropdown;
  }
</script>

<style>
  .header {
      color: white;
      padding: 10px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-family: "Montserrat", sans-serif;
      font-size: 0.8rem;

  }

  .dropdown {
      display: flex;
      flex-direction: row;
      gap: 10px;
      padding: 10px;
      border: 1px solid #ddd;
      background-color: #fff;
      font-family: "Montserrat", sans-serif;
      position: absolute;
      top: 50px;
      left: 19%;
  }

  .dropdown-content {
      padding: 10px;
      background-color: #fff;
      border-radius: 5px;
      max-width: 20rem;
  }

  .clickable {
      cursor: pointer;
      user-select: none;
      text-decoration: underline;
      color: #a2a2ff;
      margin-left: 1.25rem;
  }

  .dropdown-content-image{
      width: 50px;
      height: 50px;
  }
</style>

<div class="header">
  <p>An official website of New York State</p>
  <div class="clickable" on:click={toggleDropdown}>
    Here’s how you know ▾
  </div>
</div>

{#if showDropdown}
  <div class="dropdown">
      <div class="dropdown-content-item">
        <img src="src/assets/assured_workload.svg" class="dropdown-content-image" alt="Assured Workload" />
        <div class="dropdown-content">
          <b>Official websites use .org</b>
          <p>A .org website belongs to a government organization or to a related sponsored organization.</p>
      </div>
    </div>
    <div class="dropdown-content-item">
      <img src="src/assets/vpn_lock.svg" class="dropdown-content-image" alt="Assured Workload" />
      <div class="dropdown-content">
        <b>Secure ny.org websites use HTTPS</b>
        <p>A lock icon or https:// means you’ve safely connected to a ny.org website. Share sensitive information only on official, secure websites</p>
    </div>
  </div>
  </div>
{/if}

