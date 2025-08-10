# **Python Built-in Types: Mutability, Hashability & Characteristics**

| Type           | Mutable? | Hashable? | Ordered?  | Allows duplicates? | Indexable? | Example              |
| -------------- | -------- | --------- | --------- | ------------------ | ---------- | -------------------- |
| **list**       | ✅ Yes    | ❌ No      | ✅ Yes     | ✅ Yes              | ✅ Yes      | `[1, 2, 2]`          |
| **tuple**      | ❌ No     | ✅ Yes\*   | ✅ Yes     | ✅ Yes              | ✅ Yes      | `(1, 2, 2)`          |
| **range**      | ❌ No     | ✅ Yes     | ✅ Yes     | ✅ Yes\*            | ✅ Yes      | `range(5)`           |
| **set**        | ✅ Yes    | ❌ No      | ❌ No      | ❌ No               | ❌ No       | `{1, 2, 3}`          |
| **frozenset**  | ❌ No     | ✅ Yes     | ❌ No      | ❌ No               | ❌ No       | `frozenset({1, 2})`  |
| **dict**       | ✅ Yes    | ❌ No      | ✅ Yes\*\* | ❌ No               | ❌ No\*\*\* | `{"a": 1, "b": 2}`   |
| **str**        | ❌ No     | ✅ Yes     | ✅ Yes     | ✅ Yes              | ✅ Yes      | `"hello"`            |
| **bytes**      | ❌ No     | ✅ Yes     | ✅ Yes     | ✅ Yes              | ✅ Yes      | `b"abc"`             |
| **bytearray**  | ✅ Yes    | ❌ No      | ✅ Yes     | ✅ Yes              | ✅ Yes      | `bytearray(b"abc")`  |
| **memoryview** | ✅ Yes    | ❌ No      | ✅ Yes\*   | ✅ Yes\*            | ✅ Yes      | `memoryview(b"abc")` |
| **bool**       | ❌ No     | ✅ Yes     | —         | —                  | —          | `True`               |
| **int**        | ❌ No     | ✅ Yes     | —         | —                  | —          | `42`                 |
| **float**      | ❌ No     | ✅ Yes     | —         | —                  | —          | `3.14`               |
| **complex**    | ❌ No     | ✅ Yes     | —         | —                  | —          | `2+3j`               |
| **NoneType**   | ❌ No     | ✅ Yes     | —         | —                  | —          | `None`               |

**Notes:**

* *Tuple*: Hashable **only if** all elements are hashable.
* *Range*: No duplicates **within** the defined range, but conceptually you can have repeated numbers by creating different ranges.
* **Dict Ordered**: Since Python 3.7+, preserves insertion order by language spec.
* ***Dict Indexable?***: You can’t access by numeric index, only by key (`dict["key"]`).
* *Memoryview Ordered/Duplicates*: Depends on underlying bytes-like object.
