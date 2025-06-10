# 레포지토리 네이밍 규칙

- 모든 레포지토리 이름은 소문자로 작성해야 합니다.
- 언더스코어(`_`) 사용 허용: 단어 구분이 필요한 경우에는 `_`로 처리합니다.
- 가능한 경우 단어를 붙여 쓰기 (`deepscanbackend`)

- **대문자 사용 금지**: Git은 대소문자를 구분하지만, 일부 OS에서는 혼동을 일으킬 수 있습니다.
- **하이픈(`-`) 사용 금지**: Java 패키지, import 경로 등에서 사용이 불가능하거나 제한이 있습니다.

- C# 프로젝트의 경우에는 예외적으로 PascalCase를 권장합니다. 예: `DeepscanBackend`
- 문서 전용 저장소의 경우에는 하이픈(-) 사용을 허용합니다.
문서 중심의 레포지토리는 가독성과 명확성을 우선으로 하여, 예: `coding-convention`, `data-science-notes`  

## 예시

| 올바른 예 | 설명 |
|-----------|------|
| `deepscan_backend` | 단어 구분이 필요한 경우 |
| `csharppractice` | 붙여 쓰는 형식 |
| `javaapi` | 간단한 형식 |
| `DeepscanBackend` | **C# 프로젝트인 경우 권장** |
  
| 잘못된 예 | 문제 |
|------------|------|
| `Deepscan-Backend` | 대문자, 하이픈 포함 |
| `Kdt-Proj2-BE` | 혼합 표기, 불명확 |
| `deepscan-Backend` | 하이픈 + 대문자 혼용 |

## 기타

- 커밋 메시지는 [Conventional Commit](https://www.conventionalcommits.org/ko/v1.0.0/) 형식을 따르는 것을 권장합니다.
