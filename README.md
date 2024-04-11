# 2024_snake_Team_3
24년 그래픽스 뱀 게임 3조

## 3조 snake 게임 변형 팀 프로젝트
조장 : 20210815 백대현
조원 : 20210811 박신원 , 20210830 천예준

<img src="https://github.com/100DH/2024_snake_Team_3/assets/93199016/df8e661e-7843-4398-99d5-72b111b0a4fc"></img>

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
사용자의 이름을 입력받도록 하였습니다. 그리고 Option 버튼을 추가하여 여러가지 설정을 할 수 있는 화면을 작성하였습니다.
Option 화면에서는 봄, 여름, 가을, 겨울의 테마를 가진 4개의 테마 중 하나를 골라서 적용해 게임의 배경화면을 변경할 수 있고,
colorPicker를 이용해서 뱀의 몸통 색깔을 마음대로 정할 수 있도록 코드를 작성했습니다.
옵션 창을 벗어나 타이틀 화면으로 돌아가고 싶다면 옵션 버튼을 한번 더 누르면 됩니다.
만약 아무런 설정도 건드리지 않고 게임을 시작할 시, 뱀의 몸통은 검정색, 배경 색깔을 회색으로 나오도록 했습니다.

다음으로는 게임을 시작했을 경우인데요.
난이도를 선택하지 않고 Start Game을 선택하면 기본 설정된 난이도인 Normal 난이도로 게임이 실행됩니다.
게임을 시작하면 랜덤한 위치에 generateObstacles 함수를 이용하여 지뢰 모양의 장애물을 생성하도록 했습니다.
해당 장애물은 생성되는 food와 위치가 겹치지 않도록 코드를 작성하였으며, 장애물에 snake가 닿을 시, life가 한 개 줄어들도록 작성했습니다.
life가 0이되면 Game Over가 출력되고 약 3초뒤에 타이틀 화면으로 다시 돌아가게 됩니다.
난이도별 차이점은 기본으로 제공되는 life의 갯수, 게임 속도의 차이, 시야를 방해하는 방해물의 갯수 등이 있습니다.
뱀이 잡아먹는 음식의 모양은 여러가지 도형들을 조합해서 쥐 모양을 만들었고,
시야 방해물은 계속해서 날아다니는 물건이 무엇이 있을까 생각해보다가 풍선이 좋을 것 같아 풍선의 모양을 채택했습니다.


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
버튼의 색을 빨간색으로 하여 뱀이 혀를 내밀고 있는 것 처럼 보이도록 만들었습니다.
타이틀 화면과 Option 화면에서는 뱀이 마우스의 커서를 따라 눈이 움직이도록 만들었고,
Pause와 Game over를 할 때에도 눈을 감은 뱀의 모습이 나오도록 하여 허전하지 않도록 만들었습니다.

게임을 시작한 후 뱀이 먹게되는 먹이는 쥐의 모양을 만들었고, 장애물은 밟으면 체력이 깎이도록 지뢰의 모양을 만들었습니다.
게임이 진행되는동안 시야를 방해하는 방해물의 경우에는 하늘을 날아다니는 것이 무엇이 있을까 생각하다가 풍선의 모양을 채택했습니다.
배경은 Option 창으로 들어가서 Theme 1부터 4까지 4가지의 종류가 존재하는데요, 첫 번째 테마는 봄 느낌이 나도록 초록색 바탕에
꽃들이 흩뿌려져 있는 모습을 만들었고, 두 번째 테마는 여름을 표현하기 위해 해변과 바다, 야자수를 넣었습니다.
세 번째 테마는 가을의 모습으로 은행나무와 떨어진 낙엽을 표현하였고, 마지막 네 번째 테마는 겨울로, 눈사람과 눈, 나무등으로
겨울을 표현해 주었습니다. 테마는 옵션 창에 들어가서 언제든지 원하는 것으로 변경이 가능하고, 선택하지 않을 시 배경은 회색 바탕으로 나오게 됩니다.

또한 뱀의 몸통 색깔도 colorPicker를 통해서 마음대로 지정할 수 있도록 했기에 원하는 색깔을 지정한 후 게임을 진행하면 됩니다.


