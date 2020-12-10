# kbSimpleArray
this is a simple JavaScript class.

*how to use?
  1)first add this line in your html file
  <script src="https://cdn.jsdelivr.net/gh/Kosala167/kbSimpleArray/simple-array.min.js" defer></script>
  
  2)then try simple example like below one
  
  //first make object using your array //here it is [1, 2, 3, 5, 7]
  
  let x = new ArrayReader([1, 2, 3, 5, 7]);
  
  //then you can use methods like 'x.readArray(callback)' , 'x.arrMap(callback)' , 'x.filteredArray(callback)'
  //call back function like function testFunction(index,value){console.log("index is:"+index+" and value is : "+value);}
  
  x.readArray((index, value) => console.log(`${index}:${value}:${(value%2===0)?'even':'odd'}`));
  
  let newArray = x.arrMap((index, value) => { return value * index });//arrMap make new array from your callback function
  new ArrayReader(newArray).readArray((index, value) => console.log(`${index}:${value}`));
  
  let filteredArray = x.arrFilter((index, value) => { return value > 5 || value < 2 });//filteredArray make new array from your callback functions condition
  new ArrayReader(filteredArray).readArray((index, value) => console.log(`${index}:${value}`));
