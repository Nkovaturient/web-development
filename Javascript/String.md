# String in JavaScript
*Definition:*
---  
💠Strings are text or sequence of characters.It can be written in double quotes(" "), Single quotes(' ')

### Strings are immutable:
* No changes can be made to strings.     
    Whenever we do try to make a change, a new string is created and old one remains same.


  EXAMPLE:
  ```let name="Creator";```

## String Indices

💠Index starts from "0".In string space is also considered as an index number according to their sequence

EXAMPLE:```let name="iron man";```

EXPLANATION: from above example,   
                i -> index "0"  
                r -> index "1"  
                o -> index "2"  
                n -> index "3"  
                " " -> index "4"  
                m -> index "5"  
                a -> index "6"  
                n -> index "7"
            
```let name="iron man";```  
name[0] -> 'i'  
name[6] -> 'a'

### Concatenation
*Meaning*: Adding Strings together

Example: ```"iron"+" "+"man" = iron man```

To concatinate string we use "+".

# String Methods
**METHODS-( )**
Actions that can be performed on objects.

*Format* : ```StringName.method()```

* ## str.trim( )
💠Trims White Spaces from both ends of string and returns a new one

EXAMPLE :   
```let msg = " hey! ";```  
   ```  msg.trim(); ```  
   output: 'hey!' (but value of msg remains same);

* ## str.toUpperCase()
💠Convert Lower case letters into upper case letters.

Example:  
 ```let str="creator";```  
         ```str.toUpperCase();```  
         output : "CREATOR"

* ## str.toLowerCase()
💠Convert Upper case letters into Lower case letters.

Example:  
 ```let str="CREATOR";```  
         ```str.toLowerCase();```  
         output : "creator"





