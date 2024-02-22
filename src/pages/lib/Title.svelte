<script lang="ts">
  export let text;
  export let charCount;
  export let writedelay;
  export let writechardelay;

  let contentArray = [];

  const texts = text.split('');

  function getRandomAsciiLetter() {
    const randomNumber = Math.random();
    let charCode;

    if (randomNumber < 0.5) {
      charCode = 65 + Math.floor(randomNumber * 26);
    } else {
      charCode = 97 + Math.floor((randomNumber - 0.5) * 26);
    }

    return String.fromCharCode(charCode);
  }

  for (let i = 0; i < texts.length; i++) {
    contentArray.push("&nbsp;");
  }

  const delay = (ms) => new Promise((resolve) => setTimeout(resolve, ms));

  const animate = async (preCharCount, writeDelay, writeCharDelay) => {
    for (let i = 0; i < texts.length; i++) {
      await delay(writeDelay);
      if (texts[i]==' ') {
        contentArray[i] = "&nbsp;";
        continue;
      }
      for (let j = 0; j < preCharCount; j++) {
        await delay(writeCharDelay);
        if (preCharCount - 1 != j) {
          contentArray[i] = getRandomAsciiLetter();
        } else {
          contentArray[i] = texts[i];
        }
      }
    }
  };

  animate(charCount, writedelay, writechardelay);
</script>

<div class="title">
  {#each contentArray as char}
    <span class="title-char">{@html char}</span>
  {/each}
</div>

<style>
  .title-char:hover {
    display: inline-block;
    animation: animateChar ease 1s;
  }

  .title {
    text-align: center;
    color: #f5f5f5;
    text-shadow: 
        0.75px 0.75px 0.75px black,
        0.75px 1.5px 0.75px black,
        0.75px 2.25px 0.75px black,
        0.75px 3px 0.75px black,
        0.75px 3.75px 0.75px black,
        0.75px 4.5px 0.75px black,
        0.75px 5.25px 0.75px black,
        0.75px 6px 0.75px black,
        0.75px 6.75px 0.75px black,
        0.75px 7.5px 0.75px black,
    0.75px 13.5px 2.25px rgba(16,16,16,0.2),
    0.75px 16.5px 3.75px rgba(16,16,16,0.1),
    0.75px 18.75px 12.75px rgba(16,16,16,0.1),
    0.75px 22.5px 22.5px rgba(16,16,16,0.2);
}

  @keyframes animateChar {
    30% {
      transform: scaleY(0.8);
    }
    40% {
      transform: scaleY(1);
    }
    70% {
      transform: scaleY(1.4);
    }
    90% {
      transform: scaleY(1.2);
    }
    100% {
      transform: scaleY(1);
    }

  }
</style>
