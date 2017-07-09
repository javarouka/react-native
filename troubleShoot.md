# 읽어야 한다
## Official
- 설치 : https://facebook.github.io/react-native/docs/getting-started.html
- 디버깅 : https://facebook.github.io/react-native/docs/debugging.html

## Blog
- 윈도우 설정 : http://kwon-9981.tistory.com/15 (한글)

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

## Android Device Emulator 생성
React Native 를 개발하기 위해서는 먼저 안드로이드 가상환경을 만들어야 한다

adb 를 사용해서 커맨드라인으로 만들수도 있지만,
문서 https://developer.android.com/studio/run/managing-avds.html?hl=ko 를 보고 만드는게 편하다

기기를 만들때 이름을 명확하게 짓자. 커맨드라인실행시 필요하다
![디바이스 이름](https://developer.android.com/images/tools/avd-verifyconfig.png?hl=ko)

안드로이드 스튜디오에서는 만든 디바이스를 바로 실행해주는 GUI 가 있어서, 그 UI 의 녹색단추를 클릭하면 바로 실행된다.

하지만, 커맨드라인으로 실행할수도 있다.

### 커맨드라인 실행법

만들어진 Device 확인은 다음 명령으로 할 수 있다
```
$ emulator -list-avds
Nexus.6.A26
Nexus_5X_API_26
Nexus_5_API_26
```

1. 에뮬레이터를 구동한다
```
// @{device이름}
emulator @Nexus.6.A26
```
2. 생성한 React Native 디렉토리에서 다음을 수행한다
```
react-native run-android
```
3. 즐겁게 개발한다
