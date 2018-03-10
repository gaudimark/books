#  Conditional expressions 条件表达式

* for example:

  ```
  1.
  if x > 0:
      y = math.log(x)
  else:
      y = float('nan')
      
  2.
  def factorial(n):
      if n == 0:
          return 1
      else:
          return n * factorial(n-1)
          
  3.
  def __init__(self, name, contents=None):
      self.name = name
      if contents == None:
          contents = []
      self.pouch_contents = contents
  ```

  ​

* conditional expression:

  ```
  1.
  y = math.log(x)     if x > 0     else     float('nan')

  2.
  def factorial(n):
      return 1 if n == 0  else  return n * factorial(n-1)
      
  3.
  def __init__(self, name, contents=None):
      self.name = name
      self.pouch_contents = []
      if contents == None else contents
  ```

  ​