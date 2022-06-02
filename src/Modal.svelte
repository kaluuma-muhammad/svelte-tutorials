<script>
    /*
        Some event modifiers
        Once - makes sure that the event can only fire once (removes handler)
        preventDefault - prevent the default action (run e.preventDefault())
        self - only fires the event if the clicked element is the target
    */
    export let showModal = false;
    export let isPromo = false;
</script>

{#if showModal}
    <div class="backdrop" on:click|self>
        <div class="modal" class:promo={isPromo}>
            <slot></slot>
            <!-- <slot name="footer"></slot> -->
        </div>
    </div>
{/if}

<style>
    .backdrop {
        width: 100%;
        height: 100%;
        position: fixed;
        background: rgba(0,0,0,0.8);
    }

    .modal {
        padding: 10px;
        border-radius: 10px;
        max-width: 400px;
        margin: 10% auto;
        text-align: center;
        background: white;
    }

    .promo {
        background: crimson;
        color: white;
    }
</style>