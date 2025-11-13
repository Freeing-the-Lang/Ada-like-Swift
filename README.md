# Ada-like-Swift

Swift 문법을 **Ada 스타일의 정형 언어(Formal Language)**로 재해석하는 실험 프로젝트입니다.  
이 리포는 Swift 코드를 의미 기반(semantic)으로 분석하여 Ada 규칙에 맞는 구조로 변환하는 **트랜스파일 개념 언어**를 목표로 합니다.

---

## 🎯 목표

- Swift의 문법적 간결함 + Ada의 안정성 모델 결합
- 함수·타입·컨트롤 구조를 Ada식으로 재해석
- Pure-Rust-No-LLVM 기반 트랜스파일러 설계
- 정형적 타입 체크, 명시적 오류 모델
- Multi-main 실행 모델 실험
- 3OS 자동 빌드 및 ProofLedger 기반 메타데이터 생성

---

## 📐 Swift → Ada 매핑 규칙 (예시)

| Swift 요소 | Ada 스타일 해석 |
|-----------|----------------|
| `func` | `procedure` 또는 `function` |
| `let` | `constant` |
| `var` | `variable` |
| `class` | `tagged type` |
| `struct` | `record` |
| `enum` | `variant record / tagged union` |
| `import` | `with <package>; use <package>;` |
| 옵셔널(Optional) | 명시적 nullable 타입 또는 discriminated union |
| 프로토콜(protocol) | Ada interface 또는 tagged type hierarchy |

이 표는 프로젝트가 진행되면서 확장됩니다.

---

## 🔧 예제

### Swift 코드
```swift
func add(_ a: Int, _ b: Int) -> Int {
    return a + b
}



Ada-like-Swift 해석 형태


function Add (A : Integer; B : Integer) return Integer is
begin
    return A + B;
end Add;




📁 디렉토리 구조 (예정)


src/
  tokenizer.swift
  parser.swift
  semantics.rs
  transpiler.rs
examples/
  hello.swift
  math.swift
  control.swift

proof/
  proofledger.txt (자동 생성 예정)
  sha256/




⚙️ 빌드 & 자동화 (예정)




GitHub Actions를 통한 3OS 빌드



Ubuntu / macOS / Windows






빌드 산출물:



변환된 Ada 코드


ProofLedger


SHA256 검증 파일






태그 자동 생성 및 릴리즈 자동 업로드





📌 로드맵




[ ] Swift 토크나이저


[ ] 구문 파서


[ ] AST → Ada 변환기


[ ] 타입 시스템 정의


[ ] 의미 기반 에러 모델


[ ] Multi-main 런타임


[ ] 3OS CI/CD + ProofLedger 자동화





📝 라이선스


MIT License



💬 기여


아이디어, 코드, 테스트 케이스 어떤 형태든 기여 환영합니다.



---
