# What is Dart
- Precision - language has to be a optimizer as possible 
- Speed - language has to be minimalist and fast to run
- Tough - language has to be scalable, maintainable and readable
- Modifiable - language has to benefit of fast hot reload
- Popular Framework - language is the foundation of flutter

>[!note] Dart's Technical Envelope
>"*the choices made during development that shape the ==capabilities== and ==strengths== of language*"

## particularities of Dart
-  Dart is type safe 
    - In Compile time : STATIC TYPE CHECK
    - In Run time : RUNTIME CHECK
- Sound Null Safety 
    - variables CAN"T CONTAIN NULL, unless YOU SAY THEY CAN

## Dart Compiler
- Dart uses many Type of compilers for example:
    -  for ARM32 & ARM64 & X86_64 it use:
        - JIT - Just In Time Compiler
            - Compiles just the amount of code it needs 
            - is responsible for **Hot-Reload**
            - dose not recompile the already compiled code if it hasn't changed
            - ==\*== NOT THE BAST, NOR THE MOST OPTIMAL COMILER FOR THE PRODUCTION PHASE
        - AOT - Ahead Of Time Compiler
            - compile the entire source code
            - compile the code into platform specific machine code
            - makes sure the build is the best most optimal version of it
    - for the WEB (JavaScript) it use:
        - dartdevc - Dart Development Compiler
        - dart2js - Dart to JavaScript
- There are allows  two or more stages during development process but allows two which are:
    - DEVELOPMENT PHASE <==> JIT  
        - Easy to test the code
        - Easy to debug the code
        - Live metrics support
        - Fast coding cycles
        - Incremental recompilation
    - PRODUCTIO PHASE <==> AOT
        - App should start fast 
        - App should run fast
        - App doesn't need extra debugging features
        - App doesn't need Hot-Reload anymore
        - App should be compiled into machine code

## What is an Dart SDK
### What is an SDK
    - Software Development Kit 
    - it include : Compilers - Analyzers - Debuggers - Libraries - The Software Framework

### installing the Dart SDK will only allow developing:
    - Command Line Applications
    - server Applications
    - Non-Flutter web Applications
>[!note] As of Flutter 1.21, Flutter SDK incorporates Dart SDK 

### Dart SDK Release Channels
- STABLE CHANNEL
    - suitable for production use
    - updated roughly every 3 months
    - x.y.z; x=major, y=minor, z=patch

- BETA CHANNEL (PREVIEW RELESES)
    - preview builds for the stable channel
    - usually updated every month 

- DEV CHANNEL (PRERELEASES)
    - latest changes, may be broken or unsupported
    - usually updated twice a week

# coding Dart

- Dart is an object oriented programming (OOP) language
    - mostly everything in dart is a  class, and object are instances of these classes
    - 1, 2.0, 'example', [1,2,3], test(), null are **==Objects==**
- Everything you place inside a dart's variable is an **==Object => an instance of a class==**
- Explicit Type annotations are optional, Dart is able to infer types
    - **`var`** Keyword @compile-time
    - **`dynamic`** Keyword @run-time
- Dart is a sound typed system, it can't never evaluate into an unknown state
- Variables can't contain null, unless you say they can
- Dart is an ecosystem based on packages
- Dart packages can depend one on another
- Dart packages use libraries to share code one with another
- Libraries are stored inside the ==lib== folder
- Files outside ==lib== folder are not shared with other packages 


>[!note]- Run Dart Project
>-  using terminal ( dart run ) => the file with the same name of the project name in bin file
>- using Keyboard 
>    - start Debugging ( F5 )
>    - start Without Debugging ( Ctrl+F5 )

## About Dart Project Files 

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/Screenshot.png)

## What is Dart Packages
- Main Component On Dart Ecosystem 
- The Main Packages Manager For The Dart Packages is ==pub package==
- packages include one or more ==LIBRARIES== 
    - Libraries => THE ONLY PART THAT IS ==PUBLICY ACCESSIBLE== TO EVERYONE

## Dart Linting (LINT RULES)

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/Screenshot2.png)

-  The responsible for lint rules in dart is ==analysis_options.yaml== File which came from package named ==pedantic== 
![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/Screenshot3.png)

## PHASE
### DEVELOPMENT PHASE
 - this phase primarily focuses  on the Development and developer experience of:
    - WRITING
    - RUNNING
    - DEBUGGING	
 - Future users of the application won't have any input in side this phase
 - fast & Stable Development Workflow
 - Quick Analyzer & Reformatting tools
 - Fast Compilation & Recompilation
 - Intuitive debugging tools
 - Hot-Reload
 
### PRODUCTION PHASE
- in this phase users only cares about :
    - FAST STARTUP TIME
    - OPTIMIZED AS IT CAN GET
- Focused primarily on the user experience
- fast startup time
- Usefulness, reliability, stability
- Good-lookingness, interactivity
- tasting in real world scenarios

## Dart VM
- the RUNTIME System
- Development Experience components
    - Debugging 
    - Hot-reload
- JIT & AOT Compilation Pipelines 
- Dart VM can Execute Dart apps in 2 WAYS:
    - From source by using JIT/AOT Compiler
    - From SNAPSHOTS (JIT, AOT or Kernel snapshots)

## Effective Dart

>[!note]-  Rules you should take into consideration when coding 
>>1- Be **==ORGANIZED==** & **==CONSISTENT==** with your code
>>>     Code Objectives:
>>>>      - How & When to format
>>>>      - Function & Variable Naming
>>>>      - When you'll Refactor
>>>>      - How to structure the filles & directories
>>
>>
>>2- Write **==MINIMALIST==** & **==SIMPLE TO UNDERSTAND==** code
>>3- Always **==TEST==** your code
>

