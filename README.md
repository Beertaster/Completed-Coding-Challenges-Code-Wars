# Hello-World

6 challenges completed



__________________________________________
7 kyu
Isograms
JavaScript:

// string first coverted to lower case so that same letters of different cases would not slip through.
function isIsogram(str){
  var lower = str.toLowerCase();
  var isIso = true;
  if(str.length == 0) {
    isIso = true;
  }else{
    for(var i = 0; i < str.length; i++) {
      for(var j = i+1; j < str.length; j++) {
        if(lower[i] == lower[j]) {
          isIso = false;
          break;
        }
      }
    }
  }
  return isIso;
}
_________________________________________
7 kyu
Get the Middle Character
JavaScript:

  function getMiddle(s)
{
// In this if statment we check whether the median is a whole number
  if (s.length % 2 == 0) { 
  // Arrays start ar 0 not 1 thus (s.length) is the higher of the two medians and (s.length) - 1 is the lower.
    return s[(s.length / 2) - 1] + s[s.length / 2];
    // Again because arrays start at zero.
    // So an array of seven characters would have the 4th character in slot 3. Meaning Math.Floor would round down 3.5 to the median array slot. 
    } else { return s[Math.floor(s.length / 2)]; }
}
__________________________________________

7 kyu
Regex validate PIN code
JavaScript:

function validatePIN (pin) {
// because the 96 tests get weird I'm explicitely stating the allowed characters
 let  nums = '0123456789' 

  for ( let i = 0; i < pin.length; i++) {
     let elem = pin[i]
     if ( nums.indexOf(elem) === -1) { //this is a wonderful method call to check against invalid characters
       return false
     }
  }
  if ( pin.length === 4 || pin.length === 6) {  
    return true
  }  else { return false}
}
// Being able to use method calls is wonderful, just look at the mess that is my java attempt.
____________________________________________
Instructions: Given an array. Add the first three numbers in the array together to create the fouth and so on like fibinachi but with the lat three numbers instead of the last two. All arrays on numbers, or nothing. return the result.

function tribonacci(signature,n){
  var triarray = [];
  //if(signature.length < 3){
  //this is when I would throw an error, but the if/else stmt should be throwing back the invalid arrarys like the instructions asked.
    //return signature;
    //
  //}else{
  triarray[0] = signature[0], triarray[1] = signature[1],triarray[2] = signature[2];
  for(var i=3; i < n; i++){
    triarray[i] = triarray[i-1] + triarray[i-2] + triarray[i-3];
  }
  //for(var j=0; j < triarray.length; j++){
    //signature[j] = triarray[j];
  //}
  
  // didn't know javascript had such elegant slice code. Loved learning about this.
  return (n < 3) ? signature.slice(0, n) : triarray;
//}
}
_____________________________________
6 kyu
Consecutive strings
JavaScript:

//This code takes the first longest string in an array and concatonates it with k number of consecutive strings after the chosen string.

function longestConsec(strarr, k) {
// First get the array length and a default value for our result
  var n = strarr.length;
  result = ''
// Create an if statement first to catch errors from any invalid k
  if (n === 0 || k > n || k <= 0) {
    return "";
  }
// Then find the largest string and concatonate with k strings after.
  for (var i= 0; i < n; i++) {
    var cS = strarr.slice(i, k + i).join('');
    if (cS.length > result.length) {
      result = cS;
    }
  }
  return result;
}
_______________________________________

6 kyu
Take a Ten Minute Walk
C#:

//The input must be verified to be of length 10 and that the commands will return to the beginning
// variables are used to mimic a coordinate plane and an if statment test for a valid input length.

public class Kata
{
  public static bool IsValidWalk(string[] walk)
  {
    int x = 0;
    int y = 0;
    int z = 0;
    for(int i=0; i < walk.Length; i++) {
      if( walk[i] == "n") {
        y+= 1;
        }
        else if (walk[i] == "s") {
          y-= 1;
          }
        else if (walk[i] == "w") {
          x-= 1;
          }
        else{
            x+= 1;
            };
    };
    if ( x == 0 && y == 0) {
      z = 0;
      }
      else {
      z = 1;
      }
    if ( z == 0 && walk.Length == 10) {
      return true;
      }
      else {
      return false;
      };
  }
}
_________________________________________________

