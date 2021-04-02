<html>

  <head>
    <title>Rock Paper Scissors</title>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
    </head>

    <body>
      <h1>Welcome to the "Rock, Paper, Scissors" Game!</h1>
      <h2>Here are the rules: Click one of the three buttons below.
        <br> Then the results will print to the screen so you can see if you won, lost, or tied.
        <br> You will see a running tally of your results if you keep playing!</h2>

      <button id = "rock">Rock</button>
      <button id = "paper">Paper</button>
      <button id = "scissors">Scissors</button>

      <h3>Stats will appear below:</h3>

      <script>

        var winCounter = 0;
        var tieCounter = 0;
        var lossCounter = 0;
        var playCount = 0;

        //Rock Button Function
        $("#rock").click(function() {

        var ComputerChoice = Math.floor((Math.random() * 3) + 1);

        if (ComputerChoice == 1 ) {
          var outcome = "Rock";
          $("h3").append("<br>" + "Computer chose Rock!");
        }
        else if (ComputerChoice == 2) {
          var outcome = "Paper";
          $("h3").append("<br>" + "Computer chose Paper!");
        }
        else if (ComputerChoice == 3) {
          var outcome = "Scissors";
          $("h3").append("<br>" + "Computer chose Scissors!");
        }
        if (outcome == "Rock") {
          $("h3").append("<br>" + "You tied!");
          tieCounter ++;
        }
        else if (outcome == "Paper") {
          $("h3").append("<br>" + "That counts as a loss.");
          lossCounter ++;
        }
        else if (outcome == "Scissors") {
          $("h3").append("<br>" + "You won!");
          winCounter ++;
        }
        playCount ++;
        $("h3").append(" Wins: " + winCounter + " Losses: " + lossCounter + " Ties: " + tieCounter + " Win Percentage: %" + winCounter/playCount*100);
      })


      //Paper Button Function
            $("#paper").click(function() {

            var ComputerChoice = Math.floor((Math.random() * 3) + 1);

            if (ComputerChoice == 1 ) {
              var outcome = "Rock";
              $("h3").append("<br>" + "Computer chose Rock!");
            }
            else if (ComputerChoice == 2) {
              var outcome = "Paper";
              $("h3").append("<br>" + "Computer chose Paper!");
            }
            else if (ComputerChoice == 3) {
              var outcome = "Scissors";
              $("h3").append("<br>" + "Computer chose Scissors!");
            }
            if (outcome == "Rock") {
              $("h3").append("<br>" + "You Won!");
              winCounter ++;
            }
            else if (outcome == "Paper") {
              $("h3").append("<br>" + "You tied!");
              tieCounter ++;
            }
            else if (outcome == "Scissors") {
              $("h3").append("<br>" + "That counts as a loss.");
              lossCounter ++;
            }
            playCount ++;
            $("h3").append(" Wins: " + winCounter + " Losses: " + lossCounter + " Ties: " + tieCounter + " Win Percentage: %" + winCounter/playCount*100);
            })



            //Scissors Button Function
            $("#scissors").click(function() {

            var ComputerChoice = Math.floor((Math.random() * 3) + 1);

            if (ComputerChoice == 1 ) {
              var outcome = "Rock";
              $("h3").append("<br>" + "Computer chose Rock!");
            }
            else if (ComputerChoice == 2) {
              var outcome = "Paper";
              $("h3").append("<br>" + "Computer chose Paper!");
            }
            else if (ComputerChoice == 3) {
              var outcome = "Scissors";
              $("h3").append("<br>" + "Computer chose Scissors!");
            }
            if (outcome == "Rock") {
              $("h3").append("<br>" + "That counts as a loss.");
              lossCounter ++;
            }
            else if (outcome == "Paper") {
              $("h3").append("<br>" + "You won!");
              winCounter ++;
            }
            else if (outcome == "Scissors") {
              $("h3").append("<br>" + "You tied!");
              tieCounter ++;
            }
            playCount ++;
            $("h3").append(" Wins: " + winCounter + " Losses: " + lossCounter + " Ties: " + tieCounter + " Win Percentage: %" + winCounter/playCount*100);
            })

      </script>

    </body>

  </html>
