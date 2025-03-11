<script>
  import Trustbar from "./lib/trustbar.svelte";
  import { onMount } from "svelte";
</script>

<main
  class="main-container"
>
  <header class="offical-header-container">
      <Trustbar />
  </header>
  <header class="main-header-container">
      <div class="main-header-state-logo-container">
        <img src="src/assets/nys-logo.png" alt="New York State Logo" class="main-header-logo" />
        <p class="main-header-title">Office of Finance</p>
      </div>
  </header>
  <div class="main-content-container">
    <h1
      class="main-content-title"
    ><b>Dispute a Ticket</b></h1>
    <div class="main-content-dispute-options-container">
      <a href="https://i.imgflip.com/51ygax.jpg"><div class="main-content-dispute-option">
        Online
      </div></a>
      <a href="https://i.imgflip.com/51ygax.jpg"><div class="main-content-dispute-option">
        In-Person
      </div></a>
      <a href="https://i.imgflip.com/51ygax.jpg"><div class="main-content-dispute-option">
        By Mail
      </div></a>
      <a href="https://i.imgflip.com/51ygax.jpg"><div class="main-content-dispute-option">
        Not Guilty
      </div></a>
    </div>
    <h1
      class="main-content-title"
    ><b>Important Information</b></h1>
    <p
      class="main-content-text"
    >You must dispute a ticket within 30 days of the date the ticket was issued. If you do not dispute the ticket within 30 days, you may be found guilty by default and <b>additional penalties may apply.</b></p>
  </div>
</main>