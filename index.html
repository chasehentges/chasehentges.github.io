<!DOCTYPE html>
<html lang="en-US" prefix="og: http://ogp.me/ns#">
<head>
    <!-- Global site tag (gtag.js) - Google Analytics -->
    <script async src="https://www.googletagmanager.com/gtag/js?id=UA-146768211-1"></script>
    <script>
      window.dataLayer = window.dataLayer || [];
      function gtag(){dataLayer.push(arguments);}
      gtag('js', new Date());

      gtag('config', 'UA-146768211-1');
    </script>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chase Hentges - photo + film + point of view - nashville, tn</title>
    <meta name="description" content=""/>
    <link rel="profile" href="http://gmpg.org/xfn/11" />
    <link rel="shortcut icon" href="img/favicon.ico" />
    <link rel="stylesheet" href="style.css?v1">
</head>

<body>
    <div class="wrap">
        <header>
            <a href="" class="logo"><img src="img/chase-hentges-logo.png" class="main-logo" alt="Chase Hentges Logo"><img src="img/ch-sticker.png" class="hover-logo" alt="Chase Hentges Swiss Logo."></a>

            <h1>photo + film + point of view</h1>

            <table class="contact">
                <tr>
                    <td>call</td>
                    <td>
                        <a href="tel:612-868-7799">612.868.7799</a>
                    </td>
                </tr>
                <tr>
                    <td>write</td>
                    <td>
                        <a href="mailto:chase@chasehentges.co">chase@chasehentges.co</a>
                    </td>
                </tr>
                <tr>
                    <td>visit</td>
                    <td>
                        <a href="https://maps.google.com/?saddr=My%20Location&daddr=Nashville+TN" target="_blank">nashville, tn</a>
                    </td>
                </tr>
            </table>
        </header>

        <div class="content">
            <div style="padding:56.25% 0 0 0;position:relative;" class="video space-below"><iframe src="https://player.vimeo.com/video/363168395?title=0&byline=0&portrait=0&autoplay=1&fun=0&loop=1&muted=1&color=000000&controls=0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>
            <img src="img/baby-chase.jpg" alt="Chase Hentges as a child." class="space-below">
            <div class="bts">
                <img src="img/bts1.gif" alt="Behind the scenes - 1">
                <img src="img/bts2.gif" alt="Behind the scenes - 2">
                <img src="img/bts3.gif" alt="Behind the scenes - 3">
            </div>
        </div>
    </div>

    <div class="game-outer">
        <div class="game-inner">
            <!--------------------------------------
            --------------------------------------
             This looks fun! Click on the logo ;)
             ------------------------------------
             --------------------------------------->
            <div class="game-text">
                hit the <span>space bar</span> to launch the ball.
                <br>
                when you're done playing hit <span>esc</span>
            </div>
            <canvas width="320" height="400" id="game"></canvas>
            <script>

            </script>
        </div>
    </div>