>[!note]- There are two overarching themes to code DART:
>1- **Be consistent**
>> - When it comes to things like formatting, and casing, arguments about which is better are subjective and impossible to resolve. What we do know is that being _consistent_ is objectively helpful.
>> -  If two pieces of code look different it should be because they _are_ different in some meaningful way. When a bit of code stands out and catches your eye, it should do so for a useful reason.
>>
>
>2- **Be brief**
>> - Dart was designed to be familiar, so it inherits many of the same statements and expressions as C, Java, JavaScript and other languages. But we created Dart because there is a lot of room to improve on what those languages offer. We added a bunch of features, from string interpolation to initializing formals, to help you express your intent more simply and easily.
>> - If there are multiple ways to say something, you should generally pick the most concise one. This is not to say you should [code golf](https://en.wikipedia.org/wiki/Code_golf) yourself into cramming a whole program into a single line. The goal is code that is _economical_, not _dense_.

###  The guides
#### **[Style Guide](https://dart.dev/effective-dart/style)** 
-  This defines the rules for laying out and organizing code, or at least the parts that [`dart format`](https://dart.dev/tools/dart-format) doesn’t handle for you. The style guide also specifies how identifiers are formatted

>[!note]- Identifiers
>>- `UpperCamelCase` names capitalize the first letter of each word, including the first.
>>>- name types
>>>- name extensions
>>> ``` Dart
>>> class SliderMenu { ... }
>>> 
>>> extension MyFancyList<\T> on List<\T> { ... }
>>> 
>>> typedef Predicate<\T> = bool Function(T value);
>>> 
>>> ```
>>- `lowerCamelCase` names capitalize the first letter of each word, _except_ the first which is always lowercase, even if it’s an acronym.
>>>- If the annotation class’s constructor takes no parameters, you might want to create a separate `lowerCamelCase` constant for it.
>>>- name other identifiers
>>> ``` dart
>>> 
>>>const foo = Foo();
>>>
>>>@foo
>>>class C { ... } 
>>>
>>> var count = 3;
>>> 
>>>HttpRequest httpRequest;
>>>
>>>```
>>- `lowercase_with_underscores` names use only lowercase letters, even for acronyms, and separate words with `_`.
>>>- name packages, directories, and source files  
>>>- name import prefixes
>>>``` dart
>>>
>>>my_package
>>>└─ lib
>>>   └─ file_system.dart
>>>   └─ slider_menu.dart
>>>   
>>> import 'dart:math' as math;
>>> import 'package:angular_components/angular_components.dart' as angular_components;
>>> 
>>>   ```
>>- DO format your code using `dart format`
>>- AVOID lines longer than 80 characters
>>- DO use curly braces for all flow control statements
>>> ``` dart
>>> 
>>>if (isWeekDay) {
>>>  print('Bike to work!');
>>>} else {
>>>  print('Go dancing or read a book!');
>>> }
>>> 
>>> ```

#### **[Documentation Guide](https://dart.dev/effective-dart/documentation)** 
- This tells you everything you need to know about what goes inside comments. Both doc comments and regular, run-of-the-mill code comments.

#### **[Usage Guide](https://dart.dev/effective-dart/usage)**
- This teaches you how to make the best use of language features to implement behavior. If it’s in a statement or expression, it’s covered here.

#### **[Design Guide](https://dart.dev/effective-dart/design)**
- This is the softest guide, but the one with the widest scope. It covers what we’ve learned about designing consistent, usable APIs for libraries. If it’s in a type signature or declaration, this goes over it.

### How to read the guides
- **DO** guidelines describe practices that should always be followed. There will almost never be a valid reason to stray from them.
- **DON’T** guidelines are the converse: things that are almost never a good idea. Hopefully, we don’t have as many of these as other languages do because we have less historical baggage.
- **PREFER** guidelines are practices that you _should_ follow. However, there may be circumstances where it makes sense to do otherwise. Just make sure you understand the full implications of ignoring the guideline when you do.
- **AVOID** guidelines are the dual to “prefer”: stuff you shouldn’t do but where there may be good reasons to on rare occasions.
- **CONSIDER** guidelines are practices that you might or might not want to follow, depending on circumstances, precedents, and your own preference.

### Glossary
- A **library member** is a top-level field, getter, setter, or function. Basically, anything at the top level that isn’t a type.
- A **class member** is a constructor, field, getter, setter, function, or operator declared inside a class. Class members can be instance or static, abstract or concrete.
- A **member** is either a library member or a class member.
- A **variable**, when used generally, refers to top-level variables, parameters, and local variables. It doesn’t include static or instance fields.
- A **type** is any named type declaration: a class, typedef, or enum.
- A **property** is a top-level variable, getter (inside a class or at the top level, instance or static), setter (same), or field (instance or static). Roughly any “field-like” named construct.
## Sound Null safety 

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/NullSound.png)

 - Not Having Null Values Where You Don't Expect Them
 - Throws No Null Reference Error, if you're using null safety, with no explicitly unsafe features 
 - All types in null safe dart are non nullable by default !
 - Type are made nullable by postfixing them with the **==question mark (?)==**
 - SDK >= 2.12.0
## Dart Keywords

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/DartKeywords.png)

## Variables

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/variables.png)

### Top level Nullable variables 

```Dart
int? nullableTopLevel; // ture
// int? nullableTopLevel = null; // ture
// int? nullableTopLevel = 5; // ture
nullableTopLevel = 13; // ture
```

### Top level Non-Nullable variables 

