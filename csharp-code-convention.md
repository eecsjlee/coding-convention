좋습니다! 아래는 `csharp-code-convention.md` 파일에 들어갈 수 있는 **기본 틀 템플릿**입니다. Microsoft의 공식 스타일 가이드와 업계 관행을 참고해 **실무에 적합하도록 요약**했습니다.

---

## 📄 C# 코딩 컨벤션 (`csharp-code-convention.md`)

### 1. 파일 및 클래스 구성

* 파일당 하나의 주요 클래스만 선언
* 클래스명과 파일명을 일치시킬 것
  예: `UserService.cs` → `public class UserService`

---

### 2. 네이밍 규칙

| 대상         | 규칙           | 예시                           |
| ---------- | ------------ | ---------------------------- |
| 클래스/인터페이스  | PascalCase   | `UserService`, `IRepository` |
| 메서드        | PascalCase   | `GetUserById()`              |
| 변수         | camelCase    | `userCount`, `isValid`       |
| 상수         | PascalCase   | `MaxRetryCount`              |
| private 필드 | `_camelCase` | `_logger`, `_cache`          |
| enum       | PascalCase   | `UserRole.Admin`             |

---

### 3. 들여쓰기 및 공백

* 스페이스 4칸 들여쓰기
* 연산자 주변, 콤마 뒤에는 한 칸 공백
* 메서드 간 공백 1줄, 클래스 간 2줄
* `if`, `for`, `while` 등은 항상 중괄호 사용

```csharp
if (isEnabled)
{
    Execute();
}
```

---

### 4. using 및 네임스페이스

* `System` 관련 using은 항상 최상단
* 알파벳 순서로 정렬
* 사용하지 않는 using 제거

```csharp
using System;
using System.Collections.Generic;
using MyApp.Services;
```

---

### 5. 접근제한자 및 순서

* 접근 제한자를 **항상 명시**
* 클래스 구성 순서:

  1. Fields
  2. Constructors
  3. Properties
  4. Methods
  5. Events

---

### 6. 메서드 작성 규칙

* 하나의 메서드는 하나의 책임만 갖는다 (단일 책임 원칙)
* 비동기 메서드는 `Async` 접미사 사용

  ```csharp
  public async Task<User> GetUserAsync(int id)
  ```

---

### 7. 주석 규칙

* XML 주석 스타일 사용 권장 (`///`)
* 꼭 필요한 경우에만 주석 사용
* `TODO`, `FIXME` 태그 사용

```csharp
/// <summary>
/// 사용자를 ID로 조회합니다.
/// </summary>
public User GetUserById(int id)
```

---

### 8. 예외 처리

* 가능한 한 세부적인 예외 타입을 catch
* 공백 catch (`catch {}`) 금지
* 로그 기록 필수

```csharp
try
{
    DoWork();
}
catch (IOException ex)
{
    _logger.LogError(ex, "파일 입출력 오류");
}
```

---

### 9. 기타 스타일

* ternary operator는 간단한 경우만 사용
* null 병합 연산자 적극 활용 (`??`, `??=`)
* C# 8.0 이상에서는 switch expression 사용 권장

```csharp
var result = input switch
{
    1 => "One",
    2 => "Two",
    _ => "Other"
};
```

---

## ✅ 참고 링크

* [Microsoft 공식 C# 코딩 규칙](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions)
* [C# Naming Guidelines - .NET Foundation](https://docs.microsoft.com/en-us/dotnet/standard/design-guidelines/naming-guidelines)

---

필요하다면 이 틀을 **Markdown 파일로 추출하거나**, 팀 내부 스타일에 맞게 커스터마이징해드릴 수도 있어요.
