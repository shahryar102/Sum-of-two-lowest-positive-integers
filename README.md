# Sum-of-two-lowest-positive-integers
function sumTwoSmallestNumbers(numbers){
  array=[]
  for (i=0;i<numbers.length;i++){
    if(Number.isInteger(numbers[i])&&numbers[i]>0){
      array.push(numbers[i])}
  }  
   if (array.length<4) {console.log('Enter atleast for positive entegers inside array[]'); return}
  let lowest1=array[0], lowestIndex=0, array2=[];
  for(i=1;i<array.length;i++){
    if(array[i]<lowest1){lowest1=array[i]}
  } 
  for(i=0;i<array.length;i++){
    if(array[i]==lowest1){lowestIndex=i}
  }
  for(i=0;i<array.length;i++){
    if(!(i==lowestIndex)){array2.push(array[i])}
  }
  let lowest2=array2[0]
  for(i=1;i<array2.length;i++){
    if(array2[i]<lowest2){lowest2=array2[i]}
  } 
  console.log(`Lowest number is ${lowest1} and second lowest numbers is ${lowest2} and their sum is ${lowest1+lowest2}`)
  return lowest1+lowest2
}
sumTwoSmallestNumbers([5,8,1,4,9,3])
