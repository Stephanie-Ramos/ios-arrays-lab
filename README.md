# Arrays Lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.

# Part 1

## Question 1

Create an array of strings called `colors` that contain "orange", "red", "yellow", "turquoise", and "lavender".

Then, using array subscripting and string interpolation, print out the String `"orange, yellow, and lavender are some of my favorite colors"`.
```swift
let colors = ["orange", "red", "yellow", "turquoise", "lavender"]
```

answer: 
```swift
print("\(colors[0]), \(colors[2]), \(colors[4]) are some of my favorite colors")
```

## Question 2

Remove "Illinois" and "Kansas" from the array below.

`var westernStates = ["California", "Oregon", "Washington", "Idaho", "Illinois", "Kansas"]`

answer:
```swift
westernStates.remove(at: 5)
westernStates.remove(at: 4)
print(westernStates)
```

## Question 3

Iterate through the array below. For each state, print out the name of the state, a colon, and whether it is or is not **in the continental United States.**  

`let moreStates = ["Hawaii", "New Mexico", "Alaska", "Montana", "Texas", "New York", "Florida"]`  

answer: 
```swift
for state in moreStates {
    if state == moreStates[0] || state == moreStates[2]{
        print("\(state) is not in the contient of the United States")
    } else {
        print("\(state) is in the contient of the United States ")
    }
}
```

## Question 4

Print out how many non-whitespace characters are in `myString`:

`let myString = "This is good practice with Strings!"`

answer: 
```swift 
let formattedMyString = myString.replacingOccurrences(of: " ", with: "")
print(formattedMyString.count)
```

Iterate through the array below. For each sentence, print out how many non-whitespace characters are in it.

`let myFavoriteQuotes = ["To be or not to be, that is the question.", "The only source of knowledge is experience.", "Mr. Gorbachev, tear down this wall!", "Four score and twenty years ago..."]`

answer:
```swift
var i = 0
repeat {
    print(myFavoriteQuotes[i].replacingOccurrences(of: " ", with: "").count)
    i += 1
} while i < myFavoriteQuotes.count
```

## Question 5

Iterate through `garden` and place any 🌷 that you find into the `basket`. Replace any 🌷 that you pick up with `"dirt"`. Then print how many 🌷 are in your `basket`.

```swift
var garden = ["dirt","🌷","dirt","🌷","dirt","dirt","🌷","dirt","🌷","dirt"]
var basket = [String]()
```

answer:
```swift
var w = 0
repeat {
    if garden[w] == "🌷" {
        basket.append("🌷")
    }
    print(garden[w].replacingOccurrences(of: "🌷", with: "dirt"))
    w += 1
} while w < garden.count
print(basket.count)
```

## Question 6

The below array represents an unfinished batting lineup for a baseball team. **You, the coach,** need to make some last minute changes:

- Add "Suzuki" to the end of your lineup.
- Change "Jeter" to "Tejada".
- Change "Thomas" for "Guerrero"
- Put "Reyes" to bat 8th instead.

`var battingLineup = ["Reyes", "Jeter", "Ramirez", "Pujols","Griffey","Thomas","Jones", "Rodriguez"]`

answer: 
```swift
battingLineup.append("Suzuki")
battingLineup[1] = "Tejada"
battingLineup[5] = "Guerrero"
battingLineup.swapAt(0, 7)
print(battingLineup)
```

## Question 7

Given an array of Ints, find out if it contains a target number.  

