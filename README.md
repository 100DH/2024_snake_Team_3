# 2024_snake_Team_3
24년 그래픽스 뱀 게임 3조

## 3조 snake 게임 변형 팀 프로젝트
조장 : 20210815 백대현
조원 : 20210811 박신원 , 20210830 천예준

### 소감
#### 20210815 백대현
그래픽스 수업에서 두 번째로 하는 팀 프로젝트인 만큼 처음 했을때보다 다른 학생들과 함께 프로젝트를 하는것이 좀 더 수월하게 느껴졌고, snake게임의 코드를 변형하여 하나의 작품을 만들면서 여러가지 기능들을 추가하며 여태까지 배웠던 내용들을 복습하고, 공부할 수 있는 기회가 되어서 좋았습니다. 코드를 작성하며 뜻대로 풀리지 않는 부분이 있었지만 조원들과 함께 소통하며 머리를 맞대고 고민하니 금방금방 해결할 수 있었고, 혼자 하는것보다 훨씬 좋은 작품을 만들 수 있었던 것 같습니다. 하지만 한편으론 아직도 많은 연습이 필요하다고 생각되고, 앞으로도 열심히 해서 더 좋은 작품을 만들고 싶습니다.

#### 20210811 박신원
비록 교수님이 올려주신 코드 기반이지만 팀프로젝트로 힘을 합쳐 더 발전시킨 게임을 만들었다는것이 뿌듯했습니다.
코드를 작성하며 기능을 추가할 때 분명 제대로 틀린부분없이 작성 했음에도 불구하고 작동이 안될 때에는 길어진 코드를 다시 한번 봐야해서
난감했지만 그 과정을 통해 잘못된 부분이나 누락된 부분을 찾아내고 수정하여 정상적으로 작동을 하게 만들었을 때에는 기쁨과 성취감이 들었습니다.
이런 경험을 토대로 코드를 작성하고 팀과 함께 작업물을 만드는 능력이 성장했다고 느꼈습니다. 이번에는 p5.js로 만들었지만 이후 Three.js를 배우고 좀더 본격적으로 Three.js를 통해 작업물을 만드는 것이 기대가 됩니다.

#### 20210830 천예준
이번 과제를 하면서 느꼈던 것은 누구나 많은 생각을 가지고 있고 기발한 아이디어를 떠올리지만 그것을 프로그래밍 하는 것은 쉽지 않다 라는 생각이 크게 들었던 시간이였던 것 같습니다. 지렁이게임을 바탕으로 여러 기능을 넣는 과정에 있어 생각처럼 실행이 안되거나 아니면 어떻게 해야 실행이 될지 감을 잡기 힘든 것도 있었습니다. 그래서 위와 같이 느꼈던 것 같고, 그 과정에서 답답함을 느끼기도 했지만 꼭 이뤄내고 싶다는 생각이 들어 더 열심히 할려고 했던 것 같습니다. 많은 연습과 경험을 통해 나중엔 제가 원하는 것을 생각만 하는 것이 아니라, 실행이 가능하도록 하는 실력을 가져야 겠다는 목표를 가지게 되었습니다. 저는 그 목표를 이루기 위해 계속 나아갈 것이고, 과정 중 하나인 그래픽스 수업을 통해 더 성장 해나갈 것입니다.

## 코드 소개
저희 조는 Snake 게임의 기본 틀에서 여러가지 기능들을 추가해 보았습니다.
먼저 코드를 실행하면 제일 먼저 볼 수 있는 부분은 바로 타이틀 화면의 추가입니다.
타이틀 화면에서는 Snake Game이라는 문구로 어떤 게임인지 바로 알 수 있도록 하였고, createButton을 이용하여
게임 시작 버튼, Easy, Normal, Hard의 3개의 버튼으로 난이도를 정할 수 있도록 하였고, Input 기능을 이용하여
사용자의 이름을 입력받도록 하였습니다.