```Dart
int nonNullableTopLevel = 5; // ture
nonNullableTopLevel = 13; // ture
int nonNullableTopLevel = null; // false

late int nonNullableTopLevel2; // ture
nonNullableTopLevel2 = 30; // ture
```
 
![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/variables2.png)  

- final vars will have a value known at runtime
- const vars will have a value known at compile time

## Dart Built-in types

>[!question]- What are Dart Built-in types?
>- **the default types will find in dart SDK core folder**


![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/DartBuilt-inTypes.png)

### NUM

- **int**
- **double**

```Dart
int a = 3;
int b =2;
var c = a / b;
var d = a ~/ b;
print(c); // 1.5
print(d); // 1
```

### Strings

- a sequence of UTF-16 code units

```Dart
string s1 = 'Hello, Word';
string s2 = "It's sunny outside";
// string s2 = 'It's sunny outside'; // Error
string s2 = 'It\'s sunny outside';
//----------------------------------------------
double temp = 25.4;
string celcius = 'celcius';
string s4 = 'There are $temp degrees ${celcius.toUpperCase()}';

string a = 'Hello';
sring b = 'Word';
string simpleConcatenation = 'Hello' 'Word'; // in print -> HelloWord
string plusConcatenation = a + b; // in print -> HelloWord

string intro = "Hello, everyone! \n I'm Ahmad, welcome back";
string intro2 = '''Hello, everyone! 
I'm Ahmad, welcome back''';
string rawString = r'Hello, everyone! \n I\'m Ahmad, welcome back';
``` 

### Boolean

```Dart
bool bt = true;
bool bf = false;
```

### Lists

- Lists are Ordered Group Of Objects
- Lists -> collection containing unordered non-unique object

```Dart
List<int> list = [ 1 , 2 , 3 ];
list.forEach(print); // 1 \n 2 \n 3
print(list[0]); // 1
print(list[ list.length - 1 ]); // 3

//----------------------------------------------

List<bool> booleans = [ true, false, false, true ];

//----------------------------------------------

class A{}
List<A> listOfAObjects = [ A(), A() , A() ];

//----------------------------------------------

List<dynamic> listOfIntegersAndDoubles = [ 2 , 3.5 , 7.2 , 9 ];
List<num> listOfIntegersAndDoubles2 = [ 2 , 3.0 , 752 , 9.5 ];
List<object> complexList = [ 2 , 5.7 , 'hello' , true ];
List<object?> complexListWithNullValue = [ 2 , 5.7 , 'hello' , true , null];

//----------------------------------------------

List<int> a = [ 1 , 2 , 3 ];
List<int> b = [...a];

//----------------------------------------------
bool salesActive = true;
List<string> menu = [ 'Home' , 'Store' , 'About' , 'Search' ];
var salesMenu = [ 'Offers1' , 'Offers2'];
List<string> menu = [ 'Home' , 'Store' , 'About' , 'Search' , if(salesActive) 
					 for (var item in salesMenu) item , ];

```

### Dots Operators 

```Dart
// . & ?. used to call functions and operation of mathods
//----------------------------------------------
// .. & ?.. (cascade operator)
List<int> list1 = [ 1 , 0 , 2 ];
list1.sort();
list1 = list1.reversed.toList();
list1.addAll([ 5 , 3 , 4 ]);
list1.sort();
list1 = list1.map((e) => e + 1).toList(); // print [ 1, 2, 3, 4, 5, 6 ]

List<int> list2 = [ 1 , 0 , 2 ]
..sort()
..reversed
..addAll([ 5 , 3 , 4 ])
..sort()
..map((e) => e + 1); // print [ 0, 1, 2, 3, 4, 5 ]
//----------------------------------------------
// ... & ...? (spread operator)

var a = [1,2,3];
var b = [3,4,5];
var c = null;
var d = [ ...a , ...b ]; // print [ 1, 2, 3, 4, 5 ]
var e = [ ...a , ...?c ]; // print [ 1, 2, 3 ]

```

### Sets

- Sets ~= Lists
- sets -> collection containing unordered unique object

```Dart
var set = <int>{};
set.add(1);
set.add(3);
set.add(2);
set.add(3);
print(set); // { 1 , 2 , 3 }
set.addAll({ 4 , 5 , 6 });
//----------------------------------------------
var set1 = Set();
Set<String> set2 = { 'hello' , 'word' };
var set3 = { 1 , 2 , 3};
var set4 = <int>{};
```

### Maps

```Dart
// Map<K,V>
var map1 = {};
var map2 = {
	1:1,
	2:2,
	3:3,
};
var map3 = Map();
map3['key'] = 'value';
map3['hw'] = 'hello word';
```

### Runes

- collection containing all decimal Unicode code points of a string -> integer value uniquely identifying a given Unicode character from inside a string
```Dart
Runes runes = Runes('Hello');
print(runes); // (72 , 101 , 108 , 108 , 111 )
```

### Enum

```Dart
enum e { Sunny , cloudy , Drizzly , Rainy }
```

## Functions

- simple function
```Dart
int first(int a)=> a.isOdd ? 1 : 0;
```

- Anonymous Function
```Dart
void second(int function(int) f, int a){
	print(f.call(a)); // a
	print(f(a)); // a
}

// the anonymous function
second((a) => a , 5);
// or
var list = [ 'hello' , 'everyone' , 'www.com'].map((s) { return s.toUpperCase(); });
```

### Function parameters

- required positional parameters
```Dart
void requiredPositional(int a , int b) => print('$a $b'); 
```
- Optional positional parameters
```Dart
void optionalPositional([int a = 5 , int? b]) => print('$a $b'); 
```
- Required Named parameters
```Dart
void requiredNamed({required int a , required int b}) => print('$a $b');
```
- Optional Named parameters
```Dart
void optionalNamed({int a = 5 , int b = 10}) => print('$a $b');
```
- named Hybrid
```Dart
void namedHybrid({required int a , int b = 10}) => print('$a $b');
```

