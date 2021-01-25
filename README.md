# BigO
# Drop Constants When calcualting Big-O.#
It is very possible for O(N) code to run faster than O(1) code for specific inputs. Big O just describes the rate of increase.  For this reason, we drop the constants in runtime. An algorithm that one might have described as O(2N) is actually O(N).  Many people resist doing this. They will see code that has two (non-nested) for loops and continue this O(2N).  They think they are being more "precise". They are NOT.
