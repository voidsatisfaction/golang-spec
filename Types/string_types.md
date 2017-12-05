# String types

# 문자열 타입

* spec 버전: of June 28, 2017
* 원문 : [String types](https://golang.org/ref/spec#String_types)
* 번역자 : [연규민](@voidsatisfaction)

A *string type* represents the set of string values. A string value is a (possibly empty) sequence of bytes. Strings are immutable: once created, it is impossible to change the contents of a string. The predeclared string type is `string`.

*문자열 타입*은 문자열 값들의 집합을 나타낸다. 하나의 문자열 값은(비어있을 수 있음) 바이트들의 연속 이다. 모든 문자열은 불변이다: 한 번 생성된 문자열의 내용을 변경하는 것은 불가능하다. 미리 선언된 문자열의 타입은 `string`이다.

The length of a string s (its size in bytes) can be discovered using the built-in function `[len](/Built-in%20functions/length_and_capacity.html)`. The length is a compile-time constant if the string is a constant. A string's bytes can be accessed by integer [indices](/Expressions/index_expressions.html) 0 through `len(s)-1`. It is illegal to take the address of such an element; if `s[i]` is the i'th byte of a string, `&s[i]` is invalid.

어떠한 문자열 s의 길이(바이트 사이즈)는 내장함수인 `[len](/Built-in%20functions/length_and_capacity.html)`를 이용해서 구할 수 있다. 그 길이는 만일 그 문자열이 상수이면 컴파일시에도 상수이다. 한 문자열의 바이트는 0부터 `len(s)-1`까지의 정수 [인덱스들](/Expressions/index_expressions.html)로 접근 가능하다. 그러나 문자열의 요소 하나의 주소를 가져올 수 없다; 만약 `s[i]`이 한 문자열의 i번째 바이트라면, `&s[i]`는 사용할 수 없다.
