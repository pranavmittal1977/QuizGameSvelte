<!-- <script lang= "ts">
    let buttons = new Array(9).fill(null);
    let result = null;
    let turn = 'X';
    const winCombinations = [
        [0, 1, 2],
        [3, 4, 5],
        [6, 7, 8],
        [0, 3, 6],
        [1, 4, 7],
        [2, 5, 8],
        [0, 4, 8],
        [2, 4, 6]

    ];

    function setValue(i){
        buttons[i] = turn;
        buttons = [...buttons];
        turn = turn == 'X' ? 'O' : 'X';
        if(!buttons.includes(null)){
            result = 'Draw';
        }else{
            checkWinner();
        }
    }

    function checkWinner(){
        for (let i = 0; i < winCombinations.length; i++){
            if (buttons[winCombinations])
        }

    }
</script>

<style>
    .tictac {
        width: 300px;
        height: 300px;
        display: flex;
        flex-wrap: wrap;

    }

    .tictac button {
        width: 100px;
        height: 100px;
        margin: 0px;
    }

</style>

{#if !result}
    <div class="tictac">
        {#each buttons as button, i }
            <button on:click={() => setValue(i)}>
                {button?button:""}
            </button>
        {/each}

    </div>
{/if} -->