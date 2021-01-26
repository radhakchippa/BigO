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
