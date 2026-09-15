# 실습과제: 여러 브랜치를 활용한 GitHub 버전관리

## 1. 과제 목표

SourceTree와 GitHub를 이용하여 **하나의 웹 프로젝트를 여러 브랜치로 나누어 관리**하고,  
각 브랜치에서 작업한 내용을 최종적으로 `main` 브랜치에 병합합니다.

> 웹페이지의 디자인 완성도보다 **Branch → Commit → Merge → Push 과정**을 올바르게 수행하는 것이 핵심입니다.

---

## 2. 과제 주제

### 나를 소개하는 간단한 웹페이지 만들기

`index.html`을 이용하여 간단한 자기소개 웹페이지를 제작합니다.

예시 내용

- 이름 / 학과
- 간단한 자기소개
- 관심 분야 또는 취미
- 이메일 또는 GitHub 주소

---

## 3. 실습 조건

다음 조건을 모두 만족해야 합니다.

- GitHub Repository 1개 생성
- `main` 브랜치 사용
- `feature/...` 형식의 브랜치 **3개 이상 생성**
- 전체 커밋 **6개 이상**
- 각 기능 브랜치를 GitHub에 Push
- 최종적으로 각 기능 브랜치를 `main`에 Merge
- **병합 충돌(Conflict) 1회 이상 발생시키고 직접 해결**
- 최종 `main` 브랜치를 GitHub에 Push

---

## 4. 브랜치 구성

다음과 같이 브랜치를 생성합니다.

```text
main
├─ feature/profile
├─ feature/hobby
└─ feature/contact
```

### `feature/profile`

자기소개 내용을 추가합니다.

- 이름
- 학과
- 간단한 소개

**커밋 2회 이상**

예시

```text
profile 기본 정보 추가
profile 자기소개 내용 수정
```

### `feature/hobby`

관심 분야 또는 취미 내용을 추가합니다.

**커밋 2회 이상**

예시

```text
관심 분야 내용 추가
취미 내용 추가
```

### `feature/contact`

연락처 정보를 추가합니다.

예시

- 이메일
- GitHub 주소

**커밋 1회 이상**

```text
contact 정보 추가
```

---

## 5. 실습 순서

### STEP 1. GitHub Repository 생성

Repository 이름 예시

```text
MyProfile-Web
```

SourceTree에서 해당 Repository를 연결합니다.

---

### STEP 2. `main` 브랜치 기본 파일 작성

`index.html`을 생성하고 기본 웹페이지를 작성합니다.

최초 커밋 예시

```text
프로젝트 기본 페이지 생성
```

GitHub에 Push합니다.

---

### STEP 3. 기능별 브랜치 생성

`main` 브랜치를 기준으로 다음 브랜치를 생성합니다.

```text
feature/profile
feature/hobby
feature/contact
```

브랜치를 만들 때 현재 작업 중인 브랜치를 반드시 확인합니다.

---

### STEP 4. 각 브랜치에서 작업 및 커밋

각 브랜치로 **Checkout**하여 해당 기능을 작성합니다.

작업 후

```text
파일 수정
→ Stage
→ Commit
→ Push
```

순서로 진행합니다.

---

### STEP 5. 충돌(Conflict) 발생시키기

두 개의 브랜치에서 `index.html`의 **같은 부분 또는 같은 줄을 서로 다르게 수정**합니다.

예시

`feature/hobby`

```html
<h2>저의 관심 분야입니다.</h2>
```

다른 브랜치

```html
<h2>저의 취미를 소개합니다.</h2>
```

이후 브랜치를 병합하여 충돌을 발생시킵니다.

VSCode에서 충돌 내용을 확인하고 다음 기능 중 적절한 방법을 선택하여 해결합니다.

```text
Accept Current Change
Accept Incoming Change
Accept Both Changes
```

충돌 해결 후 다시 Commit합니다.

---

### STEP 6. `main` 브랜치로 병합

SourceTree에서 `main` 브랜치로 Checkout한 후 각 브랜치를 병합합니다.

예시

```text
feature/profile
        ↓
      main

feature/hobby
        ↓
      main

feature/contact
        ↓
      main
```

모든 병합이 완료되면 최종 `main` 브랜치를 GitHub에 Push합니다.

---

## 6. 최종 History 확인

SourceTree의 **History → 모든 브랜치**에서 브랜치가 분기되고 다시 병합된 모습을 확인합니다.

예시

```text
                    ●─●  feature/profile
                   /   \
●─────────────────●─────●
 \                       \
  ●─●  feature/hobby      ●──── main
       \                  /
        ●  feature/contact
```

> 정확히 같은 모양일 필요는 없습니다.  
> 여러 브랜치에서 각각 커밋한 흔적과 최종 병합된 과정이 확인되면 됩니다.

---

## 7. 제출물

다음 **3가지**를 제출합니다.

### ① GitHub Repository URL

예시

```text
https://github.com/아이디/MyProfile-Web
```

### ② SourceTree History 화면 캡처 1장

다음 내용이 보이도록 캡처합니다.

- `main`
- 3개 이상의 `feature/...` 브랜치
- 각 브랜치의 커밋
- Merge 과정

### ③ 완성된 웹페이지 실행 화면 캡처 1장

브라우저에서 최종 결과를 실행한 화면을 제출합니다.

---

## 8. 필수 확인사항

제출 전 아래 내용을 확인합니다.

- [ ] GitHub Repository를 생성했는가?
- [ ] `feature/...` 브랜치를 3개 이상 생성했는가?
- [ ] 전체 커밋이 6개 이상인가?
- [ ] 각 브랜치를 GitHub에 Push했는가?
- [ ] 병합 충돌을 1회 이상 해결했는가?
- [ ] 모든 기능을 `main` 브랜치에 Merge했는가?
- [ ] 최종 `main` 브랜치를 GitHub에 Push했는가?
- [ ] SourceTree History에서 브랜치 분기와 병합 과정이 확인되는가?

---

## 9. 평가 기준

웹페이지의 디자인 완성도보다 다음 내용을 중심으로 평가합니다.

- 브랜치를 기능별로 올바르게 생성했는가?
- 브랜치별로 적절하게 Commit했는가?
- Checkout을 이용하여 브랜치를 이동했는가?
- Merge 과정을 올바르게 수행했는가?
- 충돌(Conflict)을 직접 해결했는가?
- 로컬 저장소의 변경 내용을 GitHub 원격 저장소에 정상적으로 Push했는가?
- SourceTree History에서 전체 버전관리 과정이 확인되는가?
