
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

# HashMap
<img width="1312" height="1199" alt="image" src="https://github.com/user-attachments/assets/55935948-6948-4284-a473-4576a23a2aa2" />

# Linked HashMap
<img width="1312" height="1199" alt="image" src="https://github.com/user-attachments/assets/ad0861de-1cd0-421b-a5b1-3aac01bfe448" />

# TreeMap
<img width="1312" height="1199" alt="image" src="https://github.com/user-attachments/assets/8f0f051f-2c6e-44b6-8e49-d4a788e26104" />

