## 다이내믹셀 좌우모터의 속도명령값을 키보드로 각각 입력 받아 구동하는 프로젝트

start, end1, time1 : 반복문 내부 코드의 실행시간을 측정, 출력

leftspeed, rightspeed : 각 바퀴 속도 입력

### 실행결과

![image](https://github.com/user-attachments/assets/48901f70-06b4-4e58-8769-1188877848b1)

---

#### Ctrl+c를 누르면 바로 종료하지 않고 명령을 한번 더 입력하면 종료하는데 이유를 설명하라. 이걸 해결하려면 어떻게 해야 하는지 나중에 생각해볼 것

Ctrl+c가 눌릴때 ctrlc() 함수 호출, ctrl_c_pressed를 true로 설정함. 하지만 값이 루프의 조건문에 반영되려면 루프가 한 번 더 돌아야 반영이 됨.

#### 입력한 속도 명령값이 현재 모터 속도와 차이가 클 때 급가속 또는 급감속이 발생하여 진동과 소음이 발생한다. 이를 해결하는 방법을 설명하라.

명령한 속도값에 최대값, 최소값을 설정하여 급격한 속도변화를 제어
