# PortfolioWebsite
Basic Portfolio Website Using HTML,CSS,JAVASCRIPT Basically A start to The Web Dev Journey.
JAVASCRIPT NOTES YOU MUST KNOW FOR BASIC IMPLEMENTATION.
PRINT - console.log(x)-prints x in the output.

WORD VS KEYWORD
Word -         It has no meaning in the language.
like :- babu, sona, ghoda, kida, rajesh, ramesh. 
 KeyWord -      It has some meaning in the language 
like :- for, var, int. 

VARIABLE AND CONSTANT 
Variable :- the value assigned can be change further. 
Constant :- the value once assigned cannot be changed.


HOISTING:-
WE can use the Variable before initialization this is bcoz the initialization
part is seperated and placed at the top by default by javascript.

var a=12; initialization+declaration
then it'll be divided like
var a; this is placed at top of the code //initialization
a=12;//declaration 


UNDEFINED & NOT DEFINED 
UNDEFINED:- Exists but does not have any value.
NOT DEFINED:- Does not exist.


Types in javascript
1. PRIMITIVE :- a value whic if we copy get copied really is primitive
var a=[1,2,3,4];[]{}()-primitive else -reference
var b=a;


2  REFERENCE :- a value if we copy that it doesnot get actually  copied
but the reference of its main value gets copied is called a reference value. 


CONDITIONAL:- if,else,else-if.
if(){

}else{

}

LOOP:- for(var i=0;i<11;i++){
    console.log(i);
}


FUNCTION:- to reuse code to use same code with diff. data.
function abcd(a,c,b){
    console.log(a,b,c;)
}
abcd(12,13,14);
var a=[1,2,3,4,5]
ARRAY- push -add element
      pop()- remove element from last;
      unshift()-add element in start;
      shift()-remove element in start;
      splice(index)-remove particular index; 
OBJECT - 1.BlANK OBJECT-  var a={};
         2. FILLED OBJECT- var a={
            age:24, --property
            name:kartik,
            phone:909999;
            method: function{}{}
         }
         a.name ----OUtput - kartik.
for update:- a.name ="Kartik Kumar".


var        -es5 
let, const -es6
var - is function scoped can be used anywhere in parent 
function like :-

for(var i=0;i<12;i++){
    console.log(i);
}
console.log(i); 

the VAR i : -can be used here bcoz its var can be used 
anywhere in parent function.

BUT BUT BUT !!!!

for(let i=0;i<12;i++){
    console.log(i);
}
console.log(i);

let- it is braces scoped cannot use outside braces.
sp console.log(i) will not print anything will give error.

window - js doesnt have some things which we use in code we get from 
browser all those features which are not part of js but we can use them
and search for them into a object called window.

* Var adds itself to window. but let & const dont.
we get var a=12 added on window openly it exposes our data
so its not good then let wo introduced to solve this problem.


Browser Context API -1 Window
                     2 Stack
                     3 Heap Memory - Program Data is stored in heap Memory.


# EXECUTION CONTEXT- Jab bhi hum fuction chalaenge fnc apna ek 
imaginary container bana lega jismein uski teen
cheezien hogi:
1) Variables.(var a)
2)Functions inside that parent function. (function def() )
3)Lexical Environment:-Tell that what sort of things our function can access
or not access.it holdes function scopes and scope chain. 
This container is known as exuction Context.
ex-
functiona abcd(){
    var a=12;
    fuction def(){
        var b =12;
    }
}


#HOW TO COPY REFERENCE VALUES-
SPREAD OPERATOR -COPY VALUE OF ONE TO ANOTHER 
1. var a=[1,2,3,4,5]
var b=[...a]
console.log(b) = [1,2,3,4,5]
2. var obj= {name:"harsh"}
var copyobj={...obj};
change property copyobj.name="harshita";
obj= "harsh"


#TRUTHY AND FALSY
FALSY- 0 False undefined null NaN document.all
TRUTHY- all values else tham falsy values.
if(7){
    console.log("not");
}else{
    console.log("not")
}

var a=[1,2,23,34,34,4,23,4,3,45,54,3,23]

a.forEach(function(val){
    console.log(val+2);
})

for-Each never change the original array by default it 
makes changes in temporary array,,array remains same.


#FOR-IN To LOOP on objects 
var obj={
    name:"harsh",
    age:24,
    city:"Bhopal"
}

for(var key in obj){
    console.log(obj[key]);  output-harsh 
                                   24
                                   Bhopal
}


//CallBack Function 
jab bhi koi aisa code jo baad m chlta h js ko 
yeh pata hi hota ki wo complete hua ki nhi 
aise code k completion par js ko bataya jata hai ki wo complete
hogya aur aap use chla skte ho ye batane ka kam callback ka h

setTimeout(function(){
    console.log("After 2 seconds);
},2000);
run after 2000 miliseconds


#First class Functions
here we can use function as a value(Variable).
1. var a=function(){};
function sbcs(a){

}
sbcs(fuction(){console.log("hey");})


#Arrays in JS behind the scene
1. Arrays are object in javascript
js convert this var arr=[1,2,3,4]; into
arr{
    0:12;
    1:23;
    -1:12;//-ve index can't be used in an array in any
    other language but n js array is object we can do anything.
}
Now if botha re object then how to check whether it is an array
Array.isArray([])---true
Array.isArray({})--false

var a={
    name:"harsh";
    age:21
}
delete a.age;
