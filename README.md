# R_dataanalysis_source
삼양미디어 처음 시작하는 R데이터분석 책 소스

1. 1차수정 
- 2022.04.03 : "https://en.wikipedia.org/wiki/World_population" 사이트의 업데이트로 테이블이 3번에서 4번으로 변경됨
- 소스코드 변경 내용 ch03_basic_grammar.R : 
  df_wp_raw <- as.data.frame(wp[4] %>% html_table())

2. 2차수정
- 2022.4.23 : R4.2.0버전에서 파일의 한글 인코딩문제
- 파일 인코딩이 표준인 utf-8 를 따르도록 read.csv()함수가 변환되어서 ansi로 저장된 데이터파일 일부를 utf-8로 변환

3. 3차수정
- 2022.6.26 : 데이터 현행화에 따른 소스코드 변경
- 변경소스 프로젝트 textbook2.zip

4. MASS 라이브러리 업데이트로 인한 dplyr 라이브러리의 select()함수 충돌문제
- 이유: MASS 라이브러리에 select()함수와 dplyr 라이브러리의 select()함수가 이름이 같아서 사용시 충돌 발생
- 해결방법 : 10장에서 MASS 라이브러리 사용후 dplyr 라이브러리의 select()함수 사용전에 다음 명령어를 사용해서 MASS 라이브러리 unload
             detach("package:MASS", unload = TRUE)
