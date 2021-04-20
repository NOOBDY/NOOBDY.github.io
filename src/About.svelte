<div class={$$props.class} id="about">
  <div>
    <h1 id="title">about me</h1>
    <p class="subtitle">
      i like to watch movies,<br />
      solve problems,<br />
      and build cool stuff.
    </p>
    <p class="content" />
  </div>
</div>

<style>
  #about {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  #about #title {
    font-size: 150px;
    position: absolute;
    top: 20%;
    left: 25%;
    transform: translate(-50%, -50%);
  }
  .subtitle {
    font-size: 40px;
    position: absolute;
    text-align: right;
    top: 50%;
    left: 32%;
    transform: translate(-50%, -50%);
  }
  .content {
    font-size: 25px;
    text-align: left;
    position: absolute;
    top: 43%;
    left: 65%;
    transform: translate(-50%, -50%);
  }
</style>
