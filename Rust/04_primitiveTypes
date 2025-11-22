## Boolean (bool)
is_morning
is_evening = !is_morning

## Character (char)
char for single quote(’C’, ‘한’, ‘3’…)
`is_alphabetic` → 영어 뿐만 아니라 다른 언어도 인식
`is_numeric` → 숫자 인식
그외 이모지, 공백 등은 alphabet, number로 인식x

## Array
stack에 저장되는 고정 크기 자료형
| **타입** | **크기** | **저장 위치** | **특징** |
| --- | --- | --- | --- |
| `[T; N]` (배열) | 고정 | 스택 | 빠르고 안전, 크기 변경 불가 |

```rust
let arr: [타입; 길이] = [값1, 값2, 값3, ...];
let numbers: [i32; 3] = [1, 2, 3];
let arr = [10, 20, 30]; //Rust가 자동으로 [i32; 3]으로 추론
```
```rust
//모든 요소가 같은 값으로 추론
let zeros = [0; 5]; //[0, 0, 0, 0, 0]
```

**배열 요소 접근**
```rust
let arr = [3, 5, 7];
println!("{}", arr[0]); // 3
println!("{}", arr[1]); // 5
println!("{}", arr[2]); // 7
```
다른 언어들처럼 인덱스로 각 배열 요소에 접근

```rust
let a = [1, 2, 3, 4, 5];
let nice_slice = &a[1.. 4];
```
`a[start..end]`:

- start = **포함**
- end = **미포함**
- **왼쪽 inclusive**, **오른쪽 exclusive(end-exclusive)**

- `a[0..3]` → 0, 1, 2
- `a[2..5]` → 2, 3, 4
- `a[..3]` → 0, 1, 2 (생략 가능)
- `a[2..]` → 2부터 끝까지

**배열 길이 확인**
```rust
let arr = [1, 2, 3, 4];
println!("{}", arr.len()); // 4
```

## Tuple
여러 타입을 하나로 묶을 수 있는 자료형

**선언**
```rust
let tuple: (i32, f64, bool) = (5, 3.2, true); // 선언
let tuple = (5, 3.2, true); // 타입 생략 ok
```

```rust
let player = ("Kim", 37, 192.5);
```
“Kim” → `&str` , 36 → `i32` , 192.5 → `f64`

```rust
println!("{}", person.0); // "Kim"
println!("{}", person.1); // 37
println!("{}", person.2); // 192.5
println!("{name}, {age}, {height}"); // Kim, 37, 192.5
```
```rust
let (name, age, height) = player;
println!("My favorite volleybal player is {name} and she is {age} years old.");
println!("Her height is {height}cm.");
```
My favorite volleybal player is **Kim** and she is **37** years old.
Her height is **192.5**cm.

```rust
let age = player.1;
assert_eq!(age, 37, "Not equal!");
// assert_eq!(left, right) -> left == right(equal)인지 테스트하는 매크로
```

**빈 튜플(unit type, 아무 것도 반환하지 않)**
```rust
let nothing = ();
```
```rust
// (), 텅 빈 튜플 반환
fn hello() -> () {
    println!("hi");
}
```

```rust
fn return_five() -> i32 {
    // 반환값 테스트
}
```
| **반환값 테스트에 들어가는 코드** | **의미** | **반환값** |
| --- | --- | --- |
| 5 | 표현식 | 5 |
| 5; | 문(statement) | () |
| let x = 5 | 문(statement) | () |
| let x = 5; | 문(statement) | () |
| let x = 5; 5 | statement, expression | 5 |

**튜플 안의 튜플(Nested Tuple)**
```rust
let tuple_test = ((1, 2), ("a", "b"));
println!("{}", tuple_test.0.0); // 1
println!("{}", tuple_test.0.1); // 2
println!("{}", tuple_test.1.0); // "a"
println!("{}", tuple_test.1.1); // "b"
```
