<script lang="ts">
  /**
   * Source of the Image
   */
  export let src;
  /**
   * Function to execute when the element gets registered
   * 
   * Used to add the Element to the LazyLoader when it is registered
   */
  export let registerElement;

  /**
   * Maximum height for an Image if it is not in enlarged mode
   */
  export let imageMHeight;

  let enlarged = false;

  //This function is enlarging the Image (and reseting the fitMode)
  const resizeImage = () => {
    fitMode = 'contained';
    enlarged = !enlarged;
    toggleOverflow();
  }

  const toggleOverflow = () => {
    const bodyElement = document.querySelector('body');
    if (enlarged) {
        bodyElement.style.overflow = 'hidden';
    } else {
        bodyElement.style.overflow = 'auto';
    }
  }

  //This function opens the Image in a new Tab
  const openImage = () => {
    window.open(src, "_blank");
  }

  let fitMode = 'contained';

  let image;

  //This function will load the image when the element is loaded (not when building the DOM)
  const loadElement = () => {
    image.src = src;
  }
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<div class="base-image" class:enlarged on:click={resizeImage}>
    <img alt="Click to enlarge" class={fitMode} style="--ImageMHeight: {imageMHeight}px" bind:this={image} on:loadElement={loadElement} use:registerElement>
</div>


<style>
    .base-image {
        z-index: 6;
        margin-bottom: 50px;
    }

    .base-image img {
        transition: scale ease 1s;
        cursor: pointer;

        object-position: center;
        object-fit: cover;
    }

    .base-image:not(.enlarged) img {
        max-height: var(--ImageMHeight);
    }

    .base-image:not(.enlarged) img:hover {
        scale: 1.1;
    }

    .enlarged {
        z-index: 50;
        
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        background-color: rgba(0, 0, 0, 0.8);
        overflow: hidden;
    }

    .enlarged img {
        flex: 8;
        width: 80%;
        height: 80%;
        position: relative;

        transition: all ease .5s;
        cursor: default;
    }

    .enlarged .contained {
        object-fit: contain;
    }


</style>