(The built-in `contains(_:)` function will do this, but you aren't allowed to use it for this exercise.)
 
```swift
var numbers: [Int]

let target: Int = 32
```

Ex.1

```swift
numbers = [4,2,6,73,32,4,2,1]

target = 32

//true
```

Ex. 2

```swift
numbers = [32459,2,4,5,1,4,2,1]

target = 3

//false
```

answer:
```swift
var contains = numbers.filter{$0 == target}
print(contains)
```

## Question 8

Find the largest value in an array of Int.  Do not use the built-in `max()` method.

```swift
let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}

//This creates an array of 100 numbers in between 0 and 200. For now, you don't need to worry about how it does that.
```

answer:
```swift
var maxNumberArray:Int = 0
for number in arrayOfNumbers where number >= maxNumberArray {
maxNumberArray = number
}
print("The max number in the array is \(maxNumberArray)")
```

## Question 9

Find the smallest value in an array of Int.  Do not use the built in min() method.

```swift
let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}

//This creates an array of 100 numbers in between 0 and 200.  For now, you don't need to worry about how it does that.
```

answer:
```swift
var minNumberArray:Int = 200
for number in arrayOfNumber where number <= minNumberArray {
    minNumberArray = number
}
print("The min number in the array is \(minNumberArray)")
```

## Question 10

Iterate through `secondListOfNumbers`, and print out all the odd numbers.

`var secondListOfNumbers = [19,13,14,19,101,10000,141,404]`

answer:
```swift
var secondListOfNumbers = [19,13,14,19,101,10000,141,404] //print out all the odd numbers
for counter in 0...7 where secondListOfNumbers[counter] % 2 == 1{
    print(secondListOfNumbers[counter])
}
```

## Question 11

Iterate through `thirdListOfNumbers`, and print out the sum.

`var thirdListOfNumbers = [11, 26, 49, 61, 25, 40, 74, 3, 22, 23]`

answer:
```swift
let total = thirdListOfNumbers.reduce(0, +)
print(total)
```

## Question 12

Iterate through `thirdListOfNumbers`, and print out the sum of all the even numbers.

`var thirdListOfNumbers = [11, 26, 49, 61, 25, 40, 74, 3, 22, 23]`

answer:
```swift
var sum = 0
for counter in 0...9 where thirdListOfNumber[counter] % 2 == 0 {
    sum += thirdListOfNumber[counter]
}
print("The sum is \(sum)")
```

## Question 13

Append every Int that appears in both `listOne` and `listTwo` to the `sharedElements` array. Then print **how many Ints** are shared.

```swift
var listOne = [28, 64, 7, 96, 13, 32, 94, 11, 80, 68]
var listTwo = [18, 94, 48, 6, 42, 68, 79, 76, 13, 7]
var sharedElements = [Int]()
```

answer:
```swift
sharedElements = listOne + listTwo
print(sharedElements.count)
```

# Part 2

## Question 1

Write code such that `noDupeList` has all the same Ints as `dupeFriendlyList`, but has no more than one of each Int.

```swift
var dupeFriendlyList = [4,2,6,2,2,6,4,9,2,1]
var noDupeList: [Int] = []
```

answer:
```swift
noDupeList = dupeFriendlyList
let list = Set(noDupeList)
print(list)
```
## Question 2

Find the second smallest number in an Array of Ints

`let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}`

answer:
```swift
let sorted = arrayOfNumbers.sorted()
let secondSmallest = sorted[1]
```

## Question 3

If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.

Find the sum of all the multiples of 3 or 5 below 1000.

answer:
```swift
var n = 0
for number in 0...1000 where number % 3 == 0 || number % 5 == 0 {
    n += number
}
print("The sum of all multiples of 3 and 5 below 1000 is \(n)")
```

## Question 4

Make an array that contains all elements that appear **more than twice** in `someRepeatsAgain`.

```swift
var someRepeatsAgain = [25,11,30,31,50,28,4,37,13,20,24,38,28,14,44,33,7,43,39,35,36,42,1,40,7,14,23,46,21,39,11,42,12,38,41,48,20,23,29,24,50,41,38,23,11,30,50,13,13,16,10,8,3,43,10,20,28,39,24,36,21,13,40,25,37,39,31,4,46,20,38,2,7,11,11,41,45,9,49,31,38,23,41,16,49,29,14,6,6,11,5,39,13,17,43,1,1,15,25]
```

answer:
```swift 
var repeatsAgain = [Int]()
var a = 0
for x in someRepeatsAgain {
    for y in someRepeatsAgain {
        if x == y {
            a += 1
        }
        if a > 2 {
            repeatsAgain.append(y)
            break
        }
    }
    a = 0
}
repeatsAgain = Array(Set(repeatsAgain))
print(repeatsAgain.sorted())
```

## Question 5

Identify if there are 3 integers that sum to 10 in the following array. If so, print them as a triplet. If there are multiple triplets, print all possible triplets.

`var tripleSumArr = [-20,-14, -8,-5,-3,-2,1,2,3,4,9,15,20,30]`

answer: 
```swift
var triplets = [Array<Int>]()
for x in tripleSumArr {
    for y in tripleSumArr {
        for z in tripleSumArr{
            if x + y + z == 10 {
                triplets.append([x, y, z])
            }
        }
    }
}
print(Set(triplets)) 
```

## Question 6

Given an array of Strings, find the the String with the most "a"s in it.

input: `["apes", "abba", "apple"]`

output: `"abba"`

answer: 
```swift
var array = Array<String>()
var counterTwo = 0
var counterOne = 0
var most = ""

for word in array {
    for char in word {
        if char == "a" {
            counterOne += 1
        }
    }
    if counterOne > counterTwo {
        most = word
    }
    counterTwo = counterOne
    counterOne = 0
}
print(most)
```

## Question 7

Given an Array of Arrays of Ints, find the Array of Ints with the largest sum:

Input: `[[2,4,1],[3,0],[9,3]]`

Output: `[9,3]`

answer: 
```swift
var arrayOfInts = [[2,4,1],[3,0],[9,3]]
var largest = 0
var largestArray = [Int]()

for array in arrayOfInts {
    let sum = array.reduce(0, +)
    if sum > largest {
        largest = sum
        largestArray = array
    }
}
print(largestArray)
```

## Question 8

Given an Array of Tuples of type `(Int, Int)`, create an array containing all the tuples where the first Int is equal to the second Int.

Input: `[(4,2), (-3,-3), (1,1), (3,9)]`

Output: `[(-3,-3), (1,1)]`

answer:
```swift
var arrayOfTuples = [(4,2), (-3,-3), (1,1), (3,9)]
var repeatingTuples = [(Int, Int)]()
for tuple in arrayOfTuples {
    if tuple.0 == tuple.1{
        repeatingTuples.append(tuple)
    }
}
print (repeatingTuples)
```

## Question 9

Given an Array of Bools, make a variable called `allAreTrue` that is true if all of the Bools are true and false if any of them are false.

Input: `[true, false, true, true]`

Output: `false`

answer: 
```swift
var arrayOfBools = [true, false, true, true]
var allAreTrue : Bool = true

if arrayOfBools.contains(false) {
    allAreTrue = false
    
}
```

## Question 10

Given an Array of Ranges of Ints, create an array that has all the values from all the ranges in order from smallest to greatest with no duplicates.

Input: `[0..<3 , 2..<10, -4..<6, 13..<14]`

Output: `[-4,-3,-2,-1,0,1,2,3,4,5,6,7,8,9,10,13]`

answer: 
```swift
var array = [Int]()
var input = [0..<3 , 2..<10, -4..<6, 13..<14]
for i in input {
    for each in i {
        array.append(each)
    }
}
```

## Question 11

Given an array of Characters, create a String ignoring uppercase Characters and spaces.  Then uppercase every other character of the String.

Input: `let arr: [Character] = ["a", "p","P","l","E"," ","S","a","u","C,"e"]`

Output: `"ApLeAuE"`

answer: 
```swift
let arr: [Character] = ["a", "p","P","l","E"," ","S","a","u","C","e"]
var arrString = ""
for index in 0..<arr.count {
    if arr[index] != " " && String(arr[index]) == String(arr[index].lowercased()) {
        if index % 2 != 1 {
            arrString += String(arr[index]).uppercased()
        } else {
            arrString += String(arr[index])
        }
    }
}
print (arrString)
```

## Question 12

Print out each element in `myMatrix`

`var myMatrix = [[10, 14, 12], [91, 1, 9], [31, 3, 21]]`

answer:
```swift
for element in myMatrix {
    print(element)
}
```

## Question 13

Print out the sum of the diagonals of `myMatrix`.

`var myMatrix = [[10, 14, 12], [91, 1, 9], [31, 3, 21]]`

answer: 
```swift
var n = myMatrix.count
var sum = 0
for i in 0..<n {
    sum += myMatrix[i][i]
    sum += myMatrix[i][n - i - 1]
}
print("The sum of the diagonals \(sum)")
```

## Question 14

Using for loops, rotate `matrixToRotate` 90 degrees.

var matrixToRotate = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

![Matrix Rotation](images/rotated_matrix.jpeg)

answer: 
```swift
var matrixResult = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
var n = matrixToRotate.count

for i in 0..<n {
    for j in 0..<n {
        matrixResult[j][n - i - 1] = matrixToRotate[i][j]
    }
}
print(matrixResult)
```
