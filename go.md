# Go Cheat Sheet

## CLI Tools

`go test -cover`

`go test -race`

`go vet`

## Features

```go
func SumAllTails(numbersToSum ...[]int) {...}
```

```go
add := func(x,y int) {
    return x + y
}
```

```go
sliceOfStructs := []struct {
    name string
    age int
} {
    {"Amir", 39},
    {"Kippi"}, 5},
}
```

```go
type Result struct {
    string
    bool
}
```

```go
time.After(duration)
// VS
for range time.Tick(time.Second) {
    // do it once a sec
}
```

```go
fmt.PrintF("%T %#V ...")
```

```go
`This is a
Multiline string`
```

```go
type Person struct {
    Name string
}

type Student struct {
    Person
    StudentId string
}
```

```go
type StudentId = string
// VS
type StudentId string
```

```go
fmt.Printf("My name is %[1]s and I'm %[2]d years old!\n\n", "Amir", 39)
```

```go
func do(i interface{}) {
	switch v := i.(type) {
	case int:
		fmt.Printf("Twice %v is %v\n", v, v*2)
	case string:
		fmt.Printf("%q is %v bytes long\n", v, len(v))
	default:
		fmt.Printf("I don't know about type %T!\n", v)
	}
}

func main() {
	do(21)
	do("hello")
	do(true)
}
```

```go
numbers := [10]int{0,1,2,3,4,5,6,7,8,9}
s := numbers[1:4:5]
fmt.Println(s) // [1, 2, 3]
fmt.Println(cap(s)) // 4
```
