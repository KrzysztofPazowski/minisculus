Manuals, version 1

1)  The presented code is written in C#. You need to reference nunit.framework for tests to run.

2)	The code was obtained using TDD approach. Each question has own set of tests, see Question1Tests.cs, etc.

3)	The class Minisculus contains all methods needed to solve all five problems.

4)	You can delete the Minisculus class and keep redeveloping it following the tests: red, green, refactor. 

5)	Ctrl + F5 runs the Console Application. This will show the answer for the fifth question and all possible wheel settings. ‘3’ stands for ‘03’.

6)	The method DecodeWordForAllCombinations was initially used as a brut force to loop 100 times and costs O(n^2). Upon further development it was replaced by less costly EncodeWordForAllRequiredCombinations, which loops 21 times and returns a list of encoded words for all possible wheel settings. The method SubStringResponse uses it to see if the encoded words are contained in the coded message, and stops once found the encoded guess word (in this case loops only 4 times, max 21 times) and returns the wheels positions. Then the method WheelSettings produces all possible wheel setups based on the returned first wheel positions (loops 5 times).   The 100 times loop was replaced by three loops, max cost of looping: 21 + 21 +4 = 46 times.
It looks as not much was gained, but it is a backbone for more complicated algorithm, say with 4 wheels.  

Plan

1)	Refactor obeying the current Minisculus Challenge rules.

2)	Plug into .NET MVC3 framework.
-	Encode any string, user selects first and second wheel positions 
-	Decode any string, user inserts a guess word
-	The wheel rules are the same as in the Minisculus Challenge ( first – forward, second – twice backward, third – depends on second, forward)

3)	Programme Minisculus 6 :-)
-	4 wheels
-	Allow any wheel movement, forward, backward.
-	(Allow multiple wheel spinning up to 10 times.)
-	Eg. Wheel One – 4 times backward, wheel two – 7 times forward, wheel three – 10 times backward, wheel four – 2 times forward. 
-	Decode message: “Not ready yet”
-	Find all possible wheel positions.
