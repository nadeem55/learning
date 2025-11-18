# Java
## JVM (Java Virtual Machinge) Tunning
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
  - Serial GC
  - Parallel GC
  - CMS GC (Concurrent, Marking and Sweep)
  - G1 GC (Garbage-first)
  - Z GC 
        
