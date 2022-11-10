
# Specification refinement of a multithreaded counter in Why3

This is an example inspired by a blog post by Hillel Wayne [https://www.hillelwayne.com/post/refinement/]

The idea is to specifiy a counter by a single abstract action that increments its value, moving the state of the thread from Start to Done. This assumes an atomic update operation that is unavailable for implementation, and must then be refined into atomic read and write actions, controlled by a lock.

  * Abstract.mlw: abstract spec
  * Impl_lock_START.mlw: implementation and proof that it refines the abstract spec. Start with this file if you want to guess the required inductive invariant and other annotations
  * Impl_lock.mlw: the previous file with all required annotations
  * core.mlw: library modules for induction and refinement

	
