# DFS와 BFS
- DFS와 BFS는 자료탐색 기법으로 그래프를 탐색할때 사용한다.

## DFS
    - DFS는 우리말로 '깊이 우선탐색'으로 한방향으로 갈수있는데 까지 끝까지 탐색한 뒤, 
      다른 방향으로 가는 탐색 방법이다.
    - DFS는 LIFO(Last in First Out)구조인 스택과 중복을 체크하기위한 set을 이용한다.
    - 다음과 같은 사진을 통해 DFS의 탐색을 간단히 알아볼 수 있다.
![Depth-First-Search](https://user-images.githubusercontent.com/86968048/212478897-ba3b7628-ea53-4287-b572-cebe611ba9af.gif)

    - 제가 이해한 바를 영상을 통해 설명하겠습니다. 어.. 자막을 달다가 너무 힘들어서 그냥올려요.. 그 월요일날 설명하겠습니다!
    (이해가 안갈시 아래 유튜브를 참고해주세요!!)
https://user-images.githubusercontent.com/86968048/212479686-6f17f417-44d6-4159-a56f-9911dabafe5e.mp4

- - -
## BFS
    - BFS는 우리말로 '너비 우선 탐색'으로 시작점인 루트 노드와 
      같은 거리에 있는 노드를 우선으로 방문하는 방법이다.
    - BFS는 FIFO(First in First Out)구조인 큐와 중복을 체크하기위한 set을 이용한다.
    - 다음과 같은 사진을 통해 BFS의 탐색을 간단히 알아볼 수 있다
![Breadth-First-Search-Algorithm](https://user-images.githubusercontent.com/86968048/212479196-4f704308-6448-49ea-b68f-707ee8ef7dea.gif)

     - 제가 이해한 바를 영상을 통해 설명하겠습니다. 어.. 자막을 달다가 너무 힘들어서 그냥올려요.. 그 월요일날 설명하겠습니다!
    (이해가 안갈시 아래 유튜브를 참고해주세요!!)

https://user-images.githubusercontent.com/86968048/212479905-030b1a03-0465-406d-8063-e2f029411f4f.mp4

- - -

## 간단한 자료구조 설명
### 스택(Stack)
    - 스택(stack)이란 자료를 쌓은 형태 
    - 가장 늦게 들어온 데이터가 가장 먼저 밖으로 나가는 형태를 가지는 자료구조이다.(LIFO)
    - 즉, 스택 안에서 가장 위(TOP)에 위치해야만 밖으로 나갈 수 있다.

### 셋트(Set)
    - set이란 순서가 없고, 중복을 허용하지않는 자료구조이다.
    - 순서가 없다라는 말은 데이터들이 순서대로 삽입되어도, 
      set에서는 특정한 순서가 없다는 것을 말한다.
    - 중복을 허용하지 않는다는 말은 같은 데이터가 삽입되면, 마지막에 삽입된 데이터만이 저장된다.

### 큐(Queue)
    - 큐(Queue)란 순서가 있고, 중복또한 허용하는 자료구조이다.
    - 한쪽 끝에서만 삽입이 이뤄지고, 다른 한쪽 끝에서는 데이터를 내보내는 연산만 이뤄진다.(FIFO)
    - 실생활의 티켓부스에 서있는 사람들, 톨게이트에 들어가는 자동차들을 생각하면된다.
    - 큐는 원형큐, 우선순위 큐 등 다양한 종류가 있지만, 여기서는 기본적인 큐만을 설명한다.

- - -

## 참고자료
    - [유튜브, BFS와 DFS 개념적 설명] ]
      https://www.youtube.com/watch?v=gl5RhtU2mF8
    - [파이썬을 통한 BFS와 DFS 구현]  
      https://cyc1am3n.github.io/2019/04/26/bfs_dfs_with_python.html
    - [자료구조 Stack]
      https://jud00.tistory.com/entry/%EC%9E%90%EB%A3%8C%EA%B5%AC%EC%A1%B0-%EC%8A%A4%ED%83%9DStack%EA%B3%BC-%ED%81%90Queue%EC%97%90-%EB%8C%80%ED%95%B4%EC%84%9C-%EC%95%8C%EC%95%84%EB%B3%B4%EC%9E%90#:~:text=%F0%9F%93%8C%20%EC%8A%A4%ED%83%9D(Stack)%EC%9D%B4%EB%9E%80%20%EB%AC%B4%EC%97%87%EC%9D%BC%EA%B9%8C,%EB%90%98%EB%8A%94%20%EA%B5%AC%EC%A1%B0%EB%A5%BC%20%EA%B0%80%EC%A7%80%EA%B3%A0%20%EC%9E%88%EC%8A%B5%EB%8B%88%EB%8B%A4
    - [자료구조 Set]
      https://velog.io/@taeha7b/datastructure-set
    - [자료구조 Queue]
      https://donggu1105.tistory.com/163
