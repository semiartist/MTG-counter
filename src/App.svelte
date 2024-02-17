<script>
  import ScoreBoard from "./components/ScoreBoard.svelte";

  let teams = [{name: "Red", score: 20, color:"red"}, {name: "Blue", score: 20, color:"blue"}]
  
  const resetGame = () =>{
    teams = [{name: "Red", score: 20, color:"red"}, {name: "Blue", score: 20, color:"blue"}]
  }



</script>
<div class="container">

  <h1>MTG Counter App</h1>
  <div class="score-board">
    <ScoreBoard team={teams[0]} />
    <ScoreBoard team={teams[1]} />

  </div>
  
  <button on:click={resetGame}>Reset Game</button>
  
</div>


<style>
  .container {
    width: 1000px
  }
  button{
    width: 100%
  }

  .score-board{
    width: 100%;
    display: flex;
    flex-direction: row;
    align-items:stretch ;
    padding-bottom: 20px;
  }
  button {
    background-color: yellow;
  }
</style>