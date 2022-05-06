2022년 5월 6일 금요일


# SQL

- 데이터베이스
    - 데이터베이스란 여러 사람들이 공유하고 사용할 목적으로 통합 관리되는 데이터들의 모임.
    - 실시간 접근성, 계속적인 변화, 동시 공유, 참조
- 데이터베이스 기본 기능
- 데이터베이스 종류
- 관계형 데이터베이스
    - 관계형 데이터베이스 모델은 키( key )와 값 ( value )으로 이루어진 데이터들을 행( row )과 열 ( Column )로 구성된 테이블 구조로 단순화 시킨 모델
    - 관계형 데이터베이스 소프트웨어 (DBMS)
- SQL 기초지식
- 아키텍처
    - 최적화를 목표로 두고 시스템 구성과 동작원리 그리고 시스템의 구성환경등을 설명 및 설계하는 청사진 또는 설계도
- 가용성
    - 정상적으로 사용 가능한 정도
- 확장성
    - 확장이 얼마나 쉽고 가능한지에 대한 용이성
- 서버의 다중화
    - Active / Active
    - Active / Standby
    - 리플리케이션

# MYSQL

- 데이터베이스 생성
    - CREATE DATABASE dbname;
- 데이터베이스 목록
    - SHOW DATABASES;
- 데이터베이스 사용
    - USE dbname;
- 데이터베이스 삭제
    - DROP DATABASE [IF EXISTS] dbname;

- 테이블 생성
    - CREATE TABLE 테이블명 ( 컬럼명 데이터형, 컬러명 데이터형, 기본키 셋 );
    - 옵션 (UNSIGNED NOT NULL AUTO_INCREMENT, PRIMARY KEY)
- 테이블 조회
    - SHOW TABLES
    - DESC 테이블명
- 테이블 삭제
    - DROP TABLE 테이블명

- 데이터 추가
    - INSERT INTO 테이블이름 (컬럼명, ...) VALUES (컬럼값, ...);
- 데이터 검색
    - SELECT * FROM 테이블이름
- 데이터 수정
    - UPDATE 테이블이름 SET 컬럼명=컬럼값, ... WHERE 조건;
- 데이터 삭제
    - DELETE FROM 테이블이름 WHERE 조건;

