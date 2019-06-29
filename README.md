# Hello-World
Brainstorming

4 challenges completed so far (3 good ones)

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

