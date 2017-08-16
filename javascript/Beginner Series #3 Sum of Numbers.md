#



### Solution

### 1

```js
function GetSum( a,b )
{
   if(a!==b)
   		{
      	var x=0;
      	if(b<a)
        	{
          		a=a+b;
              b=a-b;
              a=a-b;
          }
      		while(a<=b)
          {
          	x=x+a;
            a++;
          }
          return x;
      }
   return a;   
}
```
### 2

```js
const GetSum = (a, b) => {
  let min = Math.min(a, b),
      max = Math.max(a, b);
  return (max - min + 1) * (min + max) / 2;
}
```