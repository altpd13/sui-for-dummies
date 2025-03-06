# Move on Sui 입문자 가이드

[1. Move on Sui 소개](#1-move-on-sui-소개)

[2. Move on Sui의 주요 개념](#2-move-on-sui의-주요-개념)

[3. Move on Sui 기본 문법](#3-move-on-sui-기본-문법)

[4. Move on Sui 개발 환경 설정](#4-move-on-sui-개발-환경-설정)

## 1. Move on Sui 소개

### Move on Sui와 일반 Move의 차이점

- **객체 중심 설계(Object-centric model)**: 스마트 컨트랙트가 객체(Entity) 단위로 관리됨
- **병렬 실행 지원(Parallel execution)**: 성능을 극대화하기 위해 트랜잭션을 독립적으로 실행
- **소유권 기반 리소스 모델**: 리소스의 이동과 소유권을 명확히 정의하여 보안 강화

## 2. Move on Sui의 주요 개념

### 객체 중심(Object-centric)

#### Object Model
- Sui의 가장 기본적인 저장 단위는 오브젝트
- 이더리움은 key-value storage를 가지는 account centric
- Sui는 unique ID로 오브젝트들을 저장
- Move on Sui 언어 패키지 자체도 오브젝트(Sui move Package)
---

### 병렬 실행(Parallel Execution)

- 독립적인 객체는 동시에 처리 가능하여 성능 향상
- 글로벌 상태 업데이트 없이 트랜잭션 병렬 실행 지원

### 소유권 및 리소스 모델

- Move의 핵심 개념인 **리소스(Resource)**를 기반으로 소유권을 명확히 정의
- 특정 계정(Account)이 소유한 리소스는 안전하게 관리됨

## 3. Move on Sui 기본 문법

### 기본적인 Move 구조

```move
module example::MyModule {
    struct MyStruct has key, store {
        value: u64,
    }
    public fun create(value: u64): MyStruct {
        MyStruct { value }
    }
}
```

### 객체 생성 및 관리

```move
struct Token has key, store {
    id: u64,
    owner: address,
}
```

## 4. Move on Sui 개발 환경 설정

### 개발 도구

- Sui SDK 설치
- Move Prover 및 Move Analyzer 사용
- Sui 개발 환경(Sui CLI, Sui Wallet) 활용

### Sui 네트워크에서 배포

1. 스마트 컨트랙트 작성
2. Sui 테스트넷에서 배포
3. 트랜잭션 실행 및 디버깅

## 5. Move on Sui 활용 사례

- NFT 생성 및 거래
- DeFi 스마트 컨트랙트 개발
- 온체인 게임 및 디지털 자산 관리

## 6. 결론

- Move on Sui는 강력한 보안성과 성능을 제공하는 스마트 컨트랙트 언어
- 객체 중심 설계와 병렬 실행 지원으로 높은 확장성을 갖춤
- 앞으로 다양한 프로젝트에서 활용될 전망