## DBMS

- 대부분 오라클 사용
- MySQL :  소규모,, 학습용으로 많이 사용,    오라클에 팔렸음 --> 상용화 움직임 보임
- 마리아DB : 많은 부분 MySQL과 같음, 오픈화되어있는 데이터베이스 시스템
- SQLite 도 해당됨

대부분 Relational Database 이다.

![image-20210413133516905](https://github.com/SUJEONG999/DBMS/blob/master/images/image1.PNG)

##  CRUD

create , read, update, delete  ---> SQL(structured Query Language) - IBM - ANSI

ex) 장고 할때, 사용자가 입력한 게시판글!!



 << [] 는 생략 가능 의미 >>

C,U,D는 DML이라고함.

C : 미리 테이블은 만들어져있다.  Insert into 테이블명 [(컬럼명 리스트, ....)] values (데이터값 리스트, ....)

U : update 테이블명 set 컬럼명 = 컬럼값, ........  [where 조건식]

D : delete [from] 테이블명   [where 조건식]

​			-----------------------> commit, rollback

R :  꺼내옴   /   select 추출하고자하는 컬럼명, ..... 

​						 from  테이블명

​						[ where 조건식 ]

​						[ group by 그룹핑 기준 칼럼 또는 식]

​						[ having 그룹조건 ]

​						[order by 정렬 기준 컬럼 [ desc ], ..... ]

- select now() ;  ----> 마리아DB
- select sysdate from dual; -------> 오라클DB



select * from where ename = 'Kim' --> 문자열 데이터 값 : 단일 인용부호만 (')



1. select  * from where ename = 'Kim'  or ename = 'Kang' or ename = 'Kong'

2. select  * from where ename in ( 'Kim' , 'Kang' , 'Kong')

3. select  * from where ename like 'K%'

   % : 0개 이상의 임의의 문자

   _ : 임의의 한 문자

   'K%' , '%K', '%K%'

-------------------------------

Storage area는 하드디스크의 공간... 어떤 플랫폼 환경이냐에 따라서 파일 형태로 저장되어 있다.

저장되어있는 읽어오거나 ...



공식언어 SQL ---> CRUD작업



장고 웹서버프로그램(Application)이고 SQLite (DBMS)



![image-20210413133516906](https://github.com/SUJEONG999/DBMS/blob/master/images/image1.PNG)

레코드(튜플)

인스턴스

어트리뷰트(속성)