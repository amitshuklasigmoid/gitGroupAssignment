##Find the largest three distinct elements in an array
###Given an array of integers, find the largest three elements.
Approach for solving the problem
####main.py file
1) Created Three_Largest class
2) Created take_input function that will take the input from input.txt file that is inside resources folder and spliting the text depending on the space and creating array (arr) of integers
3) Created return_arr function to return array arr after adding values from input.txt file
4) Created find3Largest function in which :
   -Initialized the largest three elements as minus max size using sys.
       first = second = third = -sys.maxsize

   -Iterate through all elements of array and updating first, second and third variable depending on the conditions
    a) Let current array element be x.
    b) If (x > first)
        {
            third = second
            second = first
            first = x   
        }
    c)  Else if (x > second and x != first)
        {
            third = second
            second = x 
        }
    d)  Else if (x > third and x != second)
        {
            third = x  
        }

  -Return first, second and third.
####test_print3Largest.py file
1) Created Test_find3Largest, Test_find3Largest_SampleCases classes
2) Inside Test_find3Largest class, created multiple test cases for handling input file, test cases based on some edge cases like if array size is 0,1,2 or arrays contains non numerical data like characters or float, test case for duplicate elements in array.
3) Inside Test_find3Largest_SampleCases created some test cases for different inputs and comparing with expected output and returned output
