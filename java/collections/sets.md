
| Type                      | Interface/Class                                  | Internal structure         | Ordering               | Typical complexity |
| ------------------------- | ------------------------------------------------ | -------------------------- | ---------------------- | ------------------ |
| **HashSet**               | `Set` → `HashSet`                                | `HashMap`                  | No guaranteed order    | `O(1)` average     |
| **LinkedHashSet**         | `Set` → `HashSet` → `LinkedHashSet`              | `LinkedHashMap`            | Insertion order        | `O(1)` average     |
| **TreeSet**               | `Set` → `SortedSet` → `NavigableSet` → `TreeSet` | `TreeMap` / Red-Black Tree | Sorted order           | `O(log n)`         |
| **EnumSet**               | `Set` → `EnumSet`                                | Bit/vector representation  | Enum declaration order | Very efficient     |
| **CopyOnWriteArraySet**   | `Set`                                            | `CopyOnWriteArrayList`     | Insertion/array order  | Expensive writes   |
| **ConcurrentSkipListSet** | `Set` → `NavigableSet`                           | Skip-list                  | Sorted order           | `O(log n)`         |



# When to use HashSet, LinkedHashSet, TreeSet
```
Do I need uniqueness?
        │
       YES
        │
        ▼
Do I need sorted order?
     /        \
   YES         NO
    │           │
 TreeSet    Do I need
            insertion order?
             /       \
           YES        NO
            │          │
    LinkedHashSet   HashSet
```