- mix of Params
```Dart
void mixOfParams(int a , int b , {required int c}){};
```

```Dart
void mixOfParams(int a , int b ,  [int d = 5]){};
```

### lexical Scope

```Dart
viod a(){
	var aVar = 5;
	// bVar = 7; // Error
	// cVar = 20; // Error
	
	void b(){
		var bVar = 8;
		aVar = 10; // no Error
		// cVar = 40; //Error
		
		void c(){
			var cVar = 12;
			aVar = 50; //no Error
			bVar =30; //no Error
		}
	}
}
```

>[!question]- How to call a class like calling a Function
>```Dart
>class A{
>void call() => print("I'm a function! :) ");
>}
>var a =A();
>a();
>// OR
>A()();
>```


## Dart Operators

- Operators are num Functions

 ![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/Operators.png)

- using Operators => creating Expressions

### Arithmetic Operators

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/arithmeticOperators.png)

```Dart
var a = 5;
// a1 = a, then a = a + 1;
var a1 = a++;
print(a1); // 5
//----------------------------------------------
// a = a + 1, then a2 = a;
var a2 = ++a;
print(a2); // 7
//----------------------------------------------
var b = 5;
// a1 = a, then a = a - 1;
var b1 = b--;
print(b1); // 5
//----------------------------------------------
// a = a - 1, then a2 = a;
var b2 = --b;
print(b2); // 3
```


### Equality & Relational Operators

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/equality&relationalOperators.png)

```Dart
int a = 2;
int b = 2;
print( a == b ); // true
print(identical(a , b)); // true
//----------------------------------------------
var list1 [ 1 , 2 , 3 ];
var list2 [ 1 , 2 , 3 ];
print( list1 == list2 ); // false cos: it's not const value
print(identical(list1 , list2)); // false
```

### Type test Operators

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/typeTestOperators.png)

```Dart
import 'dart:math' as math;
```

```Dart
var list = [1 , 2.5 , 'test' , null];
var i = list[0] as int;
var d = list[0] as double;
var s = list[0] as string;
var n = list[0] as null;
```

```Dart
var list = [1 , 2.5 , 'test' , null]..forEach((element){
if(element is int){
	print('$element is of int type');
}else if(element is double){
	print('$element is of double type');
}else if(element is string){
	print('$element is of string type');
}else if(element is null){
	print('$element is of null type');
}
});
```

### Assignment Operators

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/assignmentOperators.png)

```Dart
int? a;
print(a); //null
a ??= 5;
print(a); // 5
```

```Dart
int a = 1;
// a++; // a = a+1;
// ++a; // a = a+1;
//----------------------------------------------
// what if i want => a = a + 3;
a += 3;
//----------------------------------------------
var a1 = a += 3; // 4
var a2 = a -= 3; // 1
var a3 = a ~/= 3; // 0
var a4 = a *= 3; // 0
```

### Logical Operators

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/logicalOperators.png)

```Dart
var a = 5;
if( a.isEven && a .isFinite || a.isNegative){}
//----------------------------------------------
var isFalse = !(true); // print false
```

### Bit Operators

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/bitOperators.png)

```Dart
var a = 6; // 0110
var b = 5; // 0101

print( a & b ); // 0100 = 4
print( a | b ); // 0111 = 7
print( a ^ b ); // 0011 = 3
print( a << 1 ); // 1100 = 12
print( a >> 1 ); // 0011 = 3
print( ~a ); // -7
```

### Conditional Expression

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/conditionalExpression.png)

```Dart
class Car{
	final string name;
	Car(this.name);
}
//----------------------------------------------
Car rewardCar(Car? dreamCar) => dreamCar != null ? dreamCar : Car('Random');
```

## Control Flow Statements

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/controlFlowStatements.png)

### if/else statements
```Dart
bool b = true;
if(b){
	print('true');
} else{
	print('false');
}
//----------------------------------------------
if(b){
	print('true');
} else if( b == false ){
	print('false');
} else{
	print('null');
}
//----------------------------------------------
b ? print('true') : print('false');
```

### loops statements

- For 
```Dart
var list = [ 1 , 2 , 3 , 4 , 5 ];
for(var i = 0; i < list.length; i++){
	print( list[i] );
}
//----------------------------------------------
for( var item in list ){
	print( list[i] );
}
//----------------------------------------------
list.forEach(print);
//----------------------------------------------
var list2 = [ 11 , 22 , 33 , 44 , 55 ]..forEach(print);
//----------------------------------------------
```

- While
```Dart
// (while) won't enter the loop if i > 5 
int i = 0;
while( i < 5 ){
	print(i);
	i++;
}
//----------------------------------------------
// (do/while) will have one iteration before exiting the loop 
do{
	print(i);
	i++;
} while( i < 5 );
```

### Break/Continue Statements

- break => exit the loop
- continue => skip the current loop
```Dart
var list = [ 1 , 2 , 3 , 4 , 5 ];
for( var item in list ){
	if( item == 3 ){
	break;
	}else{
	print(list[i]);
	}
}
//----------------------------------------------
for( var item in list ){
	if( item == 4 ){
	continue;
	}else{
	print( list[i] );
	}
}
//----------------------------------------------
var list2 = [ 11 , 22 , 33 , 44 , 55 ].where((element) => element != 4)..forEach(print);
```

### Switch Statements

