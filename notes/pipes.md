# Pipes

### Built in
* `date`  
Formats a date input. It accepts formatting:
```angular2html
{{ dateInput | date: 'MMM/dd/yyyy' }}
```

* `uppercase`  
Takes a string and makes it uppercase.

* `lowercase`  
Takes a string and makes it lowercase.

* `titlecase`  
Takes a string and makes it capitalized.

* `number`  
Several options for formatting a number.

* `currency`  
Several options for formatting a number to currency

* `percent`  
Quite self explanatory isn't it?.

* `slice`  
Slice elements from an array.

* `json`  
Converts to json.

* `keyvalue`  
Returns an array of key value pairs of an object.

* `orderBy`  
Orders and array by a specific criteria.

* `limitTo`  
Limits array into specific number of elements.


### Parametrized pipe syntax
```angular2html
<p>Price is {{ price | currency : 'USD$' : 0.00 }}</p> 
```

### Custom Pipe implementation
Every pipe must apply the method `transform()`, and the decorator syntax is as follows:
```angular2
@Pipe({
	name: 'pipeName'
})
export class PipeName {
	transform() {
		// pipe transform here
	}
}
```