다음으로는 게임을 시작했을 경우인데요.
난이도를 선택하지 않고 Start Game을 선택하면 기본 설정된 난이도인 Normal 난이도로 게임이 실행됩니다.
게임을 시작하면 랜덤한 위치에 generateObstacles 함수를 이용하여 장애물을 생성하도록 했습니다.
해당 장애물은 생성되는 food와 위치가 겹치지 않도록 코드를 작성하였으며, 장애물에 snake가 닿을 시, life가 한 개 줄어들도록 작성했습니다.
life가 0이되면 Game Over가 출력되고 약 3초뒤에 타이틀 화면으로 다시 돌아가게 됩니다.
난이도별 차이점은 기본으로 제공되는 life의 갯수, 게임 속도의 차이, 시야를 방해하는 방해물의 갯수 등이 있습니다.

Easy 난이도를 선택하면 느린 게임 속도와 5개의 life, 1개의 시야 방해물이 존재합니다.
Normal 난이도를 선택하면 적당한 게임 속도와 3개의 life, 2개의 시야 방해물이 존재합니다.
Hard 난이도를 선택하면 빠른 게임 속도와 1개의 life, 4개의 시야 방해물이 존재합니다.

하단의 바 에는 현재 점수, 최고 기록, 남은 라이프, 난이도, 플레이어의 이름 등을 표시하도록 작성했습니다.
또한 게임 도중 P를 누르면 Pause 상태가 되어 현재 점수와 최고 점수, 플레이어의 이름을 확인할 수 있으며 잠시 게임이 멈추게 되고, 다시 한번 P를 누르게되면 게임을 계속해서 진행할 수 있게 됩니다.

생성되는 먹이를 계속 먹다보면 30퍼센트의 확률로 라이프가 1 늘어나고 라이프가 늘어나면 약 2초간 뱀의 머리부분이 반짝거리는 효과를 넣었습니다.

벽에 닿거나 자신의 꼬리부분에 닿으면 현재 점수가 초기화되며, 목숨이 한 개 줄어들고, 장애물에 닿는다면 목숨만 줄어들고 현재 점수는 초기화되지 않도록 했습니다.

라이프를 모두 소진하여 게임이 종료되면 Game over 메시지와 입력했던 사용자의 이름, 최고기록이 표시되고 게임이 종료됩니다.

## 꾸미기
디자인적인 부분은 먼저 누가봐도 뱀 게임인것을 알 수 있도록 타이틀 화면에 뱀 캐릭터를 추가하였고, 뱀의 눈이 마우스의 움직임을 따라오도록 코드를 작성하였습니다.
Pause와 Game over를 할 때에도 눈을 감은 뱀의 모습이 나오도록 하여 허전하지 않도록 만들었습니다.

게임을 시작한 후 뱀이 먹게되는 먹이는 쥐 캐릭터의 사진을 입혀놓았고, 장애물은 뱀의 천적인 매의 사진을 넣었습니다.
게임이 진행되는동안 시야를 방해하는 방해물의 경우에도 마찬가지로 뱀의 천적인 매의 사진을 넣었고,
배경에는 뱀에 풀숲을 헤쳐 돌아다니는것처럼 풀밭의 사진을 가져와서 넣었습니다.


## 각자 맡은 부분
20210815 백대현
- 타이틀 화면, Pause, Game Over 화면 꾸미기( 뱀 캐릭터 만듦 )
- 게임 시작, 난이도 선택 버튼 생성
- 타이틀 화면 출력되도록 제작
- 장애물, 먹이 ,시야 방해물 , 배경 사진 입히기
- 먹이를 먹고 생명력이 늘어났을 때 뱀의 머리부분 반짝이는 효과 추가
- 게임 난이도에 따른 차이점 생성(Life 갯수, 게임 속도, 장애물 갯수)
- 게임 종료 후 타이틀 화면으로 복귀하는 코드 작성 

20210811 박신원
- 게임 시작 시 랜덤한 위치에 생성되는 장애물 생성
- 타이틀 화면에서 플레이어의 이름을 입력받고, Pause를 실행했을 때, Game Over했을 때 플레이어의 이름과 최고 기록이 출력되도록 함
  
20210830 천예준
- 게임이 시작됐을 때 일정 구간을 반복해서 이동하며 플레이어의 시야를 방해하는 방해물 생성
- P 버튼 입력 시 게임을 일시 정지 하도록 함