```Dart
var condition = 'Sunny';
switch (condition) {
	case 'Sunny':
	print('It\'s Sunny');
	break;
	case 'cloudy':
	print('It\'s cloudy');
	break;
	case 'Drizzly':
	print('It\'s Drizzly');
	break;
	case 'Rainy':
	print('It\'s Rainy');
	break;
	default:
	print('It\'s Sunny');
}
```

### assert Statements

- work only on debug mode 
- work only of the condition is false

```Dart
var list = [];
assert(list.isNotEmpty, 'list must not be empty!');
```

### Exceptions 

- try
- throw
- catch
- finally

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/exceptions.png)

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/exceptions2.png)

```Dart
try{
// some code that may throw exception
	throw Exception;
}catch(exception){
// some code that handles the thrown exception
// to rethrow the exception for some reason
	rethrow;
} finally{
// code while be executed no matter what  
}
```

## Classes

- Empty class 
```Dart
class A {}
```

### Instance

**instance variables <==> Fields**

#### Instance Variables
```Dart
class A {
	int? _private;
//----------------------------------------------
	int? a;
	int b = 1;
//----------------------------------------------
	final int c =2;
//----------------------------------------------
	late int d;
	late final int e;
	late final int f =5;
//----------------------------------------------
	static int g =6;
	static late int h;
	static late int i = 8;
	static late final int j;
//----------------------------------------------
	static const int k =10;
}
//----------------------------------------------
void main(){
	var alfa = A();
	
	print('alfa._privat; --> ${alfa._private}');
	
	print('alfa.a --> ${alfa.a}'); // null
	print('alfa.b --> ${alfa.b}'); // 1
	print('alfa.c --> ${alfa.c}'); // 2
	
	alfa.d = 3;
	print('alfa.d --> ${alfa.d}'); // 3
	
	alfa.e = 4;
	print('alfa.e --> ${alfa.e}'); // 4
	
	print('alfa.f --> ${alfa.f}'); // 5
	print('alfa.g --> ${A.g}'); // 6
	
	A.h = 7;
	print('alfa.h --> ${A.h}'); // 7
	print('alfa.i --> ${A.i}'); // 8
	
	A.j = 9;
	print('alfa.j --> ${A.j}'); // 9
	print('alfa.k --> ${A.k}'); // 10
}
```

- any instance variables you create inside a class will have a default getter method
- any non-final fields & late final fields will have a default setter methods

### Custom Constructor
    - **Note** => constructor have no return type
```Dart
class A {
	// A(); // empty constructor
	
	A(int p, int a, int b, int d, int e, int f){
	_private = p;
	this.a = a;
	this.b = b;
	this.d = d;
	this.e = e;
	this.f = f;
	}
	
	// OR
	
	A(int c, int h) : this.c = c, this.h = h;
	
	// OR
	
	A(
	this._private;
	this.a;
	this.b;
	this.d;
	this.e;
	this.f;
	);
	
	// OR
	
	A(
	this._private;
	this.a;
	this.b;
	this.e;
	this.f;
	) : d = b;
	
	// OR
	
	A(
	this._private;
	this.a;
	this.b;
	this.e;
	this.f;
	) : d = b{
	d = b;
	}
	
	// OR
	
	// Note => nullable variables don't need to be required 
	// Note => private variables can't be Optional parameters
	A(this._private,{
	
	this.a,
	required this.b,
	required this.c,
	required this.d,
	required this.e,
	required this.f,
	});
	
//----------------------------------------------
	int? _private;
//----------------------------------------------
	int? a;
	int b = 1;
//----------------------------------------------
	final int c =2;
//----------------------------------------------
	late int d;
	late final int e;
	late final int f =5;
//----------------------------------------------
	static int g =6;
	static late int h;
	static late int i = 8;
	static late final int j;
//----------------------------------------------
	static const int k =10;
}
```

### Named Constructor
```Dart
class A{
	// default constructor
	A({
	required this.x;
	required this.y;
	});
	
	// named constructor
	
	A.zero(): x = 0, y = 0;
	// in call => var alfaZero = A.zero();
	
	A.fromJson({required Map<String, int> json}) : x = json['x']!, y = json['y']!;
	// in call => var alfaFromJson = A.fromJson(json: {'x': 5, 'y': 10});
	
	final int x;
	final int y;
}
```

### Redirecting Constructor

```Dart
class A{
	// default constructor
	A({
	required this.x;
	required this.y;
	});
	
	// named constructor
	A.zero(): x = 0, y = 0;
	// in call => var alfaZero = A.zero();
	
	// redirecting constructor
	A.zeroX({required int y}) : this(x: 0, y: y);
	A.zeroY({required int x}) : this(x: x, y: 0);
	
	final int x;
	final int y;
}
```

### Factory Constructor

- constructor that can return a value
```Dart
class A {
	A({
	required this.x;
	required this.y;
	});
	
	factory A.random({
	required bool isPositive}){
	int minNegativeValue = -90;
	int maxNegativeValue = -1;
	int minPositiveValue = 0;
	int maxPositiveValue = 99;
	
	int randomNegativeValue =
	 minNegativeValue + Random().nextInt(maxNegativeValue - minNegativeValue);
	int randomPositiveValue =
	 minPositiveValue + Random().nextInt(maxPositiveValue - minPositiveValue);
	
	return isPositive
	? A(x: randomPositiveValue, y: randomPositiveValue)
	: A(x: randomNegativeValue, y: randomNegativeValue);
	}
	
	factory A.explanation() => return A.random(isPositive: true);
	
	final int x;
	final int y;
}
```

### Singleton Pattern

```Dart
class Singleton {
	Singleton._privateConstructor();
	static final Singleton _instance = Singleton._privateConstructor();
	factor Singleton() => _instance;
}
```

