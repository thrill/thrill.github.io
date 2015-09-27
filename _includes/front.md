## About Thrill

Thrill is a C++ framework for distributed Big Data computations on a cluster of machines. It is currently being designed and developed as a research project at [Karlsruhe Institute of Technology](http://algo2.iti.kit.edu) and is in early testing.

The [development code is available on github](http://github.com/thrill/thrill) under a yet-to-be-determined open-source license and outside contributors are welcome to join and contact us. [Doxygen documentation](http://i10login.iti.kit.edu/thrill-doxygen/) automatically built from the master is available.
An [older presentation on the project](https://panthema.net/2015/0327-Project-DALKIT/) gives a good overview our target, even though many details have changed in the meantime.

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
