# javascript-good-commands

## array data manipulation
```pets.pop(); pets.push("fish", "ferret");```

```pets.shift();``` remove from start of array
```pets.unshift("fish", "ferret");``` adds item to start of the array

Use the splice method to insert one or more elements anywhere in an array, while
optionally removing one or more elements that come after it. Suppose you have an array with
the elements "dog", "cat", "fly", "bug", "ox". The following code adds "pig", "duck", and "emu"
after "cat" while removing "fly" and "bug".
```pets.splice(2, 2, "pig", "duck", "emu");```
first 2 is the index to start adding at, 2nd 2 is the number of array elements to remove

we can remove without adding any too


Use the slice method to copy one or more consecutive elements in any position and put
them into a new array. If you start with an array, pets, consisting of "dog", "cat", "fly", "bug",
and "ox", the following code copies "fly" and "bug" to the new array noPets and leaves the
original array, pets, unchanged.
```var noPets = pets.slice(2, 4);```

## changing case
```
cityToCheck = cityToCheck.toLowerCase();

cityToCheck = cityToCheck.toUpperCase();
```

If cityToCheck is "Boston", firstChar is "B".
```var firstChar = cityToCheck.slice(0, 1);```
Things to be aware of:
A string is indexed like an array. Only, instead of each index number referring to an
element, it refers to a character.

Like array indexing, string indexing begins with 0.

In the slice method, the first number inside the parentheses is the index of the first
character in the slice. The second number is not, however, the last character in the slice.
It's the first character after the slice. If you subtract the first index from the second index,
you'll always get the length of the slice.

If you omit the second number inside the parentheses, JavaScript includes all the
characters to the end of the string.


## use of .length
no double spaces
```
1 var str = prompt("Enter some text");
2 var numChars = str.length;
3 for (var i = 0; i < numChars; i++) {
4 if (str.slice(i, i + 2) === " ") {
5 alert("No double spaces!");
6 break;
```

## Strings: Finding segments
```
1 for (var i = 0; i < text.length; i++) {
2 if (text.slice(i, i + 12) === "World War II") {
3 text = text.slice(0, i) + "the Second World War" + text.slice(i + 12);
4 }
5 }
```