### Getters & Setters

```Dart
class A{
	A({
	required this.x;
	required this.y;
	});
	
	final int x;
	// int get x => x;
	final int y;
	// int get y => y;
	late int age;
	
	int get sum => x + y;
	int get diff => x - y;
	
	set yourAge(int value) => age = 2023 - value;
	// to call yourAge
	var a = A(x: 0, y: 0);
	a.yourAge = 2003;
	print('yourAge : ${a.age}');
}
```

### Static Methods

```Dart
class A{
	A({
	required this.x;
	required this.y;
	});
	
	final int x;
	final int y;
	
	static distanceBetween(A a1, A a2){
	var dx = a1.x - a2.x;
	var dy = a1.y - a2.y;
	return asrt(pow(dx, 2) + pow(dy, 2));
	}
}
```

### Inheritance

- everything you create will be an object instantiated from a class
- everything class you create will inherit, by default, the object class

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/inheritance.png)

```Dart
class Animal{
	final String name;
	Animal({required this.name});
	void whatAmI() => print('I\'m an animal!');
	Animal.fromJson() : name = 'Jerry';
	}
	
	class Bird extends Animal{
	Bird(String name) : super(name : name);
	// Bird(String name) : super.fromJson();
	}
	class Duck extends Bird{
	Duck(String name) : super(name);
	// override functions is a Polimorphism
	@override
	void whatAmI() => print('I\'m an duck!');
	void swim() {}
}
```

```Dart
class Animal{
	final String name;
	Animal({required this.name});
	void whatAmI() => print('I\'m an animal!');
	// Animal.fromJson() : name = 'Jerry';
	void chase(Animal a){}
	
	external void doSomething();
	}
	class Mouse extends Animal{
	Mouse() : super(name: 'Jerry');
	
	@override
	void doSomething(){
	// TODO: implement doSomething
	super.doSomething();
	}}
	class Cat extends Animal{
	Cat() : super(name: 'Tom');
	@override
	void chase(covariant Mouse m){}
}
```

### Abstraction

- abstraction classes
- abstraction methods
- interfaces
- in dart, there are no explicit interface use abstract classes to declare interfaces
- the extends keyword shares behavior of base to the derived class, the implements keyword forces behavior of interfaces to derived class

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/abstraction.png)

```Dart
abstract class UserRepositoryInterface{
	late final List<int> userList;
	
	void create();
	List<int> read();
	void update();
	void delete();
}

class UserRepository implements UserRepositoryInterface{
	@override
	late final List<int> userList;
	
	UserRepository(){
	userList = read();
	}
	@override
	void create() => print('created!');
	
	@override
	void update() => print('updated!');
	
	@override
	void delete() => print('deleted!');
}
```

### Mixins 

- a class of which behavior can be shared with other classes

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/mixin.png)

- simple mixin
```Dart
mixin A{
	void method1(){}
	void method2(){}
	void method3(){}
}

class B with A{
	@override
	void method1(){
	// TODO: implement method1
	super.method1();
	}

	@override
	void method2(){
	// TODO: implement method2
	super.method2();
	}
}
```

- example on mixin
```Dart
class Performer{
	void performer() => print('Performing...');
}

mixin Guitarist{
	void playGuitar() => print('playing the guitar');
	void perform() => playGuitar();
}

mixin Drummer{
	void playDrums() => print('playing the drums');
	void perform() => playDrums();
}
class Musician extends Performer with Guitarist, Drummer{}

void main(){
	Musician musician = Musician();
	musician.perform(); // will print => 'playing the drums'
	musician.playDrums();
	musician.playGuitar();

}
```
    - if class Musician extends :

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/mixins.png)

- 
```Dart
class Performer{
	void performer() => print('Performing...');
}

mixin Guitarist{
	void playGuitar() => print('playing the guitar');
	void perform() => playGuitar();
}

mixin Drummer{
	void playDrums() => print('playing the drums');
	void perform() => playDrums();
}
class Musician with Guitarist, Drummer{}

void main(){
	Musician musician = Musician();
	musician.perform(); // will print => 'playing the drums'
	musician.playDrums();
	musician.playGuitar();
}
```
    - if class Musician don't extends :

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/mixins2.png)

- 
```Dart
class Performer{
	void performer() => print('Performing...');
}

mixin Guitarist on Performer{
	void playGuitar() => print('playing the guitar');
	void test() => perform();
	void test2() => super.perform();
}

mixin Drummer{
	void playDrums() => print('playing the drums');
	void perform() => playDrums();
}
class Musician extends Performer with Guitarist, Drummer{}

void main(){
	Musician musician = Musician();
	musician.test(); // will print => 'playing the drums'
	musician.tes2t(); // will print => 'Performing...'
}
```

    - if you use the 'on' keyword with mixin you must extends the class :

```Dart
mixin Guitarist on Performer{}
```

```Dart
class Musician extends Performer with Guitarist, Drummer{}
```

### Extensions

```Dart
extension IntegerExtension on int{
	int get lukyInteger => 12;
}
```

## Generics

- generics can be used in classes and methods
- generics make everything more ==**abstract**==, more ==**universal**,== more ==**widely-compatible**==

### Keywords
- <**E**> = Elements
- <K, V> = Key, Value
- <**T**> = Type
- <**S**> = source
- <**R**> = Return

### Examples

