# 인프런 - Apple Clone Coding

[SASS]를 이용한 Apple Clone Coding

## 미리보기

https://sjkjh2.github.io/inf-apple-clone/


## 사용스택

```bash
$ npm list
inf-apple-clone@ D:\study\inf-apple-clone
├── autoprefixer@10.4.20
├── concurrently@9.1.2
├── postcss-cli@11.0.0
├── postcss@8.5.3
└── sass@1.85.1
```

## package.json

```json
{
  "scripts": {
    "sass": "sass scss:css --watch",
    "prefix": "postcss css/*.css --use autoprefixer --dir css --watch",
    "dev": "concurrently \"npm run sass\" \"npm run prefix\"",
    "build": "sass scss:build --style=compressed --no-source-map && postcss css/*.css --use autoprefixer -d css"
  },
  "devDependencies": {
    "autoprefixer": "^10.4.17",
    "concurrently": "^9.1.2",
    "postcss": "^8.4.35",
    "postcss-cli": "^11.0.0",
    "sass": "^1.85.0"
  },
  "browserslist": [
    "last 2 versions",
    "> 1%",
    "ie >= 11"
  ]
}
```

## postcss.config.js

```js
module.exports = {
  plugins: {
    autoprefixer: {}
  }
} 
```

## 설치및 실행

```bash
npm install
npm run dev
```