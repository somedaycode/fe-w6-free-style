# fe-w6-free-style

## DOM 탐색 메소드 구현

querySelector와 유사하게 동작하는 커스텀 API를 만든다.

- [x] DFS, BFS 알고리즘을 선택하여 구현

## Study Planner

목적: 자신이 공부한 시간을 측정하고 하루의 목표를 간단히 메모하여 체크할 수 있는 앱을 만든다.

### 기능 목록

- [x] 공부 시간을 측정할 수 있다.
  - 타이머, 혹은 뽀모도로 (선택기능)
- [x] 오늘 날짜를 보여준다.
- [x] 날씨를 보여준다
  - 현재 날씨
  - 슬라이더를 통한 이후의 날씨(추가)
- [ ] 히스토리 기능을 통해 공부한 장소를 지도로 보여준다
- [ ] socket.io를 통한 실시간 기능 구현
  - 온라인 확인
  - 다른 사람의 공부시간 확인

### 구현 사항

#### 날씨

1. 클라이언트에서 위도와 경도 값을 얻어낸 후, 서버에 보낸다.
   (CORS로 인해 브라우저에서 fetch요청이 불가하다.)

2. 서버는 위도와 경도를 기상청이 요구하는 X, Y grid 좌표값으로 변환하여 request를 날린다.

3. 기상청으로부터 데이터를 JSON 형태로 저장한다.

4. 클라이언트는 저장한 데이터를 가져온다.

5. 저장한 데이터를 정제하여 하늘상태, 온도, 강수량을 얻는다. 이후, 화면에 출력한다.

6. 또, 가진 데이터에 따라 다른 이미지를 출력해준다.

7. 지도 API를 이용하여 현재 행정구역을 표시해준다.

#### 타이머

1. start를 누르면 타이머 실행. start 버튼은 pause로 바뀐다.
2. disable이 default값인 reset버튼 활성화
3. pause시 타이머 일시정지 pause는 restart로 바뀐다.

#### 메모

1. 오늘 하루 할 일을 적는 곳.
2. --

----

#### 느낀 점

이 글을 쓰는 현재 날짜는 `2021-06-20`

스터디플래너 본연의 기능에 더 집중해서 개발을 했다면 완성도 있는 프로젝트가 됐을거라 생각한다.

날씨도 보여주고 싶었고, 지도 API도 사용해보고 싶었다. (처음으로 진행하는 개인 프로젝트라 욕심이 많았다.)

생각해보면 날씨는 그렇게 중요한게 아니였는데... 기상청 API의 쓴맛을 보았다.

지금 다시 이 프로젝트를 진행한다면 고등학교 수험생들을 생각하며 본연의 목적을 가진 스터디플래너를 만들지 않을까?
