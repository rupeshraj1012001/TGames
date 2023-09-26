# TGames powered by T-Services
//add inside body
<p id="bonus"></p>

// add a bonusPoints variable to keep track of the bonus points
var bonusPoints = 0;


// add Inside the game loop


if (cell.x === apple.x && cell.y === apple.y) {
  snake.maxCells++;
  score += 1;

  if (score % 5 === 0) {
    // Award a bonus point every 5 steps
    bonusPoints++;
  }

  localStorage.setItem('score', score);
  document.getElementById('score').innerHTML = score;

  // Check for bonus points
  if (bonusPoints > 0) {
    document.getElementById('bonus').innerHTML = 'Bonus: ' + bonusPoints;
  }
}

//  With this changes,  game will award a bonus point every time the player completes 5 steps .
