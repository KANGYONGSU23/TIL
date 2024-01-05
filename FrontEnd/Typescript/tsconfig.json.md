# tsconfig.json

https://www.typescriptlang.org/tsconfig

https://codingapple.com/unit/typescript-tsconfig-json/

## compilerOptions

**target**

타입스크립트 파일을 어떤 버전의 자바스크립트 파일로 변환 할 건지 정하는 것.

es5로 셋팅해놓으면 es5버전의 자바스크립트로 컴파일 해준다.

**module**   
자바스크립트 모듈간 import 문법을 구현한 떄 어떤 문법을 쓸 건지 정하는 것.   
`commonjs`는 `require` 문법   
`ex2015`, `esnext`는 `import`문법을 사용한다.   
`node16`, `nodenext`는 `import`와 `require`문법을 모두 지원한다. (단 node v12 부터)

**noImplicitAny**   
`any`타입이 의도치 않게 발생하는 경우 에러를 띄워주는 설정.

**strictNullChecks**   
`null`과 `undefined`는 각각 고유한 유형으로 간주되어 구체적인 값이 예상되는 위치에서 사용하려고 하면 타입 오류가 발생합니다.

**allowJs**   
`js` 파일들 `ts`에서 `import`해서 쓸 수 있는지

**checkJs**   
일반 `js` 파일에서도 에러체크 여부

**jsx**   
`tsx` 파일을 `jsx`로 어떻게 컴파일할 것인지 
'preserve', 'react-native', 'react'

**declaration**   
컴파일시 `.d.ts` 파일도 자동으로 함께생성 (현재쓰는 모든 타입이 정의된 파일)

**outFile**   
모든 `ts`파일을 `js`파일 하나로 컴파일해줌 (module이 none, amd, system일 때만 가능)

**outDir**   
`js`파일 아웃풋 경로바꾸기

**rootDir**    
루트경로 바꾸기 (js 파일 아웃풋 경로에 영향줌)

**removeComments**   
컴파일시 주석제거

**noImplicitAny**   
`any`타입 금지 여부

**strictFunctionTypes**   
함수파라미터 타입체크 강하게

**strictPropertyInitialization**   
`class constructor` 작성시 타입체크 강하게

**noImplicitThis**   
`this` 키워드가 `any` 타입일 경우 에러내기

**alwaysStrict**   
자바스크립트 `"use strict"` 모드 켜기

**noUnusedLocals**   
쓰지않는 지역변수 있으면 에러내기

**noUnusedParameters**   
쓰지않는 파라미터 있으면 에러내기

**noImplicitReturns**    
함수에서 `return` 빼먹으면 에러내기

**noFallthroughCasesInSwitch**   
`switch`문 이상하면 에러내기