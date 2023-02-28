# env에서 undefined 타입 제거하기

<img src="https://user-images.githubusercontent.com/82315118/221933790-f5729204-8ede-45c8-8452-ff935e712fb2.png" />

&nbsp; TypeScript를 사용하는 프로젝트에서 반드시 string을 받아야하는 특정 키값에 대하여 env로 넘기게 되면 해당 에러를 마주하게 된다

&nbsp; 이는 env의 타입이 지정되어 있지 않기 때문에 발생하는 오류인데, <br>`.d.ts` 파일의 생성을 통해 전역 객체에 있는 타입들을 확장해서 내가 원하는 타입을 선언하고 namespace로 지정할 수 있다

<img src="https://user-images.githubusercontent.com/82315118/221933805-b2c5ef10-d8b1-4a23-bda9-e3dd46824122.png" />

<br>

**_결과_**

<img src="https://user-images.githubusercontent.com/82315118/221933811-16b19dd5-82f3-4850-b679-5227db7ee733.png" />
