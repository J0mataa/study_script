# study_script
use: minecraft 1.12.2 / papper bukkit 1.12.2 / notepade++
---
스크립트 공부용입니다.
2023-02-02


</br>
</br>

---

### 1. 서버열기

1. 앞으로 다운로드 받을 파일을 모아놓을 <b>빈폴더(server)</b> 를 생성한다.
2. <b>페이퍼 버킷(paper-1.12.2-1618.jar)</b> 을 다운로드 받아 server에 넣는다.
3. start.txt 파일을 생성
> <b>3. 내용(start.txt): </b> </br>
> java -Xms512M -Xmx1024M -jar paper-1.12.2-1618.jar
</br>PAUSE

> Xms = 최소메모리 / Xmx = 최대메모리
> ※ 본인은 512mb, 최대 1024mb 사용임. (이 부분은 개인 메모리RAM 상태 보고 수정해야함.)

4. start.txt --> start.bat 으로 파일확장자 수정
5. start.bat 실행시키기
6. [멈춤발생!] --> ㄱㅊ elua.txt, logs, cache등의 파일 만들어짐.
7. elua.txt
> <b>7. 내용(elua.txt): </b> </br>
> elua = false ---> elua = true 로 수정
8. start.bat 재실행
9. Done ~~~ 뜨면 완료
#### localhost 혹은 127.0.0.1을 minecraft주소에 입력 후 입장!
</br>
</br>
참고주소: https://nalag.tistory.com/9


</br>
</br>


---

### 2. 스크립트&애드온 다운로드


참고영상(1편참고): https://www.youtube.com/watch?v=JIvuq09JpMY&list=PL7GExJh5AB9-oO6pMDiqp8_NdFNbpHM1y

다운로드 링크: https://docs.skunity.com/downloads


</br>
</br>


---
### 3. 스크립트 공부

폴더 위치: server\plugins\Skript\scripts </br>
server(본인이 생성한 폴더) > plugins > Skript > scripts </br>
scripts에서 .sk 파일들 만들기~ </br>

---


<b> ❗❗ 자신에게 서버 오피를 줘야함 ❗❗ </b> 
1. start.bat 실행시 나오는 cmd창
> <b>1. 내용(start.bat 실행cmd): </b> </br>
> op M4T4a
> </br></br>
> ※ M4T4a는 본인의 마크 닉네임

참고주소: https://www.youtube.com/watch?v=JIvuq09JpMY&list=PL7GExJh5AB9-oO6pMDiqp8_NdFNbpHM1y

---

#### 수정 시 reload하기
> <b>minecraft 게임 내에서 </b> </br>
> /sk reload 파일명 </br>
> .sk의 확장자는 생략 </br>


---


### 커맨드 스크립트

``` 
command /명령어:
	trigger:
		if player is op:
			message "안녕하세요 반갑습니다. 오피가 있다면 실행됩니다."
		else:
			message "오피가 없어 인사를 띄울 수 없습니다."
```
```
if player is op: //만약 플레이어가 op가 있다면?
  message 실행1
else:
  message 실행2
```

---

### 이벤트 스크립트

```
on chat:
	cancel event
	message "%player%님은 채팅을 칠 수 없습니다. (채팅취소이벤트)"
```

```
채팅을 치면:
  해당 이벤트를 취소(채팅취소)
  message 실행1
```
