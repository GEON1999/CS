# 브라우저 랜더링
1. DOM 트리 구축
2. 렌더트리와 렌더레이어 생성
3. 렌더레이어를 대상으로 Layout 설정
4. 렌더레이어를 대상으로 칠하기(paint)
    1. 픽셀마다 점을 찍듯 칠합니다. 이를 레스터화라고도 함
5. 레이어 합치기(composite layer) 및 표기
    1. 각각의 레이어로부터 비트맵이 생성되고 GPU에 텍스처로 업로드됨
    2. 그다음 텍스처들은서로 합쳐져 하나의 이미지로 렌더링되며 화면으로 출력됨
        
</br>

[모던자바스크립_박건_github](https://github.com/GEON1999/Modern-JavaScript-Deep-Dive/blob/main/docs/Today%20I%20Learn%20(3%EB%B6%84%EA%B8%B0)/ch38_%EB%B8%8C%EB%9D%BC%EC%9A%B0%EC%A0%80%EC%9D%98%20%EB%A0%8C%EB%8D%94%EB%A7%81%20%EA%B3%BC%EC%A0%95/%ED%95%98%EB%A3%A8_TIL.md, "github")

- 브라우저 랜더링 과정에 대한 자세한 기록