## 각자 맡은 부분
20210815 백대현
- 타이틀 화면, Pause, Game Over, option 화면 꾸미기( 마우스 커서를 따라 눈이 움직이는 뱀 캐릭터 )
- 각 계절별 테마 제작
- 4개의 테마 선택 기능 제작
- 옵션 창 구현
- 장애물과 먹이, 시야 방해물인 풍선의 디자인 제작
- colorPicker를 이용하여 뱀의 몸통 색깔 선택 기능 구현
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
        let difficulty = ''; //난이도
        let obstacles = [];
        let gameOverTime = 0; //게임 오버 후 딜레이
        let gamestop = false; //사망시 게임 중단
        let pause = false; //게임 멈춤
        
        let life = 0;
        let obstacleCount = 0; //장애물 
        
        let lifehealing = false;
        let lifeHealingTimer = 0; // 생명력 회복 색상 유지 시간
        let lifeHealingDuration = 2000; // 생명력 회복 색상 유지 기간 (2초)
        
        let picker;
        let snakeColor;
        
        
        let startButton;
        let easyButton;
        let normalButton;
        let hardButton;
        let optionButton;
        
        let themeButton1;
        let themeButton2;
        let themeButton3;
        let themeButton4;
        
        let nameInput; // 이름 입력 박스
        
        let inOptionsScreen = false;
        
        let springTheme = false;
        let summerTheme = false;
        let autumnTheme = false;
        let winterTheme = false;
        
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
          
          optionButton = createButton('Option'); //옵션 버튼 생성
          optionButton.position(width /2 + 150 , height / 2 + 230);
          styleButton(optionButton);
          optionButton.mousePressed(function() {  inOptionsScreen = !inOptionsScreen; });
          
          themeButton1 = createButton('Theme1'); //봄 테마 버튼 생성
          themeButton1.position(width /2  - 220, height / 2 - 80);
          styleButton(themeButton1);
          themeButton1.mousePressed(function() {  springTheme = !springTheme;
                                                  summerTheme = false;
                                                  autumnTheme = false;
                                                  winterTheme = false;
                                               });
          
          themeButton2 = createButton('Theme2'); //여름 테마 버튼 생성
          themeButton2.position(width /2  - 220, height / 2 - 0);
          styleButton(themeButton2);
          themeButton2.mousePressed(function() {  summerTheme = !summerTheme;
                                                  springTheme = false;
                                                  autumnTheme = false;
                                                  winterTheme = false;
                                               });
          
          themeButton3 = createButton('Theme3'); //가을 테마 버튼 생성
          themeButton3.position(width /2  - 220, height / 2 + 80);
          styleButton(themeButton3);
          themeButton3.mousePressed(function() {  autumnTheme = !autumnTheme;
                                                  springTheme = false;
                                                  summerTheme = false;
                                                  winterTheme = false;
                                               });
          
          themeButton4 = createButton('Theme4'); //겨울 테마 버튼 생성
          themeButton4.position(width /2  - 220, height / 2 + 160);
          styleButton(themeButton4);
          themeButton4.mousePressed(function() {  winterTheme = !winterTheme;
                                                  springTheme = false;
                                                  summerTheme = false;
                                                  autumnTheme = false;
                                               });
          
          picker = createColorPicker('black'); //색상 선택기 생성
          stylePicker(picker);
          picker.position(300, 300);
          snakeColor = color(255);
           // 이름 입력 박스 생성
          
          nameInput = createInput();
          nameInput.position(width / 2 - 53, height / 2 + 277);
          nameInput.size(300, 30);
          
        }
        
        // p5js Draw function - required
        
        function draw() {
          
            
          
          if (!playing && !buttonClicked && !inOptionsScreen) {
            background(127,127,127);
            themeOutput(); //테마출력
            drawborder(); //테두리그리기
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
            
            startButton.show(); //버튼 다시 보이기 
            easyButton.show();
            normalButton.show();
            hardButton.show();
            nameInput.show();
            optionButton.show();
            
            themeButton1.hide();
            themeButton2.hide();
            themeButton3.hide();
            themeButton4.hide();
            picker.hide();
            
          }
          else if (playing) {
            background(51);
            themeOutput(); //테마 출력
            scoreboard();
            textAlign(LEFT, LEFT);
        
            if (s.eat(food)) {
              pickLocation();
            }
            s.death();
            s.update();
            s.show();
        
            fill(127, 55, 255);
            drawRat(food.x, food.y, scl, scl);
            
            for (let i = 0; i < obstacles.length; i++) { //장애물 생성
              obstacleRect(obstacles[i].x, obstacles[i].y, scl, scl)
              
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
            
          } else if (pause){
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
          
          else if (inOptionsScreen) { //옵션 창 출력
              
              background(127,127,127);
              themeOutput();  //테마 버튼 클릭시 테마 출력
              drawborder(); //테두리 출력
              drawOptionsScreen() //옵션창 뱀 출력
              startButton.hide(); //시작 시 버튼 
              easyButton.hide();
              normalButton.hide();
              hardButton.hide();
              nameInput.hide(); 
              handleOptionsScreen();
              
              
          }
          
          if (gameOverTime !== 0 && millis() > gameOverTime + 3000) {
            // 3초뒤 타잍틀 화면으로 이동
            gameOverTime = 0; 
            returnToTitle(); 
          }
        }
        
        function styleButton(button) { //버튼  스타일 결정
          button.style('background-color', 'red'); // 버튼 배경 색
          button.style('color', 'white'); // 버튼 글자 색
          button.style('font-size', '20px'); // 글자 크기
          button.style('border-radius', '50px'); // 버튼 모서리 둥근 정도
          button.style('padding', '5px 20px'); // 버튼 두께
          button.style('border', 'none'); // 경계
          button.style('cursor', 'pointer'); // 커서 r
        }
        
        function stylePicker(picker){ //색상 선택기의 스타일 
          picker.style('width', '200px');
          picker.style('height', '200px');
          picker.style('border', 'none');
          picker.style('border-radius', '10px');
        }
        
        function gameOver() { //게임오버
          gamestop = false;
          playing = false;
          obstacles = []; // 장애물 초기화
          let record = [un +" / "+ s.highscore];
          background(0,0,0);
          drawborder();
          
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
          optionButton.hide();
          
          
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
            pause = !pause;
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
            fill(snakeColor);
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
            drawBallon(-dim / 2,  - dim * 1.5 + yOffset*5, dim, dim,255,0,0);
            pop();
            
            if(difficulty == "normal" || difficulty == "hard"){
            // 두 번째 블록
            push();
            translate(x2, height / 2 - dim / 2);
            fill(0);
            drawBallon(-dim / 2, -dim / 2 + yOffset*-10, dim, dim,255,140,0);
            pop();
            }
            
            if(difficulty == "hard"){
            // 세 번째 블록
            push();
            translate(x3, height / 2 + dim / 2);
            fill(125);
            drawBallon(-dim / 2, -dim / 2 + yOffset*10, dim, dim,30,144,255);
            pop();
            
            // 네 번째 블록
            push();
            translate(x4, height / 2 + dim / 2);
            fill(125);
            drawBallon(-dim / 2, -dim / 2 + yOffset*-5, dim, dim,148,0,211);
            pop();
            }
          
          pop();
        }
        
        function drawOptionsScreen() { // 옵션 화면 배경
            
            fill(150,255,100);
            ellipse(310, 100, 300, 230);
            
            e1.update(mouseX, mouseY);
            e2.update(mouseX, mouseY);
        
            e1.display();
            e2.display();
          
        }
        
        function drawborder() {
          push();
          noStroke();
          fill(150,255,100);
          rect(0,0,700,60)
          rect(0,0,60,700)
          rect(540,0,60,700)
          rect(0,580,700,60)
          pop();
        }
        
        function handleOptionsScreen() { // 옵션 화면에서 발생하는 이벤트 처리
          themeButton1.show();
          themeButton2.show();
          themeButton3.show();
          themeButton4.show();
          picker.show();
          
          
        }
        
        function themeOutput() {
          
          if(springTheme == true){
            drawSpringScene();
          }
          if(summerTheme == true){
            drawSummerScene();
          }
          if(autumnTheme == true){
            drawAutumnScene();
          }
          if(winterTheme == true){
            drawWinterScene();
          }
        }
        
        function drawSpringScene() { //봄 테마 
          push();
          noStroke();
          // 잔디 그리기
          fill(173, 255, 90); // 푸른 잔디색
          rect(0, 0, width, height); // 잔디
        
          // 꽃 그리기
          drawFlower1(width/200+90, height/200+100);
          drawFlower1(width/200+210, height/200+200);
          drawFlower1(width/200+300, height/200+300);
          drawFlower1(width/200+400, height/200+100);
          drawFlower1(width/200+500, height/200+200);
          drawFlower1(width/200+600, height/200+300);
          drawFlower1(width/200+110, height/200+580);
          drawFlower1(width/200+830, height/200+200);
          drawFlower1(width/200+900, height/200+300);
          
          drawFlower2(width/200+80, height/200+500);
          drawFlower2(width/200+200, height/200+300);
          drawFlower2(width/200+300, height/200+400);
          drawFlower2(width/200+400, height/200+500);
          drawFlower2(width/200+500, height/200+200);
          drawFlower2(width/200+700, height/200+300);
          drawFlower2(width/200+0, height/200+400);
          drawFlower2(width/200+110, height/200+250);
          drawFlower2(width/200+900, height/200+500);
          
          drawFlower3(width/200+100, height/200+350);
          drawFlower3(width/200+200, height/200+20);
          drawFlower3(width/200+300, height/200+150);
          drawFlower3(width/200+380, height/200+350);
          drawFlower3(width/200+520, height/200+300);
          drawFlower3(width/200+550, height/200+70);
          drawFlower3(width/200+0, height/200+200);
          drawFlower3(width/200+250, height/200+600);
          drawFlower3(width/200+200, height/200+500);
          drawFlower3(width/200+550, height/200+450);
          pop();
        }
        
        // 꽃 그리기 함수
        function drawFlower1(x, y) {
          push();
          noStroke();
          // 꽃잎
          fill(255, 105, 180); // 분홍색
          ellipse(x, y, 20, 20); // 중앙 꽃잎
          ellipse(x - 15, y, 20, 20); // 왼쪽 꽃잎
          ellipse(x + 15, y, 20, 20); // 오른쪽 꽃잎
          ellipse(x, y - 15, 20, 20); // 위쪽 꽃잎
          ellipse(x, y + 15, 20, 20); // 아래쪽 꽃잎
          fill(255,255,0);
          ellipse(x,y,20,20);
          pop();
        }
        function drawFlower2(x, y) {
          push();
          noStroke();
          // 꽃잎
          fill(255, 0, 0); // 빨간색
          ellipse(x, y, 20, 20); // 중앙 꽃잎
          ellipse(x - 15, y, 20, 20); // 왼쪽 꽃잎
          ellipse(x + 15, y, 20, 20); // 오른쪽 꽃잎
          ellipse(x, y - 15, 20, 20); // 위쪽 꽃잎
          ellipse(x, y + 15, 20, 20); // 아래쪽 꽃잎
          fill(255,255,0);
          ellipse(x,y,20,20);
          pop();
        }
        
        function drawFlower3(x, y) {
          push();
          noStroke();
          // 꽃잎
          fill(255, 105, 0); // 주황색
          ellipse(x, y, 20, 20); // 중앙 꽃잎
          ellipse(x - 15, y, 20, 20); // 왼쪽 꽃잎
          ellipse(x + 15, y, 20, 20); // 오른쪽 꽃잎
          ellipse(x, y - 15, 20, 20); // 위쪽 꽃잎
          ellipse(x, y + 15, 20, 20); // 아래쪽 꽃잎
          fill(255,255,0);
          ellipse(x,y,20,20);
          pop();
        }
        
        function drawSummerScene() { //여름 테마 그리기
          push();
          noStroke();
          // 하늘 그리기
          background(0, 191, 255); // 하늘색
        
          // 바다 그리기
          fill(65, 105, 225); // 파란색
          rect(0, height / 2, width, height / 2); // 바다
        
          // 해변 그리기
          fill(244, 164, 96); // 갈색
          rect(0, height / 2, width, height / 7); // 해변
        
          // 태양 그리기
          fill(255, 127, 0); // 주황
          ellipse(width / 8, height / 8, 100, 100); // 태양
        
          // 코코넛 나무 그리기
          drawCoconutTree(width / 2, height / 2);
          drawCoconutTree(width / 6, height / 1.7);
          drawCoconutTree(width /1.2, height / 1.8);
          pop();
        }
        
        function drawCoconutTree(x, y) {
          push();
          noStroke();
          // 나무 줄기
          fill(139, 69, 19); // 갈색
          rect(x - 10, y - 200, 20, 200); // 줄기
          
          push();
          // 나뭇잎
          fill(50, 205, 50); // 녹색
          ellipse(x + 50, y - 180, 80, 30); // 오른쪽 나뭇잎
          ellipse(x - 50, y - 180, 80, 30); // 왼쪽 나뭇잎
          push();
          
          ellipse(x-20, y - 230, 50, 120); // 윗부분 나뭇잎
          
          ellipse(x+20, y - 230, 50, 120); // 윗부분 나뭇잎
          pop();
          pop();
          
          // 코코넛
          fill(139, 69, 19); // 갈색
          ellipse(x - 20, y - 160, 30, 30); // 왼쪽 코코넛
          ellipse(x + 20, y - 160, 30, 30); // 오른쪽 코코넛
          fill(0);
          ellipse(x - 25, y - 150, 7, 7);
          ellipse(x - 15, y - 150, 7, 7);
          
          ellipse(x + 25, y - 150, 7, 7);
          ellipse(x + 15, y - 150, 7, 7);
          pop();
        }
        
        function drawAutumnScene() { //가을 테마 그리기
          push();
          noStroke();
          // 배경 그리기
          background(255, 228, 181); // 밝은 갈색 배경
        
          // 땅 그리기
          fill(139, 69, 19); // 갈색
          rect(0, height * 3 / 4, width, height / 4); // 갈색 땅
          // 나무 그리기
          drawTree(width / 4, height * 3 / 4, 100, 250);
          drawTree(width / 1.3, height * 3 / 4, 100, 250);
          pop();
        }
        
        function drawTree(x, y, trunkWidth, treeHeight) {
          push();
          noStroke();
          // 나무 줄기 그리기
          fill(139, 69, 19); // 갈색
          rect(x - trunkWidth / 2, y - treeHeight, trunkWidth, treeHeight); // 나무 줄기
        
          // 나뭇잎 그리기
          fill(255, 220, 0); // 주황색
          ellipse(x, y - treeHeight - 30, 200, 200); // 나뭇잎
        
          // 작은 나뭇잎 그리기
          fill(255, 220, 0); // 노란색
          ellipse(x + 60, y - treeHeight + 50, 130, 100); // 작은 나뭇잎
          ellipse(x - 60, y - treeHeight + 50, 130, 100); // 작은 나뭇잎
          
          ellipse(x - 60, y - treeHeight + 280, 20, 10); // 작은 나뭇잎
          ellipse(x - 70, y - treeHeight + 260, 20, 10); // 작은 나뭇잎
          ellipse(x - 30, y - treeHeight + 260, 20, 10); // 작은 나뭇잎
          ellipse(x - 100, y - treeHeight + 320, 20, 10); // 작은 나뭇잎
          ellipse(x - 10, y - treeHeight + 340, 20, 10); // 작은 나뭇잎
          ellipse(x + 20, y - treeHeight + 300, 20, 10); // 작은 나뭇잎
          ellipse(x + 50, y - treeHeight + 260, 20, 10); // 작은 나뭇잎
          ellipse(x + 70, y - treeHeight + 300, 20, 10); // 작은 나뭇잎
          ellipse(x + 100, y - treeHeight + 320, 20, 10); // 작은 나뭇잎
          pop();
          
        }
        
        function drawWinterScene() {
          // 배경 그리기
          background(224,255,255); // 밝은 회색 배경
          fill(248,248,255);
          
          push();
          noStroke();
          rect(0,height/2,width,height/2);
          pop();
          
          // 눈 그리기
          drawSnow(200, 100);
          drawSnow(400, 200);
          drawSnow(600, 300);
          drawSnow(300, 150);
          drawSnow(500, -200);
          drawSnow(200, 50);
          drawSnow(300, 100);
          drawSnow(400, 300);
          drawSnow(500, 350);
          drawSnow(600, 300);
          drawSnow(200, 350);
          drawSnow(100, 150);
          drawSnow(100, 350);
          drawSnow(50, 200);
          drawSnow(500, 100);
          drawSnow(50, 200);
          drawSnow(50, 200);
          
          // 나무 그리기
          drawPineTree(100, 300);
          drawPineTree(200, 500);
          drawPineTree(500, 400);
          
          // 눈사람 그리기
          drawSnowman(300, 200);
        }
        
        function drawSnow(x, y) {
          push();
            fill(255); // 흰색 눈
            noStroke();
            ellipse(x, y, 10, 10); // 눈 하나
            ellipse(x + 5, y + 5, 10, 10); // 눈 하나
            ellipse(x - 5, y + 5, 10, 10); // 눈 하나
          pop();
        }
        
        function drawPineTree(x, y) {
          push();
          noStroke();
          fill(139, 69, 19); // 갈색
          rect(x-35, y+20, 70, 100); // 나무 줄기
          fill(34, 139, 34); // 짙은 녹색
          ellipse(x - 40, y , 100, 100); // 나뭇잎
          ellipse(x + 40, y , 100, 100); // 나뭇잎
          ellipse(x, y -50, 100, 100); // 나뭇잎
          fill(255); // 흰색 눈
          ellipse(x-60, y+5, 25, 10); // 눈 하나
          ellipse(x-50, y+3, 25, 10); // 눈 하나
          ellipse(x-40, y, 25, 10); // 눈 하나
          ellipse(x-30, y+5, 25, 10); // 눈 하나
          
          ellipse(x+30, y, 25, 10); // 눈 하나
          ellipse(x+20, y+3, 25, 10); // 눈 하나
          ellipse(x+40, y+3, 25, 10); // 눈 하나
          ellipse(x+20, y+5, 25, 10); // 눈 하나
          
          ellipse(x+10, y-62, 25, 10); // 눈 하나
          ellipse(x-10, y-53, 25, 10); // 눈 하나
          ellipse(x+5, y-55, 25, 10); // 눈 하나
          ellipse(x, y-65, 25, 10); // 눈 하나
          pop();
        }
        
        function drawSnowman(x, y) { //눈사람 그리기
          push();
          noStroke();
          fill(139,80,40);
          rect(x+30,y+100,80,20); //팔
          rect(x-110,y+100,80,20); //팔
          fill(255); // 흰색
          ellipse(x, y+50, 100, 100); // 머리
          ellipse(x, y + 150, 150, 150); // 몸
          fill(0);
          ellipse(x-20, y+40, 20, 20); //눈
          ellipse(x+20, y+40, 20, 20); //눈
          fill(255,127,0);
          rect(x,y+50,50,20); //코
          pop();
        }
        
        function obstacleRect(x,y,c,c) { //지뢰
          // 검은색 네모 그리기
          
          fill(0);
          rect(x, y, c, c);
          fill(255,0,0);
          push();
          translate(10,10);
          ellipse(x,y,c/2,c/2);  
          pop();
        }
        function drawRat(x,y,c,c){ //먹이 그리기
          // 쥐 그리기
          
          push();
          noStroke();
          fill(127,127,127);
          translate(17,3);
          ellipse(x,y,c,c) //회색 귀
          pop();
          
          push();
          noStroke();
          fill(127,127,127);
          translate(3,3);
          ellipse(x,y,c,c) //회색 귀
          pop();
          
          push();
          noStroke();
          fill(255,20,147);
          translate(17,3);
          ellipse(x,y,c/2,c/2) //분홍 귀
          pop();
          
          push();
          noStroke();
          fill(255,20,147);
          translate(3,3);
          ellipse(x,y,c/2,c/2) //분홍 귀
          pop();
          
          push();
          noStroke();
          translate(10,10);
          fill(127, 127, 127); // 회색 머리
          ellipse(x, y, c, c);
          pop();
          
          push();
          noStroke();
          translate(5,8);
          fill(0, 0, 0); // 눈
          ellipse(x, y, c/4, c/4);
          pop();
          
          push();
          noStroke();
          translate(15,8);
          fill(0, 0, 0); // 눈
          ellipse(x, y, c/4, c/4);
          pop();
          
          push();
          noStroke();
          translate(10,13);
          fill(0, 0, 0); // 코
          ellipse(x, y, c/5, c/5);
          pop();
          
          
        }
        
        function drawBallon(x,y,c,c,r,g,b){ //풍선 그리기 
          
          push();
          noStroke();
          fill(0,0,0);
          translate(-7,0);
          rect(x,y,c/7,c*1.3); //손잡이
          pop();
          
          
          push();
          noStroke();
          fill(r,g,b);
          ellipse(x,y,c,c); //풍선 머리
          pop();
          
          push();
          noStroke();
          fill(r,g,b);
          translate(11,40);
          ellipse(x,y,c/4,c/5);
          pop();
          
          push();
          noStroke();
          fill(r,g,b);
          translate(-11,40);
          ellipse(x,y,c/4,c/5);
          pop();
          
        }
        
        function mouseClicked() {
          snakeColor = picker.color();
        }
