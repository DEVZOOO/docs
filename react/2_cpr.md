# CRP(create-react-project)
react 프로젝트를 생성하고, 필요한 모듈들을 설치하여 개발할 수 있는 환경을 만들어준다.   
`npx create-react-app [app-name]`
>cf) 나는 `typescript`를 사용하므로 관련 옵션을 추가하여 실행했다.   
>`npx create-react-app [app-name] --template typescript`

## 생성된 기본 프로젝트 구조
|   |   |
|---|:---:|
|app-name|  |
|&nbsp;&nbsp;&nbsp;├ README.md|(1)|
|&nbsp;&nbsp;&nbsp;├ node_modules|(2)|
|&nbsp;&nbsp;&nbsp;├ package.json|(3)|
|&nbsp;&nbsp;&nbsp;├ package-lock.json|(4)|
|&nbsp;&nbsp;&nbsp;├ .gitignore|(5)|
|&nbsp;&nbsp;&nbsp;├ public|(6)|
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├ favocon.ico|(7)|
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├ index.html|(8)|
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└ manifest.json|(9)|
|&nbsp;&nbsp;&nbsp;├ src|(10)|
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├ App.css
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├ App.js
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├ index.css
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├ index.js
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├ logo.svg
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└ serviceWorker.js

1. src   
    app의 모든 소스
2. index.html
    SPA(Single Page Application)의 특성에 따라 각 코드들을 이 html에 그린다.