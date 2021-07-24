<script>
  let showModal = true;
  let isPromo = true;
</script>

{#if showModal}
  <div class="backdrop" class:promo={isPromo}>
    <div class="modal">
      <p>Modal component</p>
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