```
/**
 * @param {string} haystack
 * @param {string} needle
 * @return {number}
 */
var strStr = function(haystack, needle) {
    if(needle == ""){
    return 0;
  }
  if(needle.length > haystack.length){
    return -1;
  }
  if(haystack == needle){
    return 0;
  }
  let resultIndex = -1;
  let haystackPointer = 0;
  let nPointer = 0;

  while(haystackPointer < haystack.length){
    if(nPointer == needle.length){
      return resultIndex;
    }
    if(haystack[haystackPointer] == needle[nPointer]){
      nPointer++
      if(resultIndex == -1){
        resultIndex = haystackPointer;
      }
    }
    else if((haystack[haystackPointer] != needle[nPointer] ) && resultIndex != -1){
      nPointer = 0;
      haystackPointer = resultIndex;
      resultIndex = -1;      
    }
    haystackPointer++
  }
  if(nPointer == needle.length){
    return resultIndex
  }
  return -1;
};

```