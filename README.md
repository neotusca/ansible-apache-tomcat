# ansible-apache-tomcat


1. 수행시 진행되는 작업
- 디렉토리(/svc/uplus/web/apache, was/tomca) 생성
- 계정 (apache:web, tomcat:was) 생성
- app. 다운로드 (apache-httpd, apr, apr-util, pcre, tomca-connector, apache-tomcat)
- 패키지 설치 (openssl-devel, expat-devel)
- app. 압축해제 및 컴파일

2. 조건
- ansible설치필요 (epel-release패키지 설치되어야 설치가능)

3. 수행설정
- group_vars/all

4. 수행방법
- 압축파일을 Cent7, Oraclelinux7에 업로드, 압축해제하여 아래 스크립트 수행
- sh apply-ansible.sh  (root계정으로 실행)

5. 버그
- 수정완료 
    - apache-tomcat압축해제 디렉토리가 예상과 다르게 해제복사되나 수작업처리하면됨

6. 주의점
- 소스 다운로드시 미러사이트의 링크소실에 대비하여 원조사이트(apache.org)에서 다운로드로 인해 속도가 느림
- 오라클 java링크의 경우, 수개월 내 링크소실 가능성있음

