#Regular Expression for Algerian Mobile Phone Numbers
    
##Mobile number format
     ^(00213|\+213|0)(5|6|7)[0-9]{8}$
    
###Javascript Example

```javascript

var reg=  /^(00213|\+213|0)(5|6|7)[0-9]{8}$/

reg.test("021481515"); // false
reg.test("0770123456"); // true
reg.test("0550123456"); // true
reg.test("0440123456"); // false
reg.test("0660123456"); // true
reg.test("00213660123456"); // true
reg.test("+213660123456"); // true

```
## PHP example show number (even with the case with numbers in same line)

```php
if(preg_match_all('/(00213|\+213|0)(5|6|7)[0-9]{8}/',$number,$matches)){
        foreach($matches[0] as $num){
            $num = preg_replace('/\+213/','0',$num);
            echo $num."<br>"; 
        }
```
