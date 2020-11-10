<!DOCTYPE html>
<html>
<head>
<body>
<script>
     alert("Do you wanna build a snow... I mean -- do you wanna play a game?");
    function computerGo() {
        let max = 3;
        let choice = Math.floor(Math.random() * Math.floor(max));

        if(choice==0) {
            return "rock";
        }else if(choice==1){
            return "paper";
        }else if(choice==2){
            return "scissors";
        }
    }

    let playerScore = 0;
    let computerScore = 0;
    let tieScore = 0;

    function playRound() {
        const playerSelection = prompt("choose your weapon: rock, paper, or scisscors!").toLowerCase();
        const computerSelection = computerGo();

        console.log("Human: " + playerSelection);
        console.log("Computer: " + computerSelection);

        if(playerSelection === 'rock'){
            if(computerSelection === 'rock'){
                tieScore++;
                alert("Rock ties rock." + '\n' + "Human: " + playerScore + '  \|  ' + "Computer: " + computerScore);
            }else if(computerSelection === 'paper'){
                computerScore++;
                alert("Rock is beaten by paper." + '\n' + "Human: " + playerScore + '  \|  ' + "Computer: " + computerScore);
            }else if(computerSelection === 'scissors'){
                playerScore++;
                alert("Rock beats scissors." + '\n' + "Human: " + playerScore + ' \| ' + "Computer: " + computerScore);
            }    
        } else if(playerSelection === 'paper'){
                    if(computerSelection === 'rock') {
                        playerScore++;
                        alert("Paper beats rock." + '\n' + "Human: " + playerScore + '  \|  ' + "Computer: " + computerScore);
                    } else if(computerSelection === 'scissors'){
                        computerScore++;
                        alert("Paper is beaten by scissors." + '\n' + "Human: " + playerScore + '  \|  ' + "Computer: " + computerScore);
                    } else if(computerSelection === 'paper'){
                        tieScore++;
                        alert("Paper ties paper." + '\n' + "Human: " + playerScore + '  \|  ' + "Computer: " + computerScore);
                    }
        } else if(playerSelection === 'scissors'){
                    if(computerSelection === 'rock') {
                        computerScore++;
                        alert("Scissors is beaten by rock." + '\n' + "Human: " + playerScore + '  \|  ' + "Computer: " + computerScore);
                    } else if(computerSelection === 'scissors'){
                        tieScore++;
                        alert("Scissors ties scissors."  + '\n' + "Human: " + playerScore + '  \|  ' + "Computer: " + computerScore);
                    } else if(computerSelection === 'paper'){
                        playerScore++;
                        alert("Scissors beats paper." + '\n' + "Human: " + playerScore + '  \|  ' + "Computer: " + computerScore);
            }
            }
        }
    function game(){
        playRound();
        console.log("H: " + playerScore + " to " + "C: " + computerScore);
        playRound();
        console.log("H: " + playerScore + " to " + "C: " + computerScore);
        playRound();
        console.log("H: " + playerScore + " to " + "C: " + computerScore);
        playRound();
        console.log("H: " + playerScore + " to " + "C: " + computerScore);
        playRound();
        console.log("H: " + playerScore + " to " + "C: " + computerScore);
        console.log("Final Score\= H: " + playerScore + " to " + "C: " + computerScore);
        if(playerScore>computerScore){
            alert("Game over. Human wins!" + ' ' + playerScore + ' to ' + computerScore)
        }else if(playerScore==computerScore){
            alert("Game over. Tie!" + ' ' + playerScore + ' to ' +computerScore)
        }else{
            alert("Game over. Computer wins!" + ' ' + playerScore + ' to ' + computerScore)
        }
        }
    game();
</script>
</body>
</head>
</html>
