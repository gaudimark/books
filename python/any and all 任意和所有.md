#  any and all 任意和所有

* For example

  ```
  1.
  any([False, False, True])

  2.
  any(letter == 't' for letter in 'monty')

  3.
  def avoids(word, forbidden):
      return not any(letter in forbidden for letter in word)
      
  4.

  ```

  ​