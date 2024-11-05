# Rock-paper-scissors
<!DOCTYPE html>
<html lang="en">
<head>
    <title>ROCK PAPER SCISSORS</title>
    <style>
        .PR {
            background-color:blue;
            color: red;
            font-size: 10px;
            padding: 10px;
            cursor: pointer;

        }
        .RP {
            background-color: blue;
            color: red;
            font-size: 10px;
            padding: 10px;
            cursor: pointer;
            
        }
        .pr {
            background-color: blue;
            color:red;
            font-size: 10px;
            padding: 10px;
            cursor: pointer;
            
        }
    </style>
</head>
<body>
    <p>Rock Paper Scissors</p>
    <button class ='PR' onclick="
    playgame('Rock');
">Rock</button>
<button class='RP' onclick="
playgame('Paper');
">Paper</button>
    <button class='pr' onclick="
     playgame('Scissors');
    ">Scissors</button>
</body>
<script>
    let computerMove ='';
    let result='';
    let win =0,loss =0,tie =0;
  
    function playgame(playermove)
    {
        
        cmptMove()
        if(playermove === 'Scissors')
        {
            if(computerMove === 'Rock')
            {
                result='Loss';
            } 
            else if(computerMove === 'Paper')
            {
                result='Win';
            }
            else if(computerMove === 'Scissors')
            {
                result='Tie'
            }
        }
        else if(playermove === 'Paper')
        {
        if(computerMove === 'Rock')
            {
                result='Win';
            } 
            else if(computerMove === 'Paper')
            {
                result='Tie';
            }
            else if(computerMove === 'Scissors')
            {
                result='Loss'
            }
        }
        else if(playermove === 'Rock')
        {
            if(computerMove === 'Rock')
            {
                result='Tie';
            } 
            else if(computerMove === 'Paper')
            {
                result='Loss';
            }
            else if(computerMove === 'Scissors')
            {
                result='Win'
            }
        } 
        if (result === 'Win')
        {
            win = win+1;
        }
        else if( result === 'Loss')
        {
            loss = loss+1;
        }
        else if(result === 'Tie')
        {
            tie = tie+1;
        }
    alert(`You picked ${playermove}. computer Picked ${computerMove},
    win:${win}  loss:${loss} tie:${tie}`);
    }
    function cmptMove()
    {
        const randomNumber = Math.random();
        if(randomNumber>=0 && randomNumber<1/3)
        {
            computerMove='Rock';
        }
        else if(randomNumber >= 1/3 && randomNumber <2/3)
        {
            computerMove ='Paper';
        }
        else if(randomNumber >= 2/3 && randomNumber <1)
        {
            computerMove ='Scissors';
        }
        return computerMove;
    }
    
</script>
</html>
