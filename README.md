# math-algoritms
Experiment. Bad code. Do not use it.

```javascript
function toFunction(arr) {
  var f = [];
  for (var i = 0; i < arr.length; i++) {
    var a = arr[i];
    var b = [];
    for (var j = 0; j < arr.length; j++) {
      if (j === i) continue;
      a /= j - i;
      b.push('(' + j + '-x)');
    }
    f.push('(' + a + '*' + b.join('*') + ')');
  }
  return Function('x', 'return ' + f.join('+') + ';');
}
```

```javascript
var a = toFunction([5,7,4,3]);

a(0) === 5
a(1) === 7
a(2) === 4
a(3) === 3
```