## 코드
        //Delcare Global Variables
        let s;
        let scl = 20;
        let food;
        let playing = false;
        let buttonClicked = false;
        let playfield = 600;
        let difficulty = '';
        let obstacles = [];
        let gameOverTime = 0;
        let gamestop = false;
        let life = 0;
        let obstacleCount = 0; //장애물 
        let img1;
        let img2;
        let img3;
        let img4;
        let lifehealing = false;
        let lifeHealingTimer = 0; // 생명력 회복 색상 유지 시간
        let lifeHealingDuration = 2000; // 생명력 회복 색상 유지 기간 (2초)
        
        let startButton;
        let easyButton;
        let normalButton;
        let hardButton;
        let nameInput; // 이름 입력 박스
        
        let x1 = 0; 
        let x2 = 0; 
        let x3 = 0; 
        let x4 = 0;
        let dim = 80.0;
        
        let e1, e2;
        
        class Eye { //눈알 그리기
          constructor(tx, ty, ts) {
            this.x = tx;
            this.y = ty;
            this.size = ts;
            this.angle = 0;
          }
        
          update(mx, my) {
            this.angle = atan2(my - this.y, mx - this.x);
          }
        
          display() {
            push();
            translate(this.x, this.y);
            fill(255);
            ellipse(0, 0, this.size, this.size);
            rotate(this.angle);
            fill(0, 0, 0);
            ellipse(this.size / 4, 0, this.size / 2, this.size / 2);
            pop();
          }
        }
        
        
        
        function setup() {
          createCanvas(playfield, 640);
          background(51);
          img1 = loadImage("https://img.lovepik.com/png/20231112/falcon-clipart-cartoon-falcon-with-big-beak-cartoon-illustration-vector_565407_wh860.png");
          img2 = loadImage("https://png.pngtree.com/thumb_back/fw800/background/20231230/pngtree-fresh-and-natural-realistic-seamless-green-lawn-grass-carpet-texture-with-image_13922800.png");
          img3 = loadImage("https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcROAGblt_QHghz5AC0BBJgySlzzJKe0Kl-md_8tuS1t5A&s");
          img4 = loadImage("https://png.pngtree.com/png-vector/20240407/ourlarge/pngtree-a-flying-hawk-bird-art-pic-png-image_12270473.png");
          s = new Snake();
          frameRate (10);
          pickLocation();
          
          e1 = new Eye(230, 100, 120);
          e2 = new Eye(400, 100, 100);
          
          startButton = createButton('Start Game'); //버튼 생성
          startButton.position(width / 2 - startButton.width / 2 - 30, height / 2);
          styleButton(startButton);
          startButton.mousePressed(startGame);
        
          easyButton = createButton('Easy');
          easyButton.position(width / 2 - easyButton.width / 2 - 20, height / 2 + 50);
          styleButton(easyButton);
          easyButton.mousePressed(function() {setDifficulty('easy');});
        
          normalButton = createButton('Normal');
          normalButton.position(width / 2 - normalButton.width / 2 - 20, height / 2 + 100);
          styleButton(normalButton);
          normalButton.mousePressed(function() {setDifficulty('normal');});
        
          hardButton = createButton('Hard');
          hardButton.position(width / 2 - hardButton.width / 2 - 20, height / 2 + 150);
          styleButton(hardButton);
          hardButton.mousePressed(function() { setDifficulty('hard');});
          
           // 이름 입력 박스 생성
          
          nameInput = createInput();
          nameInput.position(width / 2 - 53, height / 2 + 277);
          nameInput.size(300, 30);
          
        }
        
        // p5js Draw function - required
        
        function draw() {
          
          if (!playing && !buttonClicked) {
            background(150,255,100);
            fill(0);
            rect(50,50,width-100,height-100);
            fill(255,0,0);
            rect(275,100,50,400);
            fill(150,255,100);
            ellipse(310, 100, 300, 230);
            
            
            fill(255);
            textAlign(CENTER, CENTER);
            textSize(48);
            text("Snake Game", width / 2, height / 2 - 50);
            textSize(35);
            fill(0);
            text("Input name : ",width /2 - 160, height/2 + 295);
            
            
            e1.update(mouseX, mouseY);
            e2.update(mouseX, mouseY);
        
            e1.display();
            e2.display();
            
            
            
          }
          else if (playing) {
            background(51);
            image(img2, 0, 0, width, height);
            scoreboard();
            textAlign(LEFT, LEFT);
        
            if (s.eat(food)) {
              pickLocation();
            }
            s.death();
            s.update();
            s.show();
        
            fill(127, 55, 255);
            image(img3,food.x, food.y, scl, scl);
            
            for (let i = 0; i < obstacles.length; i++) { //장애물 생성
              image(img1, obstacles[i].x, obstacles[i].y, scl, scl)
            }
            
            blind(); //블라인드 생성
            
            for (let i = 0; i < obstacles.length; i++) {
              let obs = obstacles[i];
              let d = dist(s.x, s.y, obs.x, obs.y);
              if (d < 1) {
                life -= 1;
                
                
              }
              else if(life == 0){
                gameOver();
                break;
              }
            } 
            
            if (lifehealing && millis() < lifeHealingTimer + lifeHealingDuration) {
              fill(random(255), random(255), random(255)); // 랜덤한 색으로 머리의 색상 변경
              rect(s.x, s.y, scl, scl); // 뱀 머리 그리기
            } else {
              lifehealing = false; // 생명력 회복 플래그 초기화
            }
            
          } else if (!gameOverTime){
            // 일시정지 메시지 표시
            background(150,255,100);
            fill(0);
            rect(50,50,width-100,height-100);
            fill(150,255,100);
            ellipse(310, 100, 300, 230);
          
            fill(255);
            ellipse(230, 100, 120, 120);
            ellipse(400, 100, 105, 105);
            fill(0);
            rect(185, 100, 90, 20)
            rect(360, 100, 80, 20)
            
            fill(255);
            textSize(32);
            textAlign(CENTER, CENTER);
            text("PAUSED", width / 2, height / 2 - 50);
            text("Score : ", width / 2 - 65, height / 2);
            text("HighScore : ", width / 2 - 30, height / 2 + 50);
            text("Player : ", width / 2 - 60, height / 2 + 100);
            textAlign(LEFT, LEFT);
            text(s.score, width / 2 + 80, height / 2);
            text(s.highscore, width / 2 + 80, height / 2 + 50);
            text(un,width / 2 , height / 2 + 100);
            
          }
          if (gameOverTime !== 0 && millis() > gameOverTime + 3000) {
            // 3초뒤 타잍틀 화면으로 이동
            gameOverTime = 0; 
            returnToTitle(); 
          }
        }
        
        function styleButton(button) { //버튼 
          button.style('background-color', 'red'); // 버튼 배경 색
          button.style('color', 'white'); // 버튼 글자 색
          button.style('font-size', '20px'); // 글자 크기
          button.style('border-radius', '50px'); // 버튼 모서리 둥근 정도
          button.style('padding', '5px 20px'); // 버튼 두께
          button.style('border', 'none'); // 경계
          button.style('cursor', 'pointer'); // 커서 r
        }
        
        function gameOver() { //게임오버
          gamestop = false;
          playing = false;
          obstacles = []; // 장애물 초기화
          let record = [un +" / "+ s.highscore];
          background(150,255,100);
          fill(0);
          rect(50,50,width-100,height-100);
          fill(150,255,100);
          ellipse(310, 100, 300, 230);
          
          fill(255);
          ellipse(230, 100, 120, 120);
          ellipse(400, 100, 105, 105);
          fill(0);
          rect(185, 100, 90, 20)
          rect(360, 100, 80, 20)
          
          textSize(32);
          textAlign(CENTER, CENTER);
          fill(255);
          text("Game Over", width / 2, height / 2);
          
          textSize(20);
          text("Record : "+ record, width / 2, height / 2 + 50);
          gameOverTime = millis();
        }
        
        function returnToTitle() { //타이틀로 돌아가기
          playing = false;
          startButton.show(); //버튼 다시 보이기 
          easyButton.show();
          normalButton.show();
          hardButton.show();
          nameInput.show();
          buttonClicked = false; 
          obstacles = []; // 장애물 초기화
        }
        
        function generateObstacles() { //장애물 생성
          let cols = floor(playfield / scl);
          let rows = floor(playfield / scl);
          
          for (let i = 0; i < obstacleCount; i++) {
            let obstacle = createVector(floor(random(cols)), floor(random(rows)));
            obstacle.mult(scl);
            obstacles.push(obstacle);
          }
        }
        
        function setDifficulty(diff) { //난이도 설정
          difficulty = diff;
        }
        
        function startGame() { //게임시작 버튼
          un = nameInput.value(); // 사용자 이름 가져오기
          playing = true; 
          buttonClicked = true; 
          gamestop = true;
          startButton.hide(); //시작 시 버튼 
          easyButton.hide();
          normalButton.hide();
          hardButton.hide();
          nameInput.hide();
          
          
          
          if (!difficulty) { // 난이도 미 선택시
            difficulty = 'normal'; // 기본 난이도는 중간으로 설정
          }
        
          if (difficulty === 'easy') { //쉬움
            life = 5;
            frameRate(10);
            obstacleCount = 5;
            
          } else if (difficulty === 'normal') { //중간
            life = 3;
            frameRate(13);
            obstacleCount = 10;
            
          } else if (difficulty === 'hard') { //어려움
            life = 1;
            frameRate(17);
            obstacleCount = 15;
          }
          
          s = new Snake();
          pickLocation();
          generateObstacles(); //장애물 생성
        }
        
        function pickLocation() {
          let cols = floor(playfield/scl); // 행렬 열의 개수 계산
          let rows = floor(playfield/scl); // 행렬 행의 개수 계산
          
          food = createVector(floor(random(cols)), floor(random(rows))); // 무작위로 음식의 위치 선택
          food.mult(scl);
        
          // 음식이 장애물과 겹치는지 확인
          let foodIntersectsWithObstacle = false;
          for (let i = 0; i < obstacles.length; i++) {
            let obs = obstacles[i];
            let d = dist(food.x, food.y, obs.x, obs.y);
            if (d < 1) {
              foodIntersectsWithObstacle = true;
              break;
            }
          }
        
          // 음식이 장애물과 겹친다면 새로운 위치 선택
          if (foodIntersectsWithObstacle) {
            pickLocation();
            return;
          }
        
          // 음식이 뱀의 꼬리와 겹치는지 확인
          for (let i = 0; i < s.tail.length; i++) {
            let pos = s.tail[i];
            let d = dist(food.x, food.y, pos.x, pos.y);
            if (d < 1) {
              pickLocation();
              return;
            }
          }
        }
        
        
        // scoreboard
        
        function scoreboard() {
          fill(0);
          rect(0, 600, 650, 40);
          fill(255);
          textFont("Georgia");
          textSize(15);
          text("Score : ", 10, 625);
          text("Highscore : ", 100, 625);
          text(s.score, 70, 625);
          text(s.highscore, 200, 625);
          text("life : ", 230, 625);
          text(life, 280, 625);
          text("Player : " + un, 450, 625);
          
          if (difficulty == 'easy') { //난이도 표시
            text("Difficulty : ", 300, 625);
            text("Easy", 380, 625);
          }
          else if (difficulty == 'normal') {
            text("Difficulty : ", 300, 625);
            text("Normal", 380, 625);
          }
          else if (difficulty == 'hard') {
            text("Difficulty : ", 300, 625);
            text("Hard", 380, 625);
          }
          else {
            text("Difficulty : ", 300, 625);
            text("Normal", 380, 625);
          }
        }
        
        // CONTROLS function
        
        function keyPressed() {
          if (gamestop) {
          if (keyCode === UP_ARROW){
              s.dir(0, -1);
          }else if (keyCode === DOWN_ARROW) {
              s.dir(0, 1);
          }else if (keyCode === RIGHT_ARROW) {
              s.dir (1, 0);
          }else if (keyCode === LEFT_ARROW) {
              s.dir (-1, 0);
          }
          else if (key === "p" || key === "P") { // P누르면 게임 일시정지
            playing = !playing;
            }
          }
        }
        // SNAKE OBJECT
        
        function Snake() {
          this.x =0;
          this.y =0;
          this.xspeed = 1;
          this.yspeed = 0;
          this.total = 0;
          this.tail = [];
          this.score = 0;
          this.highscore = 0;
        
          this.dir = function(x,y) {
            this.xspeed = x;
            this.yspeed = y;
          }
        
          this.eat = function(pos) {
            let d = dist(this.x, this.y, pos.x, pos.y);
            if (d < 1) {
              this.total++;
              this.score++;
              text(this.score, 70, 625);
              if (this.score > this.highscore) {
                this.highscore = this.score;
              }
              text(this.highscore, 230, 625);
              
              // 30%의 확률로 생명 회복
              if (random(1) < 0.3) {
                life++;
                lifehealing = true;
                lifeHealingTimer = millis(); // 생명력 회복 시간 기록
                
                
              }
              
              return true;
            } else {
              return false;
            }
          }
        
          this.death = function() {
            for (let i = 0; i < this.tail.length; i++) {
              let pos = this.tail[i];
              let d = dist(this.x, this.y, pos.x, pos.y);
              if (d < 1) {
                life -= 1;
                this.total = 0;
                this.score = 0;
                this.tail = [];
                
              }
            }
          }
        
          this.update = function(){
            if (this.total === this.tail.length) {
              for (let i = 0; i < this.tail.length-1; i++) {
                this.tail[i] = this.tail[i+1];
            }
        
            }
            this.tail[this.total-1] = createVector(this.x, this.y);
        
            this.x = this.x + this.xspeed*scl;
            this.y = this.y + this.yspeed*scl;
        
            this.x = constrain(this.x, 0, playfield-scl);
            this.y = constrain(this.y, 0, playfield-scl);
        
        
          }
          this.show = function(){
            fill(127, 200, 0);
            for (let i = 0; i < this.tail.length; i++) {
                rect(this.tail[i].x, this.tail[i].y, scl, scl);
            }
            fill(255,255,0);
            rect(this.x, this.y, scl, scl);
          }
        }
        
        function blind(){ //가림막
          push();
            // 각 블록의 x값을 다른 속도로 증가시켜 움직이게 만들기
            x1 = x1 + 3; // 첫 번째 블록의 속도
            x2 = x2 + 4.5; // 두 번째 블록의 속도
            x3 = x3 + 6; // 세 번째 블록의 속도
            x4 = x4 + 10;
            // 도형이 캔버스 밖으로 나가면, 위치를 리셋한다.
            if (x1 > width + dim) {
              x1 = -dim;
            }
            if (x2 > width + dim) {
              x2 = -dim;
            }
            if (x3 > width + dim) {
              x3 = -dim;
            }
            if (x4 > width + dim) {
              x4 = -dim;
            }
            let yOffset = sin(frameCount * 0.1) * 20; // 주기적인 움직임을 생성하기 위해 sin 함수 사용
            // 첫 번째 블록
            
            push();
            translate(x1, height / 2 - dim * 1.5);
            fill(255);
            image(img4,-dim / 2,  - dim * 1.5 + yOffset*5, dim, dim);
            pop();
            
            if(difficulty == "normal" || difficulty == "hard"){
            // 두 번째 블록
            push();
            translate(x2, height / 2 - dim / 2);
            fill(0);
            image(img4,-dim / 2, -dim / 2 + yOffset*-10, dim, dim);
            pop();
            }
            
            if(difficulty == "hard"){
            // 세 번째 블록
            push();
            translate(x3, height / 2 + dim / 2);
            fill(125);
            image(img4,-dim / 2, -dim / 2 + yOffset*10, dim, dim);
            pop();
            
            // 네 번째 블록
            push();
            translate(x4, height / 2 + dim / 2);
            fill(125);
            image(img4,-dim / 2, -dim / 2 + yOffset*-5, dim, dim);
            pop();
            }
          
          pop();
        }
