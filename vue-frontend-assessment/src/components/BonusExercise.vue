<template>
    <div class="container">
      <h1>Explain why the result of ('b' + 'a' + + 'a' + 'a').toLowerCase() is banana.</h1>
      <br>
      <br>
      <h2>Answer:</h2>
      <h4>
        In 'b' + 'a' + <span class="badge badge-primary bg-dark">+ 'a'</span> + 'a', <strong><i>+ 'a'</i></strong> resolves to NaN ("Not a Number") because it coerces string to a number, while the character <strong><i>a</i></strong> cannot be parsed as a number. To lowercase it becomes banana.
        <br>
        <br>
        Adding NaN to "ba" turns NaN into the string "NaN" due to type conversion, which then gives baNaN. And then there is another <i>a</i> after that, giving baNaNa.
        <br>
        <br>
        The space between + + first makes a string concatenation and the second one a unary plus (i.e. "positive") operator.
      </h4>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
          
      }
    }
  }
  </script>
  
  <style>
  
  </style>