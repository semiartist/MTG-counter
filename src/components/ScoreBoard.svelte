<script>
    export let team ;

    const addPoint = () =>{
        team.score +=1;
    }

    const minusPoint = () =>{
        team.score -= 1;
        checkScore()
    }

    const checkScore = () =>{

      if (team.score === 0) {
        alert(team.name+" team you lose!")
      
    }
  }
</script>


<div class="board" style="border-color:{team.color}">
    <h3>Team {team.name}: {team.score}</h3>
    <div class="button">
        <button class="plus" on:click={addPoint}>+</button>
        <button class="minus" on:click={minusPoint}>-</button>
    </div>
</div>


<style>
    .board {
        flex: 1;
        border: dashed;
        padding-bottom: 20px;
    }
    .plus {
        background-color: green;
    }
    .minus {
        background-color: red;
    }
</style>