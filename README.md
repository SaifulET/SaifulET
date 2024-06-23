
// 1. summation of two numbers
function summation(a,b){
    return a+b;
}
let sum= summation(4,5);
console.log(sum);

// 2. Identify a number whether it Even or Odd
function EvenOrOdd(a){
    if(a%2==0)
        return true;
    else 
        return false;
}
let number = EvenOrOdd(5);
console.log(number);

// 3.Maximum Number 
function maxNumber(arr){
    let i=1;
    let max=arr[0];
    while (i<arr.length){
        if(max<arr[i]){
            max=arr[i];
        }
        i++;
    }
    return max;
}
let AnArray=[60,4,3,5,23,53];
console.log(maxNumber(AnArray));

// 4.Reverse string 

function ReverseString(str){
    let arr=str.split("");
    let arrrev =arr.reverse();
    return arrrev.join("");
}
let AnStr="Saiful";
console.log(ReverseString(AnStr));

// 5.filter odd numbers 
function filterOddNumber(arr){
    const odds=[];
    arr.forEach(e=> {
        if(e%2!=0){
            odds.push(e);
        }
    });
    return odds;
}
let AnArry=[2,4,5,6,2,9,0,1];
console.log(filterOddNumber(AnArry));


// 6.sum of array 
function sumarray(arr){
    let sum=0;
    arr.forEach(e => {
        sum+=e;
    });
    return sum;
}
let anarray=[2,3,4,5,6,7];
console.log(sumarray(anarray));

// 7.sort an array 
function sortanarray(arr){
    for(let i=0;i<arr.length;i++){
        for(let j=0;j<arr.length;j++){
            if(arr[i]<arr[j])
                {
                    let c=arr[i];
                    arr[i]=arr[j];
                    arr[j]=c;
                }
        };
    };
    return arr;
}
let anarry=[4,2,53,42,5,1];
console.log(sortanarray(anarry));

// 8.capitalized first letter 
function capFirstLetter(arr){
    arr =arr.charAt(0).toUpperCase()+ arr.slice(1)
    return arr;
}
let anstr="saiful";
console.log(capFirstLetter(anstr));
