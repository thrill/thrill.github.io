<div style="float: right; margin-left: 12px">
  <img src="assets/logo-600.png" alt="Thrill logo" width="140" height="140" />
</div>

## About Thrill

Thrill is a C++ framework for **distributed Big Data batch computations on a cluster of machines**. It is currently being designed and developed as a research project at [Karlsruhe Institute of Technology](http://algo2.iti.kit.edu) and is in early testing.

The [development code is available on github <span class="icon  icon--github"><svg viewBox="0 0 16 16"><path fill="#828282" d="M7.999,0.431c-4.285,0-7.76,3.474-7.76,7.761 c0,3.428,2.223,6.337,5.307,7.363c0.388,0.071,0.53-0.168,0.53-0.374c0-0.184-0.007-0.672-0.01-1.32 c-2.159,0.469-2.614-1.04-2.614-1.04c-0.353-0.896-0.862-1.135-0.862-1.135c-0.705-0.481,0.053-0.472,0.053-0.472 c0.779,0.055,1.189,0.8,1.189,0.8c0.692,1.186,1.816,0.843,2.258,0.645c0.071-0.502,0.271-0.843,0.493-1.037 C4.86,11.425,3.049,10.76,3.049,7.786c0-0.847,0.302-1.54,0.799-2.082C3.768,5.507,3.501,4.718,3.924,3.65 c0,0,0.652-0.209,2.134,0.796C6.677,4.273,7.34,4.187,8,4.184c0.659,0.003,1.323,0.089,1.943,0.261 c1.482-1.004,2.132-0.796,2.132-0.796c0.423,1.068,0.157,1.857,0.077,2.054c0.497,0.542,0.798,1.235,0.798,2.082 c0,2.981-1.814,3.637-3.543,3.829c0.279,0.24,0.527,0.713,0.527,1.437c0,1.037-0.01,1.874-0.01,2.129 c0,0.208,0.14,0.449,0.534,0.373c3.081-1.028,5.302-3.935,5.302-7.362C15.76,3.906,12.285,0.431,7.999,0.431z"/></svg></span>](http://github.com/thrill/thrill) under a BSD open-source license and outside contributors are welcome to join and contact us. [Doxygen documentation](http://i10login.iti.kit.edu/thrill-doxygen/) automatically built from the master is available.
An [older presentation on the project](https://panthema.net/2015/0327-Project-DALKIT/) gives a good overview our target, even though many details have changed in the meantime.

<table>
<tr>
<td>GitHub:</td>
<td>
<iframe src="http://ghbtns.com/github-btn.html?user=thrill&repo=thrill&type=watch&count=true" frameborder="0" scrolling="no" width="80" height="20"></iframe>
<iframe src="http://ghbtns.com/github-btn.html?user=thrill&repo=thrill&type=follow&count=true" frameborder="0" scrolling="no" width="110" height="20"></iframe>
</td>
</tr>
</table>

Travis-CI: [![Travis-CI Status](https://travis-ci.org/thrill/thrill.svg?branch=master)](https://travis-ci.org/thrill/thrill)

Some of the main goals for the design are:

- To create a high-performance Big Data batch processing framework.

- Expose a **powerful C++ user interface**, that is efficiently tied to the framework's internals. The interface supports the Map/Reduce paradigm, but also versatile **"dataflow graph" style computations** like Apache Spark or Apache Flink with host language control flow.<br>
See our [WordCount example](http://i10login.iti.kit.edu/thrill-doxygen/word__count_8hpp_source.html#l00035).

- Leverage newest **C++11 and C++14 features** like lambda functions and auto types to **make writing user programs easy and convenient**.

- Enable compilation of **binary programs with full compile-time optimization** runnable directly on hardware without a virtual machine interpreter. Exploit cache effects due to less indirections than in Java and other languages. **Save energy and money** by reducing computation overhead.

- Due to the **zero-overhead** concept of C++, enable applications to process small datatypes efficiently with no overhead.

- Support external memory well by implementing **I/O-efficient algorithms** where needed, but **keep most computations in RAM**.

- Perform **full pipelining of data flows**, where pipelined stages are often combined at compile time.

- **Avoid all unnecessary round trips of data to memory or disk**.

- Enable **reproducible benchmarking** of programs due to RAII memory management.

In the long term the framework can play a **mediator role** between Big Data applications and lower layer algorithms research, which may include:

- Research into more communication efficient distributed algorithms for basic operations like sorting, selection, hashing, etc.

- Support fault tolerant execution with lower overheads due to fault-resilient algorithms and better checkpointing.

- Join Big Data research with succinct data structures and compression to enable more computations to be performed in RAM.

## Current Authors and Contributors:

[Michael Axtmann](https://github.com/MichaelAxtmann),
[Timo Bingmann](http://panthema.net),
[Emanuel Jöbstl](http://eex-dev.net/),
[Sebastian Lamm](https://github.com/sebalamm),
[Huyen Chau Nguyen](http://chau-nguyen.de/),
[Alexander Noe](https://github.com/alexnoe),
[Matthias Stumpp](https://matstumpp.wordpress.com/),
[Peter Sanders](http://algo2.iti.kit.edu/sanders.php),
[Sebastian Schlag](https://github.com/SebastianSchlag),
[Tobias Sturm](http://tobiassturm.de).
