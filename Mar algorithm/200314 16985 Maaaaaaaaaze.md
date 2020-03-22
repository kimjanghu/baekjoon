## # 16985. Maaaaaaaaaze

평화롭게 문제를 경작하며 생활하는 BOJ 마을 사람들은 더 이상 2차원 미로에 흥미를 느끼지 않는다. 2차원 미로는 너무나 쉽게 탈출이 가능하기 때문이다. 미로를 이 세상 그 누구보다 사랑하는 준현이는 이런 상황을 매우 안타깝게 여겨 아주 큰 상금을 걸고 BOJ 마을 사람들의 관심을 확 끌 수 있는 3차원 미로 탈출 대회를 개최하기로 했다.

대회의 규칙은 아래와 같다.

- 5×5 크기의 판이 5개 주어진다. 이중 일부 칸은 참가자가 들어갈 수 있고 일부 칸은 참가자가 들어갈 수 없다. 그림에서 하얀 칸은 참가자가 들어갈 수 있는 칸을, 검은 칸은 참가자가 들어갈 수 없는 칸을 의미한다.
- 참가자는 주어진 판들을 시계 방향, 혹은 반시계 방향으로 자유롭게 회전할 수 있다. 그러나 판을 뒤집을 수는 없다.
- 회전을 완료한 후 참가자는 판 5개를 쌓는다. 판을 쌓는 순서는 참가자가 자유롭게 정할 수 있다. 이렇게 판 5개를 쌓아 만들어진 5×5×5 크기의 큐브가 바로 참가자를 위한 미로이다. 이 때 큐브의 입구는 정육면체에서 참가자가 임의로 선택한 꼭짓점에 위치한 칸이고 출구는 입구와 면을 공유하지 않는 꼭짓점에 위치한 칸이다.
- 참가자는 현재 위치한 칸에서 면으로 인접한 칸이 참가자가 들어갈 수 있는 칸인 경우 그 칸으로 이동할 수 있다.
- 참가자 중에서 본인이 설계한 미로를 가장 적은 이동 횟수로 탈출한 사람이 우승한다. 만약 미로의 입구 혹은 출구가 막혀있거나, 입구에서 출구에 도달할 수 있는 방법이 존재하지 않을 경우에는 탈출이 불가능한 것으로 간주한다.

이 대회에서 우승하기 위해서는 미로를 잘 빠져나올 수 있기 위한 담력 증진과 체력 훈련, 그리고 적절한 운이 제일 중요하지만, 가장 적은 이동 횟수로 출구에 도달할 수 있게끔 미로를 만드는 능력 또한 없어서는 안 된다. 주어진 판에서 가장 적은 이동 횟수로 출구에 도달할 수 있게끔 미로를 만들었을 때 몇 번 이동을 해야하는지 구해보자. 

## 입력

첫째 줄부터 25줄에 걸쳐 판이 주어진다. 각 판은 5줄에 걸쳐 주어지며 각 줄에는 5개의 숫자가 빈칸을 사이에 두고 주어진다. 0은 참가자가 들어갈 수 없는 칸, 1은 참가자가 들어갈 수 있는 칸을 의미한다.

## 출력

첫째 줄에 주어진 판으로 설계된 미로를 탈출하는 가장 적은 이동 횟수를 출력한다. 단, 어떻게 설계하더라도 탈출이 불가능할 경우에는 -1을 출력한다.

## 예제 입력 1 복사

```
1 1 1 1 1
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
1 1 1 1 1
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
1 1 1 1 1
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
1 1 1 1 1
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
1 1 1 1 1
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
```

## 예제 출력 1 복사

```
12
```

## 예제 입력 2 복사

```
1 1 1 1 1
1 0 0 0 1
1 0 0 0 1
1 0 0 0 1
1 1 1 1 1
0 0 0 0 0
0 1 1 1 0
0 1 0 1 0
0 1 1 1 0
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
0 0 1 0 0
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
0 1 1 1 0
0 1 0 1 0
0 1 1 1 0
0 0 0 0 0
1 1 1 1 1
1 0 0 0 1
1 0 0 0 1
1 0 0 0 1
1 1 1 1 1
```

## 예제 출력 2 복사

```
-1
```

## 예제 입력 3 복사

```
1 1 1 1 1
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
1 1 1 1 1
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
1 1 1 1 1
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
1 1 1 1 1
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
0 0 0 0 0
1 1 1 1 1
```

## 예제 출력 3 복사

```
12
```

## 예제 입력 4 복사

```
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
```

## 예제 출력 4 복사

```
12
```

## 예제 입력 5 복사

```
0 0 0 1 0
0 0 0 0 0
1 0 1 1 1
0 0 0 1 0
0 0 1 0 0
0 1 0 0 0
1 1 0 0 0
1 0 0 1 0
0 1 1 1 0
0 1 0 1 0
0 0 1 0 0
1 0 0 0 0
0 1 0 0 0
0 0 1 0 0
1 1 1 0 0
1 0 0 0 1
1 0 0 0 0
0 0 1 0 1
0 1 1 0 0
0 1 0 0 0
0 0 0 1 0
1 0 0 0 0
0 0 1 0 0
0 1 0 0 1
0 1 0 0 0
```

