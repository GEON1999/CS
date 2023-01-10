## XML

JSON

```jsx
{
	"MovieList" : [
		{
			"name" : "spiderman",
			"rate" : 5
		},
		{
			"name" : "ironman",
			"rate" : 4
		}
	]
}
```

⇒

XML

```jsx
// 프롤로그. 버전과 인코딩 등을 표기
<?xml version="1.0" encoding="UTF-8">
<MovieList>
  <Movie>
    <name>spiderman</name> <rate>5</rate>
  </Movie>
  <Movie>
    <name>ironman</name> <rate>4</rate>
  </Movie> 
</MovieList>
```

- JSON 과 같이 중괄호가 아니라 닫힌 태그로 이루어진 구조 데이터
- 닫힌 태그가 계속해서 들어가기 때문에 JSON 과 비교했을 대 무거움
- 자바스크립트 Object 로 변화하기가 JSON 보다 힘듬
- html 태그와는 별개로 XML 에는 기본 제공 이름이 없음 (div, span 등)

### sitemap.xml

- xml 의 대표적인 사용사례는 sitemap.xml 이다.
    - sitemap.xml 은 SEO 를 위해 필수적인 존재다.
    - google 을 예시로, 웹 크롤러가 신규 또는 최근에 업데이트된 페이지를 지나치거나 서로 링크가 종속적으로 연결되지 않은 경우 google 이 일부 페이지를 누락할수 있음. 이를 sitemap.xml 이  방지함
