# fly-with-go

🐹 go is the language I want to 🛶 conquer next 🌍.

<p>
  <img src='./images/go.gif' height=200 />
  <img src='./images/cat.gif' height=200 />
  <img src='./images/joker.gif' height=200 />
  <img src='./images/deadpool.gif' height=200 />
</p>

<h2 id="home">🏷️ contents</h2>

- #### [🛴 basic](#basic)

  - ##### [🖨️ printing](#printing)

  - ##### [🔫 function](#function)

  - ##### [🌳 variable](#variable)

  - ##### [🥚 basic types](#basic-types)

  - ##### [🚂 type conversion](#type-conversion)

  - ##### [🍭 loop](#loop)

  - ##### [👻 conditional statement](#conditional-statement)

  - ##### [🎣 defer](#defer)

- #### [🚀 advanced](#advanced)

- #### [📙 documents](#documents)

- #### [🚧 license](#license)

<h2 id="basic">🛴 basic</h2>

<h3 id="printing">🖨️ printing</h3>

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

**[⬆️ back to top](#home)**

<h3 id="function">🔫 function</h3>

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

**[⬆️ back to top](#home)**

<h3 id="variable">🌳 variable</h3>

```go
package main

import "fmt"

// global variables
var canFly bool
var age int = 21

func main() {
  // explict
  var name string = "Cuong Duy Tran Nguyen"
  // inferred
  var job, address = "Software Engineer", "Ho Chi Minh city"
  // shorthand
  gender := "male"
  // constant
  const homeTown = "Tam Ky city, Quang Nam province"
	fmt.Println(canFly, name, age, job, address, gender, homeTown)
}
```

**[⬆️ back to top](#home)**

<h3 id="basic-types">🥚 basic types</h3>

```
bool

string

int  int8  int16  int32  int64
uint uint8 uint16 uint32 uint64 uintptr

byte // alias for uint8

rune // alias for int32
     // represents a Unicode code point

float32 float64

complex64 complex128
```

```go
package main

import "fmt"

func main() {
	var (
		name string = "Cuong Duy Nguyen"
		age int = 21
	)
	fmt.Printf("type: %T, value: %v\n", name, name)
	fmt.Printf("type: %T, value: %v\n", age, age)
}
```

**[⬆️ back to top](#home)**

<h3 id="type-conversion">🚂 type conversion</h3>

```go
package main

import (
	"fmt"
	"math"
)

func main() {
	var z uint = uint(math.Sqrt(64))
	var i int = 7
	var f float64 = float64(i)
	fmt.Print(z, i, f)
}
```

**[⬆️ back to top](#home)**

<h3 id="loop">🍭 loop</h3>

```go
package main

import "fmt"

func main() {
	for i := 0; i < 7; i++ {
		fmt.Println(i)
  }
  // for continued
  max := 0
	for ; max < 7777 ; {
		max += 7
	}
  fmt.Println(max)
  // while
  sum := 0
	for sum < 777 {
		sum += 7
	}
  fmt.Println(sum)
  // forever
  for {
		fmt.Println("go")
	}
}
```

**[⬆️ back to top](#home)**

<h3 id="conditional-statement">👻 conditional statement</h3>

```go
package main

import (
  "fmt"
  "runtime"
  "time"
)

func compare(x, y int) (z string) {
	if x > y {
		z = "x is greater than y"
	} else {
		z = "x is smaller than y"
	}
	return
}

func isEven(number int) bool {
	if num := number % 2; num == 0 {
		return true
	}
	return false
}

// switch case
func checkOS() string {
	switch os := runtime.GOOS; os {
		case "linux":
			return "🐧 Linux"
		case "darwin":
			return "🌌 macOS"
		default:
			return os
	}
}
// switch case without condition
func showGreeter() string {
	h := time.Now().Hour()
	switch {
		case h < 12:
			return "good morning"
		case h < 17:
			return "good afternoon"
		default:
			return "good evening"
	}
}

func main() {
	t := compare(6, 7)
  fmt.Println(t)
  fmt.Print(isEven(7))
  fmt.Print(checkOS())
  fmt.Println(showGreeter())
}
```

**[⬆️ back to top](#home)**

<h3 id="defer">🎣 defer</h3>

> A defer statement defers the execution of a function until the surrounding function returns.

> Deferred function calls are pushed onto a stack. When a function returns, its deferred calls are executed in last-in-first-out order.

```go
package main

import "fmt"

func main() {
	fmt.Println("counting")

	for i := 0; i < 10; i++ {
		defer fmt.Println(i)
	}

	fmt.Println("done")
}
```

**[⬆️ back to top](#home)**

<h2 id="advanced">🚀 advanced</h2>

<h2 id="documents">📙 documents</h2>

- #### 🦊 [golang.org](https://golang.org/)

- #### 🦌 [A Tour of Go](https://tour.golang.org)

- #### 🐧 [Golang for Node.js Developers](https://github.com/miguelmota/golang-for-nodejs-developers)

- #### 🐠 [Golang Tutorial  from zero to hero](https://milapneupane.com.np/2019/07/06/learning-golang-from-zero-to-hero/)

- #### 🐳 [Go Cheat Sheet](https://github.com/a8m/golang-cheat-sheet)

<h2>🚧 license</h2>

MIT © [cuongw](https://github.com/cuongw)
