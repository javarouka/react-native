# 읽어야 한다
- 설치 : https://facebook.github.io/react-native/docs/getting-started.html
- 디버깅 : https://facebook.github.io/react-native/docs/debugging.html
- 윈도우 설정 : http://kwon-9981.tistory.com/15 ()

# window 설치 시 주의할점
유독 window 에서의 설치가 문서가 명확하지 않아 고생했다

## 환경변수 설정
Android Studio 설치 시 기본적으로 sdk 경로는
```
{userHomeDir}\AppData\Local\Android\sdk
```
이다

이 기준으로 환경변수
- ANDROID_HOME : {userHomeDir}\AppData\Local\Android\sdk
- Path : {기존path}%ANDROID_HOME%\platform-tools;%ANDROID_HOME%\emulator

설정이 필요하다.

새 터미널을 띄우고  타이핑했을때 
```
$ adb
$ emulator
```
가 정상동작하면 OK.
