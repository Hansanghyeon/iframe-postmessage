## 문제정의

A사이트, B사이트가 있습니다.

A사이트에 B사이트를 iframe을 inline으로 불러왔습니다.

A사이트에서 B사이트 iframe으로 setInterval로 postmessage를 전송합니다.

B사이트는 postmessage를 받을 준비를하는 js코드를 가지고있는데. A사이트는 B사이트에 이런 이벤트가 등록되어있는지 모르는채로 응답 postmessage가 올때까지 계속 postmessage를 전송합니다.

B사이트는 OAuth2.0 인증을 위해서 인증하는 도메인으로 이동했다 돌아옵니다. OAuth2.0 인증 토큰을 부모 frame으로 postmessage를 보내서 부모 frame에서 인증정보를 가지고있게 하려합니다.

A사이트는 인증정보를 받고 쿠키에 해당 정보를 저장한다음 B사이트 iframe으로 토큰정보를 보냅니다.

**이때 B사이트의 postmessage 받는 이벤트가 동작하지 않고있습니다.**

## 테스트

그래서 페이지 이동이있어도 프레임간의 postmessage 이벤트가 잘받아지나 확인하기위한 데모를 작성합니다.

테스트를 간단하게 하기위해서 `vscode - Live Server` 익스텐션을 사용합니다.
