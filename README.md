[제작기간] : 2021.1.27. ~ 2021.2.13

[제작인원] : 3명 (BE : 1, FE: 2)

[서비스기간] : 2021.02.20 ~ (계속서비스중)

[역할] : FE
외주를 맡아 진행했습니다. 클라이언트가 원하는 디자인에 맞게 **커뮤니티 게시판**과 **메모 탭**을 만들었습니다. 현재 약 600명의 인원이 사용하고있는 서비스입니다. 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/004d906e-3885-4b42-b9f2-f1f1100af893/Untitled.png)

[깃허브 링크] 
[기술스택]

```jsx
{
		"platform" : [ios, android]
    "language": [ javascript ] ,
    "framework": [ nodejs, react,react-native, apollo, graphql, expo]
}
```

구글 스프래드시트와 github로 팀원과 협업했습니다.

### 게시판 이슈사항

everytime 어플의 게시판처럼 만드는게 목표였습니다.

- react-navigation으로 글,게시판,검색 등의 화면 이동
- 게시판 설계: 
게시판을 아래로 내리면 uselazyQuery로 서버에서 글을 불러와 렌더링하게함. 모든 글은 datalist 객체에 저장 FlatList로 페인팅. React.memo로 렌더링을 최소화.
- 내가 글을 삭제할 경우, 내가 보는 화면에서 해당 글이 없어져야 하는 이슈 : 
datalist 객체에서 해당 글을 삭제하고 삭제 글 아래에 위치한 글들을 다시 렌더링.

### apk 파일 빌드

- expo가 제공하는 cmd 명령어를 이용해 apk파일을 빌드했습니다.
- 클라이언트의 요구에 디자인을 수정하고 apk파일을 만드는 과정을 반복했습니다. CI/CD 환경을 경험했습니다.

### ios 이슈

- android와 ios마다 디자인을 다르게 해야 했었음. (keyboadAvoidingView 이슈 등등)
- android는 시뮬레이션이 간단했으나 ios는 mac 등 애플 관련 기기가 없어 시뮬레이션이 어려웠음.
- 결국 widoow 로컬 컴퓨터에서 가상머신으로 mac을 실행하고, ios 시뮬레이터 xcode를 이용해 해결.

[아쉬운점]

2주라는 짧은 기간안에 집중적으로 개발한 첫 대규모 프로젝트였습니다. 코드가 지저분 하고 , react기반 이어서 앱의 크기가 크고, low level로 접근해 구현을 못한점  등 아쉬운이  남는 프로젝트였습니다.
