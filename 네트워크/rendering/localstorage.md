# 로컬스토리지

> 로컬스토리지는 웹 스토리지 객체로 브라우저 내에 { key : value } 형태로 오리진에 종속되어 저장되는 데이터를 뜻함
> 
- 하나의 키에 오로지 하나의 값만 저장됨
- 데이터는 사용자가 브라우저에서 수동으로 삭제하지 않는 한 평생 동안 로컬저장소에 저장되며 만료날짜가 없음
    - 사용자가 창이나 탭을 닫아도, 컴퓨터를 종료해도 만료되지 않음
- 최대 저장용량은 5MB
- 로컬스토리지 데이터는 자동으로 서버로 전송되지 않(쿠키는 자동 전송됨)

</br>

### 사용법

- 설정 : localStorage.setItem(key, value);
- key에 해당하는 value가져오기 : localStorage.getItem(key);
- 제거 : localStorage.removeItem(key);
- 전체제거 : localStorage.clear()

</br>

[momentom 클론 中](https://github.com/GEON1999/momentom_js/blob/main/js/todo.js)

- 로컬스토리지 사용 프로젝트

</br>

## URL

![https://blog.kakaocdn.net/dn/C6XK5/btrHdwRZ3ur/HRw5pH5V26sRgRWuVuSzm0/img.png](https://blog.kakaocdn.net/dn/C6XK5/btrHdwRZ3ur/HRw5pH5V26sRgRWuVuSzm0/img.png)

- 오리진이 같은 브라우저 내에서 로컬스토리지를 공유함
- https 의 default prot 는 443 이며 생략될 수 있음
