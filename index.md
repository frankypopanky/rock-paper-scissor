<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <script>

const compPsr = ['rock', 'scissor','paper'];
let pointsComputer = 0;
let pointsMy = 0;
let i = 0;

function computerPlay(){
    computerSelection = compPsr[Math.floor(Math.random()*compPsr.length)];
    return computerSelection;
}
function myPlay(){
    playerSelection = window.prompt('ssp').toLowerCase();
    return playerSelection;
}

function playRound(playerSelection, computerSelection){
    computerSelection= computerPlay();
    playerSelection= myPlay();
    console.log(playerSelection, computerSelection);
    if (playerSelection === computerSelection){
        console.log('Point for both');
        pointsComputer ++;
        pointsMy ++;    
    }
    else if (computerSelection != playerSelection){
        
        if ((computerSelection === 'rock')&& (playerSelection ==='scissor')){
            console.log('Point for Computer');
            pointsComputer ++;    
        }
        else if ((computerSelection === 'paper')&& (playerSelection ==='rock')){
            console.log('Point for Computer');
            pointsComputer ++;
        }
        else if ((computerSelection === 'scissor')&& (playerSelection ==='paper')) {
            console.log('Point for Computer');
            pointsComputer ++;
        }
        else{
            console.log('Point for me');
            pointsMy ++;
        }
    }
}

function game() {
    for (i; i < 5; i++) {
        playRound();
        console.log('Me: ' + pointsMy);
        console.log('Computer: ' + pointsComputer);
    }
}
game();
    </script>
</body>
</html>
