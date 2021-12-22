<script>
  let toggleMore = false;
  let rotateArrow = false;
  // Toggle button content: 'More' / 'Less'; Up / Down arrow
  const toggleButtonText = () => {
    toggleMore = !toggleMore;
    rotateArrow = !rotateArrow;
  };
</script>

<button on:click={toggleButtonText} on:click>
  {toggleMore ? "Less" : "More"}
  <svg
    class:rotateArrow
    height="32"
    viewBox="0 0 32 32"
    width="32"
    xmlns="http://www.w3.org/2000/svg"
  >
    <g fill="none" fill-rule="evenodd">
      <circle cx="16" cy="16" fill="#303030" r="16" />
      <path d="m11.2 13.6 4.8 4.8 4.8-4.8" stroke="#fff" stroke-width="2" />
    </g>
  </svg>
</button>

<style>
  button {
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-size: 0.75rem;
    font-weight: 700;
    letter-spacing: 5px;
    width: 115px;
    height: 39px;
    text-transform: uppercase;
    color: hsla(var(--gray) / 0.5);
    background-color: hsl(var(--white));
    border: none;
    border-radius: 28px;
    padding-left: 0.75rem;
    cursor: pointer;
    transform: rotate(0deg);
  }
  svg circle {
    fill: hsl(var(--gray));
  }
  button:hover svg circle {
    fill: #999999;
    transition: fill 0.3s;
  }
  .rotateArrow {
    transform: rotate(180deg);
    transition: 0.3s;
  }
</style>