- Example generic class
```Dart
class Tuple<E>{
	final E? _a;
	final E? _b;
	final E? _c;
	
	E? get first => _a;
	E? get second => _b;
	E? get third => _c;
	
	const Tuple(this._a, this._b, this._c);
	Tuple.fromList(List<E> list) :
	 _a = list.asMap().containsKey(0) ? list[0] : null,
	 _b = list.asMap().containsKey(1) ? list[1] : null,
	 _c = list.asMap().containsKey(2) ? list[2] : null;
	
	Tuple<num> operator +(Tuple<num> t) { 
		if(this is Tuple<num>){
			final thisAsTupleNum = this as Tuple<num>;
			return Tuple(
				thisAsTupleNum._a! + t._a!,
				thisAsTupleNum._b! + t._b!,
				thisAsTupleNum._c! + t._c!,
				);
		}
		return const Tuple(0, 0, 0);
	}
	Tuple<num> operator -(Tuple<num> t) { 
		if(this is Tuple<num>){
			final thisAsTupleNum = this as Tuple<num>;
			return Tuple(
				thisAsTupleNum._a! - t._a!,
				thisAsTupleNum._b! - t._b!,
				thisAsTupleNum._c! - t._c!,
				);
		}
		return const Tuple(0, 0, 0);
	}
	
	
	@override
	String toString() => 'Tuple(first: $first, second: $second, third: $third)';
}

void main(){
	const t1 = Tuple(1, 2, 3);
	const t2 = Tuple(4, 5, 6);
	const t3 = Tuple(1, "2", 3);
	const t3 = Tuple('a', 'b', 'c');
	const t5 = Tuple(Object(), Object(), Object());
	final t6 = tuple.fromList(['Hello','I','am','ahmad']);
	const tSum1 = t1 + t2;
	const tSum2 = t3 + t2;
	const tDiff = t1 - t2;
	const tDiff2 = t3 - t2;
	
	print('tSum --> $tSum '); // tSum --> Tuple(first: 5, second: 7, third: 9)
	print('tSum2 --> $tSum2 '); // tSum --> Tuple(first: 0, second: 0, third: 0)
	print('tDiff --> $tDiff '); // tDiff --> Tuple(first: -3, second: -3, third: -3)
	print('tDiff --> $tDiff '); // tDiff --> Tuple(first: 0, second: 0, third: 0)
}
```

    - if you want to generic a specific type in a general type
```Dart
class tuple<E extends num>{}
// this will only accept int,double
```

- Example 2 generic class
```Dart
class Stack<T>{
	final List<T> _stack = [];
	
	T get peak => _stack.last;
	int get length => _stack.length;
	bool get canPop => _stack.isNotEmpty;
	
	T pop(){
		final T last = _stack.last;
		_stack.removeLast();
		return last;
	}
	
	void push(T value) => _stack.add(value);
}

void main(){
	var stackInt = Stack<int>();
	var stackString = Stack<String>();
	
	stackInt.push(1);
	stackInt.push(2);
	stackInt.push(3);
	stackInt.push(4);
	stackInt.pop();
	print(stackInt.peak); // will print => 3
	
	stackString.push('1');
	stackString.push('2');
	stackString.push('3');
	stackString.push('4');
	if(stackString.canPop){ StackString.pop(); }
	print(stackString.peak); // will print => '3'
}
```

- Example generic method
```Dart
class Utils{
	static T? getItem<T>(List<T> list, int index) => 
		list.asMap().containsKey(index) ? list[index] : null;
}

void main(){
	var list = ['a', 'b'];
	print(Utils.getItem(list, 1)); // will print => 'b'
}
```

>[!question]- **When & Why You Should Use Generic Types?**
>1- the When : you need to implement data structures of your own
>>```Dart
>>class Stack<\T>{
>>	final List<\T> _stack = [];
>>	
>>	T get peak => _stack.last;
>>	int get length => _stack.length;
>>	bool get canPop => _stack.isNotEmpty;
>>	
>>	T pop(){
>>		final T last = _stack.last;
>>		_stack.removeLast();
>>		return last;
>>	}
>>	
>>	void push(T value) => _stack.add(value);
>>}
>>```
>
>1- the Why:  you won't have to reimplement the same class for each type
>2- the When: some portions of your code are kind of repetitive: 
>>```Dart
>>// bad ✕
>>void main(){
>>	final result1 = (((a + b) / 2) *  1 / 3) % 4;
>>	final result2 = (((a + b) / 2) *  1 / 3) % 4;
>>	final result3 = (((a + b) / 2) *  1 / 3) % 4;
>>	final result4 = (((a + b) / 2) *  1 / 3) % 4;
>>}
>>// good ✓
>>double calculate<\T extends num>(T a, T b)
>> 	=> (((a + b) / 2) *  1 / 3) % 4;
>>
>>void main(){
>>	final result1 = calculate(1, 2);
>>	final result2 = calculate(5.4, 4.2);
>>	final result3 = calculate(5, -3.6);
>>	final result4 = calculate(74.3, 82);
>>}
>>```
>



## Libraries

- every Dart file you create is by default a new library
![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/libraries.png)

## Synchronous & Asynchronous

### introduction

- Dart Isolate => the component in which the dart code runs

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/synchronous&asynchronous.png)

>[!question]- When running an application, does Dart spawn only one isolate?
> YES, is only spawns one isolate called "main"

>[!question]- What is it going to happen if the event loop has to calculate a really complicated expression?
>Is there a solution to this limitation?
>- YES, there is, it's called Parallelism 
>- however, there is a drawback, creating multiple isolates is resource intensive  

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/synchronous&asynchronous2.png)

- Microtasks events have a higher priority compared to future events 
```Dart
void main(){
	print('A');
	Future((){
		print('B');
		Future(() => print('C'));
		Future.microtask(()=> print('D'));
		Future(() => print('E'));
		print('F');
		});
	print('G');
}
// what will be printed is => AGBFDCE
```

