# BigO
# Drop Constants When calcualting Big-O. #
It is very possible for O(N) code to run faster than O(1) code for specific inputs. Big O just describes the rate of increase.  For this reason, we drop the constants in runtime. An algorithm that one might have described as O(2N) is actually O(N).  Many people resist doing this. They will see code that has two (non-nested) for loops and continue this O(2N).  They think they are being more "precise". They are NOT.  Big-O allows us to express how the runtime scales.  We just need to accept that it doesn't mean that O(N) is always better than O(N^2).
# Drop the NON-Dominant Terms #
You should drop the non-dominant terms
* O(N^2 + N) becomes O(N^2).
* O(N + logN) becomes O(N).
* O(%*2^N + 1000N^100) becomes O(2^N).
# Multi-part Algorithms: Add vs Multiply #
* If your algorithm is in the form "do this, then when you're all done, do that" then you add the runtimes.
* If your algorithm is in the form "do this for each time you do that" then you multiply the runtimes.
# Amortized Time #
An Arraylist or a dynamically resizing array, allows you to have the benefits of an array while offering flexibility in size.  You won't run out of space in the ArrayList since its capacity will grow as you insert Elements.  An Arraylist is implemented with an array. When the array hits capacity, the ArrayList class will crea a new array with double the capacity and copy all the elements over the new array.  How do you describe the runtimeof insertion?  The Array could be full.  If the array contains N elements, then inserting a new element will take O(N) time. You will have to create a new array of size 2N and then copy N elements over.  This insertion will take O(N) time.  However, we also know that this doesn't happen very often.  The vast majority of the time insertion will be O(1) time.  We need a concept that takes both 
