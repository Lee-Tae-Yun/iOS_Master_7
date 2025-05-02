# 📘 Day 5 Today I Learned - 문법 학습 시작!

## ✅ 함수의 사용방법 이해하기

### ✨ 함수 사용의 장점
- 🔄 재사용 가능 - 한 번 작성한 함수를 여러 번 호출할 수 있습니다.
- 👀 가독성 향상 - 코드의 목적을 명확히 설명할 수 있습니다.
- 🔧 유지보수 용이 - 특정 기능을 수정할 때, 함수를 수정하면 전체 코드에서 반영됩니다.

---

## 📍 반환 값이 있는 함수

함수가 특정 연산을 수행한 후, 결과를 반환하는 형태

```swift
func multiply(a: Int, b: Int) -> Int {
    return a * b
}

let result = multiply(a: 5, b: 3)
print(result) // 15 출력
```
`a`와 b를 곱한 후 결과값을 반환(`return`)합니다.

## 📍 여러 개의 매개변수를 받는 함수

```swift
func introduce(name: String, age: Int) {
    print("제 이름은 \(name)이고, 나이는 \(age)살입니다.")
}

introduce(name: "Tom", age: 25)
```

---

### 과제

### 두 수를 더하는 함수 만들기
```swift
func addNumbers(num1: Int, num2: Int) -> Int {
    return num1 + num2
}

var num1: Int, num2: Int
print("두수를 입력하세요 ex) 1 2 : ", terminator: "")
var input = readLine() ?? ""
var numbers = input.split(separator: " ")
num1 = Int(numbers[0]) ?? 0
num2 = Int(numbers[1]) ?? 0

var reslut: Int = addNumbers(num1: num1, num2: num2)
print("입력된 수 : \(num1), \(num2) \n두 수의 합 : \(reslut)")
```

### 두수를 비교하는 함수 만들기
```swift
// 두 수를 비교하는 함수 만들기
func numbersComparison(num1: Int, num2: Int) -> Int {
    if num1 > num2 {
        return num1
    }
    else {
        return num2
    }
}

var num1: Int, num2: Int
print("두수를 입력하세요 ex) 1 2 : ", terminator: "")
var input = readLine() ?? ""
var numbers = input.split(separator: " ")
num1 = Int(numbers[0]) ?? 0
num2 = Int(numbers[1]) ?? 0

var reslut: Int = numbersComparison(num1: num1, num2: num2)
print("입력된 수 : \(num1), \(num2) \n더 큰수 : \(reslut)")

```

### 평균 계산 함수 만들기
```swift
// 평균 계산 함수 만들기
func calculateAverage(score1: Int, score2: Int, score3: Int) -> Double {
    let sum = score1 + score2 + score3
    let avg: Double = Double(sum)/3.0
    
    return avg
}

var score1: Int, score2: Int, score3: Int
print("세 개의 수를 입력하세요 ex) 1 2 3 : ", terminator: "")
var input = readLine() ?? ""
var numbers = input.split(separator: " ")
score1 = Int(numbers[0]) ?? 0
score2 = Int(numbers[1]) ?? 0
score3 = Int(numbers[2]) ?? 0

var reslut: Double = calculateAverage(score1: score1, score2: score2, score3: score3)
print("입력된 수 : \(score1), \(score2), \(score3) \n평균 값 : \(reslut)")

```

### 구구단 출력 함수 만들기
```swift
func printMultiplicationTable(_ number:Int){
    for i in 1...9{
        print("\(number) * \(i) = \(number*i)")
    }
}

var input = readLine() ?? ""
var number: Int = Int(input) ?? 0

printMultiplicationTable(number)
```

### 가위바위보 게임 만들기
```swift
func getComputerChoice() -> String {
    let choices = ["Scissors", "Rock", "Paper"]
    return choices.randomElement()!
}

func determineWinner(userChoice: String, computerChoice: String) -> String{
    if userChoice == computerChoice{
        return "Draw!"
    }
    else if userChoice == "Scissors" && computerChoice == "Paper" ||
                userChoice == "Rock" && computerChoice == "Scissors" ||
                userChoice == "Paper" && computerChoice == "Rock" {
            return "You Win!!"
    }
    else {
        return "You Lose Try again!"
    }
}

var input = ""
while true{
    print("Please choose and enter Rock, Scissors or Paper.(Type ‘Stop’ to exit the game.)")
    input = readLine() ?? ""
    if input == "Stop"{
        print("End the game")
        break
    }
    let userChoice = input
    let computerChoice = getComputerChoice()
    let result = determineWinner(userChoice: userChoice, computerChoice: computerChoice)
    print("사용자: \(userChoice), 컴퓨터: \(computerChoice)")
    print(result)
}
```