### Synchronous

- synchronous => a task that needs to be solved before proceeding to solving the next one

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/synchronous.png)

>[!question]- ITERABLE VS LIST
>**ITERABLE :**
>>- much more as abstract collection
>>- it is constructed lazily  => when an element is accessed 
>>- it is traversed with the help of an iterator(curr, nextItem())
>>- it doesn't need to have a specified length
>>- Accessing an element with regenerate all elements until the desired one is found
>
>**List :**
>>- Special non-lazily Iterable => constructed as soon it's called
>>- Has defined size and items are stored at a specific index

    - Iterables are lazy-loaded
    - Iterables generate just the right amount of item they need
```Dart
Iterable<int> showGenerator(int n) sync* {
	print('Generator started');
	for(var i = 1; i <= n; i++){
		print('i -> $i');
		yield i;
	}
	print('Generator end');
}
void main(){
	final a = showGenerator(10); 
	// if you only call this line nothing will happend, you have to access some of the atreputes in 
	// the Iterable to print or do what it should do, like next :
	print('a.last --> ${a.last}'); 
	print('a.first --> ${a.first}'); 
}
```
- the output : 

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/iterable.png)

    - to call Iterable inside anther Iterable yp should use 'yield*'
```Dart
Iterable<int> showNegativeGenerator(int n) sync* {
	print('Negative Generator started');
	for(var i = 1; i <= n; i++){
		print('-i -> ${-i}');
		yield i;
	}
	print('Negative Generator end');
}
Iterable<int> showGenerator(int n) sync* {
	print('Generator started');
	for(var i = 1; i <= n; i++){
		print('i -> $i');
		yield i;
	}
	yield* showNegativeGenerator(n);
	print('Generator end');
}
void main(){
	var generated = showGenerator(10); 
	print('generated.last --> ${generated.last}'); 
}
```
- the output : 

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/iterable2.png)


### Asynchronous

- asynchronous => a task that doesn't needs to be solved before proceeding to processing the next one
![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/asynchronous.png)

- Future Example 1
```Dart
void main(){
	print('Start');
	
	Future(() => 1).then(print);
	Future(() => Future(() => 2)).then(print);
	
	Future.delayed(const Duration(seconds: 1), () => 3).then(print);
	Future.delayed(const Duration(seconds: 1), () => Future(() => 4)).then(print);
	//[Note]-> Future.delayed(Duration.zero, () => x) == Future(() => x)
	
	Future.value(5),then(print);
	Future.value(Future(() => 6)).then(print); // == Future(() => 6)
	
	Future.sync(() => 7).then(print); // == Future.value(7)
	Future.sync(() => Future(() => 8)).then(print); // == Future(() => 8)
	
	Future.microtask(() => 9).then(print);
	Future.microtask(() => Future(() => 10)).then(print); 
	//Future.microtask(() => (){}) == Future(() => 10), but placed on microtask queue
	
	Future(() => 11).then(print);
	Future(() => Future(() => 12)).then(print);
	
	print('End');
}
```
- the output : 

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/asynchronous2.png)

- Future Example 1
```Dart
void main(){
	print('1');
	scheduleMicrotask(() => print('2'));
	
	Future(() => print('4')).then((_) => print('5')).then((_) {
		print('6');
		scheduleMicrotask(() => print('7'))
	}).then((_) => print('8'));
	
	scheduleMicrotask(() => 9);
	
	Future(() => print('10')).then((_) => Future(() => print('11')))
	.then((_) => print('12'));
	
	Future(() => print('13'));
	scheduleMicrotask(() => print(14));
	print('15');
}
```
- the output : 

![](https://raw.githubusercontent.com/Ahmad-alnahal/Dart-Tutorial/main/images/asynchronous3.png)

- Future with await Example 1
```Dart
Future main() async {
late finel int a;

print('Start');

await Future(() => 1).then((value) => a = value);
//OR
a = await Future(() => 1);

print(a);
print('End');
}
```

- Stream Example 1
```Dart
Stream.periodic(const Duration(seconds: 1), (x) => x).listen(print);

Stream.fromFutures([Future(() => 3), Future.value(2)]).listen(print); // will print -> 2 3
```

- Stream Example 2
```Dart
void main(){
	final StreamController streamController = StreamController<int>();
	// final StreamController streamController = StreamController<int>().brodcast();
	// brodcast() used if you want to use multiple streamSubscription 
	final streamSubscription = streamController.listen(print);
	
	var vallue = 0;
	Timer.periodic(const Duration(seconds: 1), (timer){
		if(value == 5){
			timer.cancel();
			streamController.close();
			streamSubscription.cancel();
		}else{
		streamController.add(value++);
		}
	});
}
```

- Stream Example 3
```Dart
Future main() async{
	final StreamController streamController = StreamController<int>();
	
	var vallue = 0;
	Timer.periodic(const Duration(seconds: 1), (timer){
		if(value == 5){
			timer.cancel();
			streamController.close();
		}else{
		streamController.add(value++);
		}
	});
	
	var max = 0;
	await streamController.stream.forEach((value){
		max = (value > max)? value : max;
	});
	print('Max is --> $max');
}
```

- Stream Example 4
```Dart
void main(){
	asyncGenerator().listen(print);
}

var negativeStream = Stream<int>.periodic(const Duration(milliseconds: 500), (x) => -x);

Stream<int> asyncGenerator() async*{
	for(var i = 0; i < 5; i++){
		await Future<void>.delayed(const Duration(seconds: 1));//=> will print every second from 1_4
		yield i;
	}
	yield* negativeStream;//after print from 1-4 will print from -1 _ -endless
}
```