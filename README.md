### Assignment

In this project, you will use object oriented programming to create a `Rectangle` class and a `Square` class. The `Square` class should be a subclass of `Rectangle`, and inherit its methods and attributes.

#### Rectangle class

When a Rectangle object is created, it should be initialized with `width` and `height` attributes. The class should also contain the following methods:
* `set_width`
* `set_height`
* `get_area`: Returns the area
* `get_perimeter`: Returns the perimeter
* `get_diagonal`: Returns the diagonal
* `get_picture`: Returns a string describing the rectangle with lines of asterisk "\*" characters. The number of lines should be equal to the height, and the number of "\*" in each line should be equal to the width. There should be a new line (`\n`) at the end of each line. If the width or height is greater than 50, the method should return: "Too big for picture.".
* `get_amount_inside`: Takes another shape (square or rectangle) as an argument. Returns the number of times the input shape could fit inside the original shape (with no rotations). For instance, a rectangle with a width of 4 and a height of 8 could fit in two squares with sides of 4.

Finally, if an instance of the Rectangle class is represented as a string, it should look like: `Rectangle(width=w, height=h)`, where "w" and "h" refer to the width and height of the object.

#### Square class

The Square class should be a subclass of Rectangle. When a Square object is created, it should be initialized with a single attribute describing the side of the shape. The `__init__` method should use this value for both the `width` and `height` attributes of the Rectangle class.

On top of the methods specified for the Rectangle class, the Square class should also contain a `set_side` method. This method should update both the `width` and the `height` of the shape.

Be sure to update the `set_width` and `set_height` methods on the Square class, so that the width and height always match.

Finally, if an instance of a Square is represented as a string, it should look like: `Square(side=s)`, where "s" describes describes the side of the object.

#### For example

```py
rect = shape_calculator.Rectangle(10, 5)
print(rect.get_area())
rect.set_height(3)
print(rect.get_perimeter())
print(rect)
print(rect.get_picture())

sq = shape_calculator.Square(9)
print(sq.get_area())
sq.set_side(4)
print(sq.get_diagonal())
print(sq)
print(sq.get_picture())

rect.set_height(8)
rect.set_width(16)
print(rect.get_amount_inside(sq))
```

The previous snippet should return:

```
50
26
Rectangle(width=10, height=3)
**********
**********
**********

81
5.656854249492381
Square(side=4)
****
****
****
****

8
```

### Development

Write your code in `shape_calculator.py`. For development, you can use `main.py` to test your `shape_calculator()` function. Click the "run" button and `main.py` will run.

### Testing 

We imported the tests from `test_module.py` to `main.py` for your convenience. The tests will run automatically whenever you hit the "run" button.

### Submitting

Copy your project's URL and submit it to freeCodeCamp.
