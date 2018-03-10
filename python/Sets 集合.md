# Sets 集合

* For example

  ```
  1.
  def subtract(d1, d2):
      res = dict()
      for key in d1:
          if key not in d2:
              res[key] = None
      return res
      
  2.
  def has_duplicates(t):
      d = {}
      for x in t:
          if x in d:
              return True
      d[x] = True
      return False

  3.
  def uses_only(word, available):
      for letter in word:
      if letter not in available:
          return False
      return True

  ```

* Sets

  ```
  1.
  def subtract(d1, d2):
      return set(d1) - set(d2)

  2.
  def has_duplicates(t):
      return len(set(t)) < len(t)

  3.
  def uses_only(word, available):
      return set(word) <= set(available)

  ```

  ​