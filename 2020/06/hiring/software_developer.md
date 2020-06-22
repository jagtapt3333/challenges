Question 01 answer 


# A Python3 program to find if 2 given line segments intersect or not 

  

class Point: 

    def __init__(self, x, y): 

        self.x = x 

        self.y = y 

  

# Given three colinear points p, q, r, the function checks if  

# point q lies on line segment 'pr'  

def onSegment(p, q, r): 

    if ( (q.x <= max(p.x, r.x)) and (q.x >= min(p.x, r.x)) and 

           (q.y <= max(p.y, r.y)) and (q.y >= min(p.y, r.y))): 

        return True

    return False

  

def orientation(p, q, r): 

    # to find the orientation of an ordered triplet (p,q,r) 

    # function returns the following values: 

    # 0 : Colinear points 

    # 1 : Clockwise points 

    # 2 : Counterclockwise 

      

    

    

      

    val = (float(q.y - p.y) * (r.x - q.x)) - (float(q.x - p.x) * (r.y - q.y)) 

    if (val > 0): 

          

        # Clockwise orientation 

        return 1

    elif (val < 0): 

          

        # Counterclockwise orientation 

        return 2

    else: 

          

        # Colinear orientation 

        return 0

  

# The main function that returns true if  

# the line segment 'p1q1' and 'p2q2' intersect. 

def doIntersect(p1,q1,p2,q2): 

      

    # Find the 4 orientations required for  



Question 02 ans 

# Python3 program to count buildings  

# that can see sunlight. 

  

# Returns count buildings that 

# can see sunlight 

def countBuildings(arr, n): 

  

    # Initialuze result (Note that first  

    # building always sees sunlight) 

    count = 1

  

    # Start traversing element 

    curr_max = arr[0] 

    for i in range(1, n): 

      

        # If curr_element is maximum, 

        # update maximum and increment count 

        if (arr[i] > curr_max): 

          

            count += 1

            curr_max = arr[i] 

  

    return count 

  

# Driver code 

arr = [7, 4, 8, 2, 9] 

n = len(arr) 

print(countBuildings(arr, n)) 

