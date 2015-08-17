## About Thrill

Thrill is a C++ framework for distributed Big Data computations on a cluster of machines. It is currently being designed and developed as a research project at [Karlsruhe Institute of Technology](http://algo2.iti.kit.edu) and is in early testing.

The [development code is available on github](http://github.com/thrill/thrill) under the MIT license and outside contributors are welcome to join and contact us. [Doxygen documentation](http://i10login.iti.kit.edu/c7adox/) automatically built from the master is available.

Some of the main goals for the design are:

- To create a high-performance Big Data processing framework.

- Expose a **powerful C++ user interface**, that is efficiently tied to the framework's internals. The interface supports the Map/Reduce paradigm, but also versatile **"dataflow graph" style computations** like Apache Spark or Apache Flink with host language control flow.<br>
See our [WordCount example](http://i10login.iti.kit.edu/c7adox/word__count_8hpp_source.html#l00035).

- Leverage newest **C++11 and C++14 features** like lambda functions and auto types to **make writing user programs easy and convenient**.

- Enable compilation of **binary programs with full compile-time optimization** runnable directly on hardware without a virtual machine interpreter. Exploit cache effects due to less indirections than in Java and other languages. **Save enery and money** by reducing computation overhead.

- Due to the **zero-overhead** concept of C++, enable applications to process small datatypes efficiently with no overhead.

- Support external memory well by implementing **I/O-efficient algorithms** where needed, but **keep most computations in RAM**.

- Perform **full pipelining of data flows**, where pipelined stages are often combined at compile time. Avoid all unnecessary round trips of data to memory or disk.

- Enable **reproducible benchmarking** of programs due to RAII memory management.

In the long term the framework can play a **mediator role** between Big Data applications and lower layer algorithms research, which may include:

- Research into more communication efficient distributed algorithms for basic operations like sorting, selection, hashing, etc.

- Support fault tolerant execution with lower overheads due to fault-resilient algorithms and better checkpointing.

- Join Big Data research with succinct data structures and compression to enable more computations to be performed in RAM.

## Current Authors and Contributors:

Michael Axtmann,
[Timo Bingmann](http://panthema.net),
Emanuel Jöbstl,
Sebastian Lamm,
Huyen Chau Nguyen,
Alexander Noe,
Matthias Stumpp,
[Peter Sanders](http://algo2.iti.kit.edu/sanders.php),
Sebastian Schlag,
[Tobias Sturm](http://tobiassturm.de).