<script type='text/javascript' src='https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js'></script>
<script type='text/javascript'>

    $( '.logo' ).click(function(e) {
        e.preventDefault();
        if ($(window).width() > 500) {
            $('body').addClass('modal-open');
        }
    });

    const canvas = document.getElementById('game');
    const context = canvas.getContext('2d');
    // each row is 14 bricks long. the level consists of 6 blank rows then 8 rows
    // of 4 colors: red, orange, green, and yellow
    const level1 = [
      [],
      [],
      [],
      [],
      ['R','R','R','R','R','R','R','R','R','R','R','R','R','R'],
      ['R','R','R','R','R','R','R','R','R','R','R','R','R','R'],
      ['O','O','O','O','O','O','O','O','O','O','O','O','O','O'],
      ['O','O','O','O','O','O','O','O','O','O','O','O','O','O'],
      ['G','G','G','G','G','G','G','G','G','G','G','G','G','G'],
      ['G','G','G','G','G','G','G','G','G','G','G','G','G','G'],
      ['Y','Y','Y','Y','Y','Y','Y','Y','Y','Y','Y','Y','Y','Y'],
      ['Y','Y','Y','Y','Y','Y','Y','Y','Y','Y','Y','Y','Y','Y']
    ];
    // create a mapping between color short code (R, O, G, Y) and color name
    const colorMap = {
      'R': '#000',
      'O': '#404040',
      'G': '#7F7F7F',
      'Y': '#BFBFBF'
    };
    // use a 2px gap between each brick
    const brickGap = 2;
    const brickWidth = 20.7;
    const brickHeight = 6;
    // the wall width takes up the remaining space of the canvas width. with 14 bricks
    // and 13 2px gaps between them, thats: 400 - (14 * 25 + 2 * 13) = 24px. so each
    // wall will be 12px
    const wallSize = 2;
    const bricks = [];
    // create the level by looping over each row and column in the level1 array
    // and creating an object with the bricks position (x, y) and color
    for (let row = 0; row < level1.length; row++) {
      for (let col = 0; col < level1[row].length; col++) {
        const colorCode = level1[row][col];
        bricks.push({
          x: wallSize + (brickWidth + brickGap) * col,
          y: wallSize + (brickHeight + brickGap) * row,
          color: colorMap[colorCode],
          width: brickWidth,
          height: brickHeight
        });
      }
    }
    const paddle = {
      // place the paddle horizontally in the middle of the screen
      x: canvas.width / 2 - brickWidth / 2,
      y: 380,
      width: brickWidth,
      height: brickHeight,
      // paddle x velocity
      dx: 0
    };
    const ball = {
      x: 130,
      y: 260,
      width: 5,
      height: 5,
      // how fast the ball should go in either the x or y direction
      speed: 2,
      // ball velocity
      dx: 0,
      dy: 0
    };
    // check for collision between two objects using axis-aligned bounding box (AABB)
    // @see https://developer.mozilla.org/en-US/docs/Games/Techniques/2D_collision_detection
    function collides(obj1, obj2) {
      return obj1.x < obj2.x + obj2.width &&
             obj1.x + obj1.width > obj2.x &&
             obj1.y < obj2.y + obj2.height &&
             obj1.y + obj1.height > obj2.y;
    }
    // game loop
    function loop() {
      requestAnimationFrame(loop);
      context.clearRect(0,0,canvas.width,canvas.height);
      // move paddle by it's velocity
      paddle.x += paddle.dx;
      // prevent paddle from going through walls
      if (paddle.x < wallSize) {
        paddle.x = wallSize
      }
      else if (paddle.x + brickWidth > canvas.width - wallSize) {
        paddle.x = canvas.width - wallSize - brickWidth;
      }
      // move ball by it's velocity
      ball.x += ball.dx;
      ball.y += ball.dy;
      // prevent ball from going through walls by changing its velocity
      // left & right walls
      if (ball.x < wallSize) {
        ball.x = wallSize;
        ball.dx *= -1;
      }
      else if (ball.x + ball.width > canvas.width - wallSize) {
        ball.x = canvas.width - wallSize - ball.width;
        ball.dx *= -1;
      }
      // top wall
      if (ball.y < wallSize) {
        ball.y = wallSize;
        ball.dy *= -1;
      }
      // reset ball if it goes below the screen
      if (ball.y > canvas.height) {
        ball.x = 130;
        ball.y = 260;
        ball.dx = 0;
        ball.dy = 0;
      }
      // check to see if ball collides with paddle. if they do change y velocity
      if (collides(ball, paddle)) {
        ball.dy *= -1;
        // move ball above the paddle otherwise the collision will happen again
        // in the next frame
        ball.y = paddle.y - ball.height;
      }
      // check to see if ball collides with a brick. if it does, remove the brick
      // and change the ball velocity based on the side the brick was hit on
      for (let i = 0; i < bricks.length; i++) {
        const brick = bricks[i];
        if (collides(ball, brick)) {
          // remove brick from the bricks array
          bricks.splice(i, 1);
          // ball is above or below the brick, change y velocity
          // account for the balls speed since it will be inside the brick when it
          // collides
          if (ball.y + ball.height - ball.speed <= brick.y ||
              ball.y >= brick.y + brick.height - ball.speed) {
            ball.dy *= -1;
          }
          // ball is on either side of the brick, change x velocity
          else {
            ball.dx *= -1;
          }
          break;
        }
      }
      // draw walls
      context.fillStyle = '#7F7F7F';
      context.fillRect(0, 0, canvas.width, wallSize);
      context.fillRect(0, 0, wallSize, canvas.height);
      context.fillRect(canvas.width - wallSize, 0, wallSize, canvas.height);
      // draw ball if it's moving
      if (ball.dx || ball.dy) {
        context.fillRect(ball.x, ball.y, ball.width, ball.height);
      }
      // draw bricks
      bricks.forEach(function(brick) {
        context.fillStyle = brick.color;
        context.fillRect(brick.x, brick.y, brick.width, brick.height);
      });
      // draw paddle
      context.fillStyle = '#000';
      context.fillRect(paddle.x, paddle.y, paddle.width, paddle.height);
    }
    // listen to keyboard events to move the paddle
    document.addEventListener('keydown', function(e) {
      // left arrow key
      if (e.which === 37) {
        paddle.dx = -3;
      }
      // right arrow key
      else if (e.which === 39) {
        paddle.dx = 4;
      }
      // space key
      // if they ball is not moving, we can launch the ball using the space key. ball
      // will move towards the bottom right to start
      if (ball.dx === 0 && ball.dy === 0 && e.which === 32) {
        ball.dx = ball.speed;
        ball.dy = ball.speed;
      }
    });
    // listen to keyboard events to stop the paddle if key is released
    document.addEventListener('keyup', function(e) {
      if (e.which === 37 || e.which === 39) {
        paddle.dx = 0;
      }
    });
    // listen to keyboard events to close game
    document.addEventListener('keydown', function(e) {
      if (e.which === 27) {
        $('body').removeClass('modal-open');
      }
    });
    // start the game
    requestAnimationFrame(loop);

    //This wonderful game was provided by Steven Lambert (https://gist.github.com/straker)
</script>
</body>
</html>
