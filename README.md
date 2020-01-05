# WeatherApp

React Native Weather App

## expo

    npm install -g expo-cli

expo 설치

expo는 create-react-app과 같은 것이다.

react native를 수동으로 작업하고 싶다면 react native cli 를 설치

react native cli 는 native file들을 더 많이 컨트롤 하고 싶을 때를 위함.

expo는 모든 native file을 숨기고 관리해준다.

expo의 가장 큰 장점은 휴대폰에서 앱을 테스트 할 수 있다.

단점은 native file을 크게 제어할 수 없다.

expo는 수동적인 작업들이 덜 필요하고, 시작하는데 훨씬 더 빠른 방식.

## Creating the project

    expo init "projectname"

원하는 폴더로 가서 위 명령어를 입력.

blank 선택.

project name 설정.

    npm start

프로젝트 실행.

    I m using node version v.12.13
    and I met a bugs...
    error invaild regular expression.......
    and I found a solution without downgrading node
    https://github.com/expo/expo-cli/issues/1074

    \node_modules\metro-config\src\defaults\blacklist.js

    var sharedBlacklist = [
    /node_modules[/\\]react[/\\]dist[/\\].*/,
    /website\/node_modules\/.*/,
    /heapCapture\/bundle\.js/,
    /.*\/__tests__\/.*/
    ];
    change to:

    var sharedBlacklist = [
    /node_modules[\/\\]react[\/\\]dist[\/\\].*/,
    /website\/node_modules\/.*/,
    /heapCapture\/bundle\.js/,
    /.*\/__tests__\/.*/
    ];

npm start를 했을때 node version이 높아 발생하는 에러가 발생 할 때 위 경로의 blacklist.js 부분을 변경.

    expo login

아이폰에 테스트를 위해 expo login
