# Lock-Primitives

A better synchronization mechanism: Sequential Lock

Seqlocks are an important synchronization mechanism and represent a significant improvement over
conventional reader-writer locks in some contexts. They avoid the need to update a synchronization
variable during a reader critical section, and hence improve performance by avoiding cache coherence
misses on the lock object itself. Unfortunately, they rely on speculative racing loads inside the critical
section. This makes them an interesting problem case for programming-language-level memory models
that emphasize data-race-free programming.