## 예제 출력 5 복사

```
22
```

## 예제 입력 6 복사

```
0 0 0 0 0
0 0 0 0 0
1 0 0 0 1
0 0 1 0 0
0 0 1 1 1
0 1 0 0 1
0 0 0 0 1
0 0 0 0 0
0 0 0 0 0
0 1 0 0 0
0 1 0 0 1
1 0 0 1 0
0 0 0 1 0
0 1 1 0 0
0 1 0 0 0
1 0 1 0 0
0 0 0 0 0
1 0 0 0 0
0 0 0 1 0
1 0 0 0 0
0 0 0 1 0
0 0 0 0 1
1 1 0 0 0
1 0 0 1 1
1 0 0 0 0
```

## 예제 출력 6 복사

```
-1
```

## 예제 입력 7 복사

```
1 1 0 0 0
0 0 0 0 1
0 0 1 0 0
0 0 0 0 0
0 0 0 0 0
0 0 1 1 1
1 0 0 0 0
0 0 1 0 0
0 0 1 1 1
0 0 1 0 0
0 0 0 0 0
0 0 1 0 1
0 0 0 0 0
0 0 0 1 0
0 0 1 0 1
0 0 1 0 0
1 0 0 0 0
0 0 1 1 0
1 0 1 0 0
0 0 1 0 1
0 0 1 1 0
1 1 0 1 1
0 0 0 0 1
0 1 0 1 0
0 1 0 0 0
```

## 예제 출력 7 복사

```
16
```

## 예제 입력 8 복사

```
0 0 1 0 0
0 0 0 0 0
1 1 0 0 0
0 0 1 0 0
1 1 1 0 0
0 0 0 0 1
1 0 0 0 0
0 1 0 0 1
0 0 0 0 0
0 1 0 1 0
1 0 0 0 1
1 1 1 1 1
1 1 0 0 0
0 0 0 1 0
0 0 0 1 0
0 0 0 1 1
0 0 1 0 0
0 1 1 1 0
1 0 0 0 0
0 1 1 0 1
0 1 0 0 0
0 0 0 1 0
1 0 0 0 0
0 0 0 1 0
0 0 0 1 0
```

## 예제 출력 8 복사

```
18
```

## 출처

- 문제를 만든 사람: [BaaaaaaaaaaarkingDog](https://www.acmicpc.net/user/BaaaaaaaaaaarkingDog)

## Code

```python
import sys
from collections import deque
def bfs():
    global N, minV, tmp
    dx = [0, 1, 0, -1, 0, 0]
    dy = [1, 0, -1, 0, 0, 0]
    dz = [0, 0, 0, 0, 1, -1]
    visited = [[[0] * N for _ in range(N)] for _ in range(N)]
    q = deque()
    q.append((0, 0, 0, 0))
    visited[0][0][0] = 1
    while q:
        x, y, z, cnt = q.popleft() # 각 축과 이동횟수를 기록
        if (x, y, z) == (4, 4, 4):
            if minV > cnt:
                minV = cnt
        for k in range(6):
            nx = x + dx[k]
            ny = y + dy[k]
            nz = z + dz[k]
            if 0 <= nx < N and 0 <= ny < N and 0 <= nz < N and tmp[nx][ny][nz] == 1 and not visited[nx][ny][nz]:
                visited[nx][ny][nz] = 1
                q.append((nx, ny, nz, cnt+1))

def rotate(k, tmp): # 판 돌리는 함수
    global N
    rtmp = [[0] * N for _ in range(N)]
    for i in range(N):
        for j in range(N):
            rtmp[j][N-1-i] = tmp[k][i][j]
    tmp[k] = rtmp

def game():
    global tmp, minV
    for one in range(4): # 5중 for문을 이용해 각 판을 돌리고 bfs 실행
        if one:
            rotate(0, tmp)
        if tmp[0][0][0]: # 만약 출발점이 1이라면 다음 판으로 이동
            for two in range(4):
                if two: # 첫번째 경우의 경우 돌리지 않는다.
                    rotate(1, tmp)
                for three in range(4):
                    if three:
                        rotate(2, tmp)
                    for four in range(4):
                        if four:
                            rotate(3, tmp)
                        for five in range(5):
                            if five:
                                rotate(4, tmp)
                            bfs()
                            if minV == 12:
                                return

def ordered(n, k):
    global used, order, maze, tmp
    if n == k:
        for i in range(k):
            tmp[order[i]] = maze[i] # 판 순서 복사
        game()
        return
    else:
        for i in range(k): # 판 순서 리스트 순열
            if not used[i]:
                used[i] = 1
                order[n] = i
                ordered(n+1, k)
                used[i] = 0
            elif minV == 12:
                return

N = 5
maze = [[list(map(int, sys.stdin.readline().split())) for _ in range(N)] for _ in range(N)]
tmp = [[[0] * N for _ in range(N)] for _ in range(N)] # 판의 순서에 따른 저장을 하기 위한 리스트
order = [0] * N
used = [0] * N
minV = 10**9
ordered(0, 5)
if minV == 10**9: # minV가 변하지 않으면 -1
    minV = -1
print(minV)
```
