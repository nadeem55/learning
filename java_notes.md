# Java
## Memory Types (Stack & Heap)
- Statck & Heap
- Stack contains variables and objects
- Heap
- Marking and Sweaping
- GC (Garbage Collector) targets the heap and remove the variables and objects which don't have direct and indirect link with Stack
- System.gc() -- to ask the garbage collector to collect/clean the variables and objects from heap
- Sweeping techniques
  - Normal sweeping
  - Sweeping & compacting
  - Sweeping & coping
- Types of Heap
  - Heap Momory
      - Young generation (eden space & survivor space)
      - Old generation, it is also called tenured space (moving the objects from survior space to old generation space is called scavenging)
  - Non-Heap Memory
      - ~~Permanent generation~~  Metaspace (since Java 8)
        - Contains classes meta data (class structure, constant, methods of class, annotations, opitimization)
- Strategies for GC
  - Stop the World (pause the application)
  - Concurrent
- Different Garbage Collectors
  - Serial GC  - single threaded
  - Parallel GC - multi threaded
  - CMS GC (Concurrent, Marking and Sweep) - multi threaded
  - G1 GC (Garbage-first) - multi threaded
  - Z GC
      - maximum pause is 10ms
      - Available since Java 15
      - Multi threaded and Concurrent
      - Only aplicable to 64bit system
## JVM (Java Virtual Machinge) Tunning
- How the heap is functioning
- What is the latency rate
- What is throughput
        
## To Change Installed JDK Version
- sudo update-alternatives --config java ```if multiple JDK are installed then this command is used to show and change default JDK```
