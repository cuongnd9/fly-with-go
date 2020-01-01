# fly-with-go

🐹 go is the language I want to conquer next.

<p>
  <img src='./images/gopher.png' height=250 />
  <img src='./images/cat.gif' height=250 />
  <img src='./images/joker.gif' height=250 />
</p>

## 🏷️ contents

- #### [🛴 basic](#basic)

- #### [🚀 advanced](#advanced)

  - ##### [🖨️ printing](#printing)

  - ##### [🔫 function](#function)

- #### [📙 documents](#documents)

<h2 id="basic">🛴 basic</h2>

<h4 id="printing">🖨️ printing</h4>

```go
package main

import (
  "fmt"
  "math"
)

func main() {
  fmt.Println("Hello %s", "🐹 Go")
  fmt.Println(math.Pi)
}
```

<h4 id="function">🔫 function</h4>

```go
package main

import "fmt"

func add(a int, b int) int {
  return a + b
}

func subtract(a, b int) int {
  return a - b
}

func swap(a, b int) (int, int) {
  return b, a
}

// named return values
func split(number int) (a, b int) {
	a = number / 10
	b = number % 10
	return
}

func main() {
  fmt.Println(add(6,9)) // 15
  fmt.Println(subtract(17, 10)) // 7
  a, b := swap(10, 17)
  fmt.Println(a, b) // 17 10
  fmt.Println(split(19)) // 1 9
}
```

<h2 id="advanced">🚀 advanced</h2>

<h2 id="documents">📙 documents</h2>

#### 🦊 [golang.org](https://golang.org/)

#### 🦌 [A Tour of Go](https://tour.golang.org)

#### 🐧 [Golang for Node.js Developers](https://github.com/miguelmota/golang-for-nodejs-developers)

#### 🐠 [Golang Tutorial  from zero to hero](https://milapneupane.com.np/2019/07/06/learning-golang-from-zero-to-hero/)
