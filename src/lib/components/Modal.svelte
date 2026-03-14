<script>
    let {showModal = $bindable(), children} = $props();
    let dialog = $state();

    $effect(() => {
		if (showModal) dialog.showModal();
	});

</script>

<dialog bind:this={dialog}
    onclose= {() => (showModal = false)}
    onclick={(e) => { if (e.target === dialog) dialog.close(); }}
    >

    <div class="modal-shell">
      <button class="close" aria-label="Close dialog" autofocus onclick={() => dialog.close()}>
        ×
      </button>

      <div class="modal-body">
        {@render children?.()}
      </div>
    </div>

</dialog>


<style lang="css">
    dialog {
      max-width: 34rem;
      width: min(90vw, 560px);
      border-radius: 18px;
      border: 1px solid rgba(255, 255, 255, 0.32);
      padding: 0;
      background: radial-gradient(120% 120% at 80% 0%, rgba(36, 194, 255, 0.15), transparent 55%),
        linear-gradient(145deg, rgba(14, 107, 207, 0.08), rgba(14, 44, 83, 0.4));
      box-shadow: 0 30px 70px rgba(15, 31, 51, 0.35);
      color: #0f1f33;
      backdrop-filter: blur(12px);
      overflow: hidden;
    }
    dialog::backdrop {
      background: rgba(6, 14, 26, 0.55);
    }
    .modal-shell {
      position: relative;
      padding: 24px;
      background: rgba(255, 255, 255, 0.82);
      border-radius: 16px;
    }
    .modal-body {
      display: grid;
      gap: 12px;
      color: #0f1f33;
    }
    .close {
      position: absolute;
      top: 12px;
      right: 12px;
      width: 32px;
      height: 32px;
      border-radius: 10px;
      border: 1px solid rgba(15, 31, 51, 0.12);
      background: rgba(255, 255, 255, 0.8);
      color: #0f1f33;
      font-size: 1.1rem;
      font-weight: 800;
      cursor: pointer;
      transition: transform 120ms ease, box-shadow 120ms ease, background 120ms ease;
    }
    .close:hover,
    .close:focus-visible {
      transform: translateY(-1px);
      box-shadow: 0 10px 20px rgba(15, 31, 51, 0.18);
      outline: none;
      background: rgba(255, 255, 255, 0.95);
    }
    dialog[open] {
      animation: zoom 0.28s cubic-bezier(0.34, 1.56, 0.64, 1);
    }
    @keyframes zoom {
      from {
        transform: scale(0.94);
      }
      to {
        transform: scale(1);
      }
    }
    dialog[open]::backdrop {
      animation: fade 0.2s ease-out;
    }
    @keyframes fade {
      from {
        opacity: 0;
      }
      to {
        opacity: 1;
      }
    }
</style>
