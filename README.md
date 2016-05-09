# heOmer.js

The heOmer is small function base on [`heDate.js`](https://github.com/daniellevanon/he-date) project that return the Omer day(ספירת העומר).

HeDate site http://he-date.info/site.html (Hebrew)

## Quick Examples

```javascript
var s=omer(new HeDate(),1);
//now s is event string or null.
 ```
## Demo

http://he-date.info/public/demoOmer.html
 
```html
	<script src='heDate.min.js'></script>
	<script src='HeOmer.min.js'></script>
	<script>
		var year = (new HeDate()).getYear();
		var heDate = new HeDate(year,1,1);
		while (heDate.getYear()==year){
			var event=omer(heDate,1);
			if (event){
				var li = document.createElement("li");
				var t = document.createTextNode(heDate.toString() + "   -   " + event);
				li.appendChild(t);
				document.getElementById("list").appendChild(li);
			}
			heDate.setDate(heDate.getDate()+1);
		}
	</script>
```

## License
 
Copyright (c) 2014 (ה'תשע"ה) daniel levanon (daniellevanon@gmail.com)

HeDate may be freely distributed under the MIT license. (see LICENSE.md file)
 
