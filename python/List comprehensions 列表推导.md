# List comprehensions 列表推导

* For example

  ```
  1.
  def capitalize_all(t):
      res = []
      for s in t:
          res.append(s.capitalize())
      return res
      
  2.
  def only_upper(t):
      res = []
      for s in t:
          if s.isupper():
              res.append(s)
      return res
  ```



* List comprehensions

  ```
  1.
  def capitalize_all(t):
      return [s.capitalize() for s in t]
      
  2.
  def only_upper(t):
      return [s for s in t if s.isupper()]
  ```

  ​