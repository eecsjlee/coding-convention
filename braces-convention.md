# 중괄호 `{}` 스타일

Java는 기본적으로 다음 **두 가지 스타일** 중 하나를 사용

## 1. **K\&R 스타일 (Kernighan & Ritchie style)** – 자바 기본 스타일

```java
public String getEmail() {
    return email;
}
```

## 2. **One-liner 스타일** – 아주 짧은 코드일 때만 사용

```java
public String getEmail() { return email; }
```

이건 **getter처럼 한 줄짜리 메서드**를 간결하게 표현하고 싶을 때 가끔 사용
하지만 Java에서는 잘 안 씁니다.

> 이런 스타일은 JavaScript나 C#에서는 자주 쓰지만,
> Java에서는 팀 코드 컨벤션에 따라 **권장하지 않음**

## 어떤 게 좋은가?

> **Java에서는 `{}`는 줄바꿈해서 쓰는 게 표준**입니다.

그러니 다음처럼 작성하는 게 가장 좋습니다

```java
public String getEmail() {
    return email;
}
```

## IntelliJ에서 스타일 자동 적용

1. `Ctrl + Alt + L` 또는 `Code > Reformat Code`
2. 설정: `File > Settings > Code Style > Java`
3. `{` 스타일도 설정 가능!
