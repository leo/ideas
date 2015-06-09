# Dynamic libraries

To me, it looks like developers are caring more and more about frameworks and pretty libraries which speed up the development-process and enable them to do more in less time (which of course saves money, but that’s not why were here, right?). The disadvantage of this method is that while they’re doing so, they’re losing the sense for being able to squish out the maximum of performance. This leads to a much slower www, but helps agencys - and other companies that are creating websites for money - to finish more orders within the same time.

Marco Arment [commented][1] this scenario in a pretty neat way:

> The entire culture dominant among web developers today is bizarrely framework-heavy, with seemingly no thought given to minimizing dependencies and page weight. Most times I land on a Stack Overflow page with a simple Javascript question, the highest-voted answer is “Just include [framework X] and then call this function,” even though a few posts beneath it is a perfectly suitable, standalone 10-line function.

We need to do something about this. What about a node module that only outputs the functions that are called within the code and leaves the remaining ones out when using multiple libraries? We could also combine muiltiple occurrences of the same code into functions. It should of course also directly replace the instances with the suitable function-call.

[1]: http://www.marco.org/2015/05/15/tools-are-the-problem