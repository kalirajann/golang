# golang

Install golang in your machine
Install go extenstion VS code

package main

import "fmt"

func main() {
	fmt.Println("Hello World")
}

### How to run: 

go build {filename} - creates the executable
go run {filename} - runs the file

package {name}- assiociated executable 
        2 types - execuatable or reusable

main is keyword for execuatble.
other names - reusable

package main -> build -> main.exe   (main func must be defined for main)
package abcd -> build -> nothing




### fmt (standard library)

used to act as bride to get the access to other libraies such as debug, math, encoding, io, crpto

### Package Info

golang.org/pkg

### variables

Go - Static Type like Java, C# & unlike dynamic types such as Javascript, python

**Basic Types:**
bool
int
string
float64


go can determine the type of variable itself.

2 ways of variable declaration.
	var card string = "Ace of Spades"
	card1 := "Initialization go itself detemines the data type"
  
  
Reassignment
	card1 = "Reassigning"
  
  
Variables can be initialized outside of a function, but cannot be assigned a variable.
  
### Simulation link

https://play.golang.org/


### Function

	card := newCard()
	fmt.Println(card)


func newCard() string {
	return "Five of Diamonds"
}


### Slices and Loops

Array - Fixed length of list
Slice - Array that can grow or shrink. items be same datatypes

cards := []string{newCard(), "card2"}

	cards = append(cards, "card3")

	for i, card := range cards {
		fmt.Println(i, card)
	}
  
  func newCard() string {
	return "Five of Diamonds"
}



### Custom Type & receiver

//Custom Type
	cards1 := deck{newCard(), "card2", "card3"}
	cards1.print()
	
//on other file	
type deck []string

//(d deck) - receiver
func (d deck) print() {
	for i, card := range d {
		fmt.Println(i, card)
	}
}
