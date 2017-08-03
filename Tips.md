
## Boolean Expression

null, undefined, ' ' the empty string and 0 the number are all false boolean expression.
But be careful, '0' the string, [ ] the empty array, and {} the empty object are all true boolean expression.

so instead of using

      if(x != null)

You can write the shorter format
   
      if(x)

Similarly, if you want to check both null and empty. You can do like this:

      if(x != null && x != ' ')

However, You can write short and nice
   
      if(x)

## Conditional Ternary Operator

Instead of this,

      if (x) {
         foo();
      } else {
         bar();
      }

you can use the ternary operator,

      return x ? foo( ) :bar( )

## Short Circuit Operator

&& and ||, these operators are called as short circuit operators. Consider the following code.

      function foo(x) {
         var win;
         if (x) {
            win = x;
         } else {
            win = window;
         }
      }

You can rewrite above code as 

      function foo(x) {
         var win = x || window;
      }

&& is also used to reduce the lines of code, Please find the code below.

      if (student) {
         if (student.name) {
            if (student.name[index]) {
               foo(student.name[index]);
            }
         }
      }

You can rewrite the code as

      if (student && student.name && student.name[index]) {
         foo(student.name[index]);
      }

or, you can use a variable as,

      var flag = student && student.name && student.name[index];
      if (flag) {
         foo(student.name[index]);
      }

## Iteration using for loop:

For loop:

    var paragraphs = [1, 2, 3, 4, 5, 6];
    for (var i = 0; i < paragraphs.length; i++) {
       var paragraph = paragraphs[i];
       console.log(paragraph);
    }

Above code can be modified as below.

    var paragraphs = [1, 2, 3, 4, 5, 6];
    for (var i = 0, paragraph; paragraph = paragraphs[i]; i++) {
       console.log(paragraph);
    }
