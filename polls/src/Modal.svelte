<script>
  export let message = 'DEFAULT';
  export let showModal = false;
  export let isPromo = false;
</script>

{#if showModal}
  <!-- Forwarding "on click" event -->
  <div class="backdrop" class:promo={isPromo} on:click>
    <div class="modal">
      <p>{message}</p>
    </div>
  </div>
{/if}

<style lang="scss">
	@import "./styles/styles.scss";

  .backdrop {
    width: 100%;
    height: 100%;
    position: fixed;
    background: rgba(0,0,0,0.8);
  }

  .modal {
    padding: 10px;
    border: {
      radius: 10px;
    }
    max: {
      width: 400px;
    }
    margin: 10% auto;
    text: {
      align: center;
    }
    background: $white;
  }

  .promo {
    color: $blue;
    font: {
      weight: bold;
    }
  }
</style>