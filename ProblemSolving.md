# How to start solving engineering problem
1. Divide and conquer: Remember to crawl before walk and walk before run. 
   This means in this approach we understand big picture (draw architecture and big picture of what's required) ; 
   divide big problem into small subproblems and attack each sub problem one at a time. The idea is if we can make 
   each subproblem fixed then we puttogether it should work ; if not then we put first two fixes together andmake it work then add third in the mix etc. but basically one slice at a time. The idea is to identifying the tiniest part that's not working and fixing it. For solving each of this subproblem we could use any of following steps.
2. Start by simulating each problem locally and try fixing it.
3. If there is any log of error or error message search it ether on company wiki or the Internet.
4. If trying to use some API and not working then read the documentation of API from cretors (i.e. original source)| make sure you've thoroughly understood how the technology you are using works.
5. If it was working before and not working now (example. main branch works fine but your feature branch has issues) then check what is changed in comparison to the previous working code
6. If issue related to library being used and documentation not helping then checkout code (only possible if open source) read through the code and documentation of any particular library you are using(Ex. If you are using any Nuget package then read the documentation of that package and go the code/repo of it)
