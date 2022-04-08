<script>
  export let color = 'pink'
  export let text = 'learn more'
  export let href = '/'
</script>

<a href="{href}" class="{color}">{text}</a>

<style>
  a {
    font-family: "Fraunces", serif;
    font-weight: 900;
    font-size: 0.9375rem;
    line-height: 1.667;
    letter-spacing: 0.0625rem;
    text-transform: uppercase;
    color: var(--color-dark-blue);
    position: relative;
    z-index: 1;
  }

  a::after{
    content: "";
    width: 8.5625rem;
    height: 0.625rem;
    border-radius: 2rem;
    background-color: var(--card-color);
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    bottom: 0.0313rem;
    z-index: -1;
    opacity: .25;
    transition: opacity .4s ease;
  }

  a:hover::after {
    opacity: 1;
  }

  .yellow {
    --card-color: hsl(51, 100%, 49%);
  }

  .pink {
    --card-color: hsl(7, 99%, 70%);
  }

</style>