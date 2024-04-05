# LLM-HyperClova-X
📗 Naver HyperClova X Model Study

### Theme 1. Summary Model
- 일시 : 2024.02.20
- 사용한 데이터셋 : -
- 개요 : Clova X Summary API를 사용해서 요약 모델을 생성
- 참고 : [Naver Cloud Platform](https://medium.com/naver-cloud-platform/%EC%9D%B4%EB%A0%87%EA%B2%8C-%EC%82%AC%EC%9A%A9%ED%95%98%EC%84%B8%EC%9A%94-clova-summary%EB%A1%9C-%EB%89%B4%EC%8A%A4-%EC%9A%94%EC%95%BD-%EC%84%9C%EB%B9%84%EC%8A%A4-%EB%A7%8C%EB%93%A4%EA%B8%B0-%EC%9D%B4%EA%B1%B4-%EB%A7%88%EC%B9%98-%EC%84%B8%EC%A4%84-%EC%9A%94%EC%95%BD-%EB%B4%87-dac29e97d1e4)
- 모델 생성 후기

| 구분 | 장점 | 단점 |
| ----------------------- | ---------------------------------------------- | ---------------------------------------------- |
| HyperClova Summary API | 1. 별도의 Prompt 없이 Summary API를 사용해서 간단하게 요약문을 생성할 수 있다. <br> 2. 결과가 빠르게 생성된다. <br> 3. language, model, tone, summaryCount라는 4가지 파라미터를 조정해서 결과를 다듬을 수 있다. <br> 4. 전체 기사에서 중요한 문장을 선정해서 요약문을 만드는 방식으로 문장 재구성, 새로운 어휘 등을 사용하지 않는다.|1. Prompt가 없기 때문에 여러 명령을 입력할 수 없다. 결과가 정적이다. <br> 2. 한국어, 일본어만 요약문을 생성할 수 있다. <br> 3. 문장 단위로만 요약해주기 때문에 빠르게 읽기는 좋지만, 생략되는 문장이 많다. <br> 4. 중요 문장 추출 같은 느낌이라, summaryCount를 늘리면 요약 이전의 기사와 비슷해진다.|
| Open AI GPT | 1. Prompt를 사용해서 모델의 성격이나, 답변의 어조 등 다양한 부분을 조절할 수 있다. <br> 2. 문장을 연결하고, 재구성하는 등 요약문에 더 많은 내용을 담는다. |1. 결과 생성이 오래 걸린다. API 요청 전송과 결과를 받아오는데 약 20초 정도 걸린다. <br> 2. GPT가 오직 요약만을 위한 모델이 아니기 때문에 재구성하는 과정에서 Hallucination(환각효과)이 우려되기도 한다.|

