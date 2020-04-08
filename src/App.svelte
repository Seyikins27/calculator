<script>
  export let name;
  let screen = " ";
  const append = value => {
    screen = screen + value;
  };
  const evaluate = value => {
    let res = eval(value.toString());
    screen = res;
  };

  const clear = () => {
    screen = " ";
  };
</script>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<center>
  <div class="container">
    <div class="card">
      <h3>Hello Calculator</h3>
      <div class="grid-3">
        <div>
          <input type="text" bind:value={screen} placeholder="0" />
        </div>
      </div>

      <div class="grid-3">
        <button class="btn btn-slgm btn-dark" on:click={() => append(1)}>
          1
        </button>
        <button class="btn btn-lg btn-dark" on:click={() => append(2)}>
          2
        </button>
        <button class="btn btn-lg btn-dark" on:click={() => append(3)}>
          3
        </button>
      </div>
      <div class="grid-3">
        <button class="btn btn-lg btn-dark" on:click={() => append(4)}>
          4
        </button>
        <button class="btn btn-lg btn-dark" on:click={() => append(5)}>
          5
        </button>
        <button class="btn btn-lg btn-dark" on:click={() => append(6)}>
          6
        </button>
      </div>
      <div class="grid-3">
        <button class="btn btn-lg btn-dark" on:click={() => append(7)}>
          7
        </button>
        <button class="btn btn-lg btn-dark" on:click={() => append(8)}>
          8
        </button>
        <button class="btn btn-lg btn-dark" on:click={() => append(9)}>
          9
        </button>
      </div>
      <div class="grid-3">
        <button class="btn btn-lg btn-dark" on:click={() => append('-')}>
          -
        </button>
        <button class="btn btn-lg btn-dark" on:click={() => append(0)}>
          0
        </button>
        <button class="btn btn-lg btn-dark" on:click={() => append('+')}>
          +
        </button>
      </div>
      <div class="grid-3">
        <button class="btn btn-lg btn-dark" on:click={() => append('*')}>
          *
        </button>
        <button class="btn btn-lg btn-dark" on:click={() => append('/')}>
          /
        </button>
        <button class="btn btn-lg btn-dark" on:click={() => evaluate(screen)}>
          =
        </button>
      </div>
      <div class="grid-3">
        <button class="btn btn-lg btn-dark" on:click={() => clear()}>CE</button>
      </div>

    </div>
  </div>
</center>
