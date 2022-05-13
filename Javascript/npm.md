# NPM(Node Packaged Manager)
npm은 **Node.js로 만들어진 패키지(모듈)을 관리해주는 툴**이다. Node.js에서 사용할 수 있는 모듈들을 패키지화에서 모아둔 저장소 역할이며 설치, 관리를 수행할 수 있는 CLI를 제공한다. npm에 업로드된 노드 모듈을 패키지라고 부른다. 모듈이 다른 모듈을 사용할 수 있는 것처럼, 패키지도 다른 패키지를 사용할 수 있다. 이러한 관계를 의존 관계라고 한다. npm은 package.json 파일로 프로젝트의 정보와 패키지들의 의존성을 관리한다.

<br/>

## npm 모듈 설치
```cmd
npm i <패키지명>
```

<br/>

## package.json
- 사용하고 있는 패키지들의 명세가 작성되어 있다.
- package.json을 공유해 개발 환경을 빠르게 구축할 수있다.
- Maven의 pom.xml 역할과 비슷하다.

```json
{
	"name" : "test",
	"description" : "javascript's test programming.",
	"keywords" : ["util", "f", "server", "client", "browser"],
	"author" : "Goorm",
	"contributors" : [],
	"dependencies" : [],
	"repository" : {"type": "git", "url" : "git://gitbub.com/documentcloud/test.git" },
	"main" : "test.js",
	"version" : "1.1.6"
}
```

<br/>

## 장점👍
- **관리 용이** : package.json안에서 dependencies 한곳에 다 뭉치게 되어 라이브러리 관리가 편하다.
- **설치 용이** : npm install로 node_modules에 잘 정돈되어 라이브러리가 빠르게 설치된다.

<br/>

## yarn
npm의 일관성, 보안, 빌드시 성능 등에 문제를 해결하기 위해 Facebook이 yarn을 개발하였다. yarn의 릴리즈 초기에는 yarn의 성능이 뛰어났지만 현재는 성능부분의 차이는 거의 없다고 봐도 무방하다.


<br/>

## 참고
> https://ooeunz.tistory.com/19  
> https://dkwjdi.tistory.com/187
