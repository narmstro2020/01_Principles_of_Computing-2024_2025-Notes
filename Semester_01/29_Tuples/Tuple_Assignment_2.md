
# Assignment 2: Advanced Tuple Operations and Applications

## Instructions

1. **Nested Tuples**
   - Create a nested tuple `city_data` with the following structure:
     ```python
     city_data = (("New York", "USA"), ("Paris", "France"), ("Tokyo", "Japan"))
     ```
   - Access and print the country of the second city (Paris) from `city_data`.

2. **Using Tuples as Dictionary Keys**
   - Create a dictionary named `coordinates_dict` with the following data, using tuples as keys to represent coordinates:
     - Key: `(34.0522, -118.2437)`, Value: `"Los Angeles"`
     - Key: `(40.7128, -74.0060)`, Value: `"New York"`
     - Key: `(51.5074, -0.1278)`, Value: `"London"`
   - Write code to:
     - Print the city name corresponding to the coordinates `(40.7128, -74.0060)`.
     - Check if the coordinates `(48.8566, 2.3522)` (Paris) are in the dictionary and print an appropriate message indicating if they are found.

3. **Tuple Conversion and Generator Expressions**
   - Create a list named `squared_numbers` with values `[1, 2, 3, 4, 5]`.
   - Convert `squared_numbers` to a tuple after squaring each element using a generator expression.
   - Print the resulting tuple.

**Submission**: Submit a Python script that performs all tasks and includes comments explaining each part.
