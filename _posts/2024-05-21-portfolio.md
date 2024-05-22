---
layout: single
title:  "정의효 | 백엔드 개발자"
categories:
  - portfolio
---

# 240521
* 학원 서버 종료되서 로컬에서 서버 연결중
* mysql - dbeaver 계정 생성 오류발생 - hosts 파일에서 이름을 localhost -> definitionhyo 추가
* 사용자로 등록이 안되있어 cmd실행후 mysql연결 후 USER CREATE 및 GRANT 옵션 부여 후 FLUSH PRIVILEGES < mysql에서 쿼리 작성 후 테이블 다시 로드
  * mysql -u root -p / CREATE USER 'definitionhyo'@'localhost' IDENTIFIED BY 'password'; / GRANT ALL PRIVILEGES ON *.* TO 'definitionhyo'@'localhost' WITH GRANT OPTION; / FLUSH PRIVILEGES;

* 새로운 사용자 생성 후 기존 db 옮기는법(debeaver, mysql사용 기준) : db우클릭 -> 도구 -> dump(폴더,파일이름 작성후 start) 후 복사 하려는 곳에 restore

* 동백시네마는 잘 되는데(프로젝트 실행하니까 오류뜸->definer제거 해봄)
zero는 오류 뜸
Task execution failed

이유:
 Error executing process  
 mysql버전차이 오류 -> 덤프할때 mysql 바이너리로 해봄 -> 안됨, 상세보기 결과 -> ERROR 1449 (HY000): The user specified as a definer ('@@@@'@'%') does not exist 덤프 파일에 포함된 일부 뷰, 트리거 또는 저장 프로시저가 특정 사용자를 정의자로 설정하고 있는데, 해당 사용자가 현재 MySQL 서버에 존재하지 않아서 발생 -> DEFINER= 부분을 찾아서 1. 현재 존재하는 사용자로 변경 2. 정의자 제거 or 빈문자열로 변경 -> 정의자 제거함 -> 됨