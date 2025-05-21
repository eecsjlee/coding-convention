# Code Convention (공통 코딩 컨벤션)

이 레포지토리는 프로젝트에 참여하는 모든 개발자들이 언어에 관계없이 **일관된 스타일과 가독성 높은 코드**를 작성할 수 있도록 돕기 위한 **범용 코딩 컨벤션**입니다.

언어별 세부 규칙은 별도 문서를 참고하세요:
- [C# 코딩 컨벤션](./csharp-code-convention.md)
- [Python 코딩 컨벤션](./python-code-convention.md)
- [JavaScript/TypeScript 코딩 컨벤션](./js-ts-code-convention.md)

---

## 1. 들여쓰기 (Indentation)

- 들여쓰기는 **공백 4칸**을 기본으로 합니다. (탭 사용 금지)
- 중첩 블록 구조는 명확하게 들여씁니다.

## 2. 중괄호 사용 (Braces)

- **항상 중괄호를 명시**합니다.
- 한 줄짜리 조건문, 반복문도 생략하지 않습니다.

```csharp
// Bad
if (isOk) DoSomething();

// Good
if (isOk)
{
    DoSomething();
}
````

## 3. 공백 사용 (Whitespace)

* 연산자 주변, 쉼표 뒤에는 **공백을 추가**합니다.
* 함수명과 괄호 사이에는 공백을 넣지 않습니다.

```js
// Good
const sum = a + b;
function greet(name) { ... }
```

## 4. 줄 길이 (Line Length)

* 한 줄 최대 **100자\~120자**를 넘지 않도록 작성합니다.
* 긴 표현식은 의미 있는 단위로 줄바꿈합니다.

## 5. 네이밍 규칙 (Naming)

| 항목      | 규칙                 |
| ------- | ------------------ |
| 변수, 함수  | `camelCase`        |
| 클래스, 타입 | `PascalCase`       |
| 상수      | `UPPER_SNAKE_CASE` |

## 6. 파일/폴더 이름

* **소문자-hyphen-case** 또는 **CamelCase**를 권장합니다.
* 언어별 규칙이 있다면 해당 언어 컨벤션 문서에 따릅니다.

## 7. 주석 (Comment)

* 주석은 **무엇을** 했는가보다 **왜** 했는지를 설명합니다.
* TODO, FIXME는 명확하게 태그를 달고 작성합니다.

```js
// TODO: 에러 처리 로직 추가 필요
```

## 8. 빈 줄 (Line Break)

* 논리적 단위가 끝나면 **빈 줄로 구분**하여 가독성을 높입니다.

## 9. 코드 정렬 및 순서

* 파일 내 요소 정렬은 다음과 같은 순서를 권장합니다:

  * 상수 → 변수 → 함수 → export 또는 public API
  * 클래스 내부: 필드 → 생성자 → 메서드 순


## 📁 언어별 컨벤션

* 언어나 프레임워크 특성에 맞는 세부 규칙은 아래 문서를 참고해주세요.

| 언어                    | 문서 링크                                                    |
| --------------------- | -------------------------------------------------------- |
| C#                    | [csharp-code-convention.md](./csharp-code-convention.md) |
| Python                | *(예정)* `python-code-convention.md`                       |
| JavaScript/TypeScript | *(예정)* `js-ts-code-convention.md`                        |

## 기타 참고 사항

* 자동화된 코드 포맷터(예: Prettier, dotnet-format, Black 등)를 사용하여 포맷 일관성을 유지하는 것을 권장합니다.
* 모든 PR은 이 컨벤션을 기준으로 코드 리뷰를 받게 됩니다.

