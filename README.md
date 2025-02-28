# **Bresenham's Line Algorithm**  

Bresenham's Line Algorithm is a widely used method in computer graphics for drawing a straight line between two given points. It is an optimized approach that relies solely on integer arithmetic, making it both faster and more efficient than traditional methods that involve floating-point calculations.  

By using a decision parameter, Bresenham’s algorithm determines the closest pixel to the ideal line path, ensuring smooth and accurate line rendering. This makes it particularly useful for low-resolution displays where precision is crucial.  

## **Algorithm**  

#### **Step 1:** Input the coordinates of the two endpoints, \( (x_1, y_1) \) and \( (x_2, y_2) \).  

#### **Step 2:** Compute the absolute differences:  
   - \( dx = |x_2 - x_1| \)  
   - \( dy = |y_2 - y_1| \)  

#### **Step 3:** Determine the direction of movement:  
   - If \( x_2 > x_1 \), set \( sx = 1 \); otherwise, set \( sx = -1 \).  
   - If \( y_2 > y_1 \), set \( sy = 1 \); otherwise, set \( sy = -1 \).  

#### **Step 4:** Initialize the error term:  
   - \( err = dx - dy \)  

#### **Step 5:** Set the starting point:  
   - \( (x, y) = (x_1, y_1) \)  

#### **Step 6:** Iterate until reaching \( (x_2, y_2) \):  
   1. Plot the point \( (x, y) \).  
   2. Compute \( e2 = 2 \times err \).  
   3. If \( e2 > -dy \):  
      - Update \( err = err - dy \)  
      - Update \( x = x + sx \)  
   4. If \( e2 < dx \):  
      - Update \( err = err + dx \)  
      - Update \( y = y + sy \)  

#### **Step 7:** Repeat Step 6 until the endpoint \( (x_2, y_2) \) is reached.  


