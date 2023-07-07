---
layout: single
title:  "1st team project(itwillbs)"
categories:
  - projects
---

<!-- 프로젝트 시작하는날부터 블로그에 정리하려고 했으나
    프로젝트, 정처기 필기시험 준비하느라 그렇게 못했다는점..
    그래서 일자별 한일이 정확하지않음..
    그래서 중간중간 시간내서 했어야 했다고 생각함..
    2차 프로젝트때는 매일매일 뭐했는지 기록하기 
    강사님 : 주석 중요 필수! 
    중간중간 주석을 넣기는 했으나 상세하게 안넣어서 플젝끝나고 주석 넣고 있는중.
    다음플젝부터는 코드짜면서 주석도같이하기!-->

# 프로젝트명 : 영화 예매 사이트

## 개발 기간 : 23-05-17 ~ 23-06-30
* 프로젝트 인원 : 7인
* 개발 언어 : 자바 , JSP, HTML, JS, CSS
* 사용기술 : jQuery, AJAX, JSON, MyBatis, Bootstrap, spring
* 서버 & DB : Apache Tomcat, MySQL
* 협업도구 : GitHub, Notion, Discord, GoogleDrive
* <details>
    <summary>개발 일정</summary>
    <ul> 
        <li>05-17 ~ 05-22 : 아이디어 회의</li>
        <li>05-18 ~ 05-22 : 화면 구상</li>
        <li>05-18 ~ 06-01 : 요구사항 정의</li>
        <li>05-19 ~ 05-29 : DB설계</li>
        <li>05-29 ~ 06-12 : DB수정 및 기능구현</li>
        <li>06-12 ~ 06-29 : 기능구현</li>
        <li>06-27 ~ 06-30 : 오류수정 및 발표</li>
    </ul>
  </details>
<br>

## 담당 파트
<!--팀원 모두가 첫 프로젝트라 기획단계 예를 들면 요구사항정의서, 화면구상도 테이블정의서 부분에서 더 많은 회의를하고 좀 더 세분화 시키고 생각을 많이 해봤어야했는데 그렇게 하지않아 프로젝트 도중에도 DB의 제약조건, 컬럼추가 등의 우역곡절이 많았음 
+ 우리 팀은 먼저 화면구현(뷰) 먼저하고 기능 중심으로 조를 나눠 자신이 구현했던 뷰가 아닌 다른뷰의 기능을 구현했음 -> 의도는 맡은 파트가 아닌 다른 파트도 구현하며 여러 기능들을 구현하고싶었음 -> 현실은 뷰는 뷰일 뿐이었고 기능을 나누어 자신이 담당한 파트를 구현하는것만으로도 어려웠음 --> 
* 구현
  * 관리자 - 회원관리(수정,삭제)
  * 관리자 - 영화관리(api, 등록, 삭제 수정)
  * 관리자 - 결제관리(api)<br><br>
* 사용한 기능
  * jstl(if, forEach, choose, when, otherwise)
  * bootstrap
  * jqeury
  * ajax
  * api
  * CRUD
  * 검색
  * 페이징처리
<br>
* admin_member_list
  * CRUD
  * 검색
  * bootstrap 모달
  * jstl(if, foreach, when, choose)
  * <details>
    <summary>느낀점</summary>
    <ul> 
      <li>자바스크립트에서 memberID를 받아서 사용하기위해 member_id를 받아서 저장해야함 -> 스크립트에서 EL을 통해 가져오는 값을 사용하기 위해 jQuery의 $(selector).data(key, value)를 사용</li>
      <li>controller 뿐만아니라 jQuery로 값을 전달할때 속성값을 전달할 수 있음 -> onclick="deleteNonMember('${member.member_id}')"</li>
      <li>뷰에서 확인창을 구현하기위해 부트스트랩에서 모달코드를 가져와서 어떤 형태로 구성되고, 구현되는지 숙지 후 사용을 하였다. -> 모달뿐만이 아니라 다른 기능을 구현할때 사용할 코드들도 어떻게 사용되는지, 어디로 매핑되는지, 어떤값을 보내야 하는지, 그리고 어떤 상황일때 어떻게 실행이되는지 = 어떻게 구현하고 코드가 어떻게 실행되는지 정리하는것이 중요하다고 느낌</li>
    </ul>
    </details>

* admin_member_oneperson
  * CRUD
  * bootstrap 모달
  * jstl(choose, when, formatNumber(fmt))
* admin_movie_management
  * CRUD
  * bootstrap 모달
  * jstl(choose, when)
* admin_movie_detail
  * API(kobis)
  * CRUD
  * bootstrap 모달
  * jQuery

* admin_movie_regist
  * CRUD
  * ajax
  * jQuery
  * <details>
    <summary>느낀점</summary>
    <ul> 
      <li>api를 통해 가져온 값을 저장, ajax를 통해 페이지 이동없이 입력되도록 구현하는게 처음엔 힘들었지만 개념을 이해하고나니 어떻게 해야하는지 느낌이와서 총 2개를 사용했는데 첫번째로 api(kobis)를 통해 영화제목을 받아와서 저장 후 api(kobis) 받아온 영화제목을 data값으로 보내 상세정보를 한번더 받아와서 ajax로 입력되도록 하였음.</li>
    </ul>

* admin_payment_list
  * CRUD
  * jstl(forEach, choose, when)

* admin_payment_list_detail
  * CRUD
  * ajax


## 느낀점 & 보완점
