# Who likes it?

You probably know the "like" system from Facebook and other pages. People can "like" blog posts, pictures or other items. We want to create the text that should be displayed next to such an item.

Implement a function likes :: [String] -> String, which must take in input array, containing the names of people who like an item. It must return the display text as shown in the examples:

### Examples:

  -  likes [] // must be "no one likes this"
  -  likes ["Peter"] // must be "Peter likes this"
  -  likes ["Jacob", "Alex"] // must be "Jacob and Alex like this"
  -  likes ["Max", "John", "Mark"] // must be "Max, John and Mark like this"
  -  likes ["Alex", "Jacob", "Mark", "Max"] // must be "Alex, Jacob and 2 others like this"

### Solution

### 1

>function likes(names) {
>
>  $like_list="";
>
>  if(names.length===0)
>
>      $like_list="no one likes this";
>
>  else if(names.length===1)
>
>      $like_list=names[0]+' likes this';
>
>  else
>
>  {
>
>      if(names.length===2)
>
>          $like_list=names[0]+' and '+names[1];
>
>      else if(names.length===3)
>
>          $like_list=names[0]+', '+names[1]+' and '+names[2];
>
>      else
>
>          $like_list=names[0]+', '+names[1]+' and '+(names.length-2)+' others';
>
>      $like_list=$like_list+' like this';
>
>  }
>
>  return $like_list;
>
>}

### 2

>function likes(names) {
>  names = names || [];
>  switch(names.length){
>    case 0: return 'no one likes this'; break;
>    case 1: return names[0] + ' likes this'; break;
>    case 2: return names[0] + ' and ' + names[1] + ' like this'; break;
>    case 3: return names[0] + ', ' + names[1] + ' and ' + names[2] + ' like this'; break;
>    default: return names[0] + ', ' + names[1] + ' and ' + (names.length - 2) + ' others like this';
>  }
>}