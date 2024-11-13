## Non-Deadlock Bugs
Simple atomicity violation: use and re-use, the wrong assumption of the atomic operations, but in fact it could be interrupted

order violation: enforce the order

## Deadlock bugs
**Four condition**:

Mutual exclusion: lock-free approach: use the atomic instruction based on hardware 

Hold-and-wait: solution is to ensure locks could be acquires at once. The easiest way is to set a big lock outside to ensure only one process could enter.

No preemption: `trylock`. If unsuccessful, then unlock the lock previously hold.

Circular wait: provide partial ordering. Use the address of lock as the order, and always acquire lower address lock first.
