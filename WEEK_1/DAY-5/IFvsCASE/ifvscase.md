
## 🆚 If vs Case

| Feature              | `if` Statement                                             | `case` Statement                                                 |
| -------------------- | ---------------------------------------------------------- | ---------------------------------------------------------------- |
| **Usage**            | Inside `always` block                                      | Inside `always` block                                            |
| **Output**           | Must be `reg`                                              | Must be `reg`                                                    |
| **Priority**         | **Priority-based**: only the first true condition executes | **No priority**: all matching cases are independent              |
| **Multiple Matches** | Only **one branch executes**                               | Multiple branches can be matched (if wildcards or overlaps used) |
| **Default / Else**   | `else` acts as default                                     | `default` acts as default                                        |
| **Latch Risk**       | Incomplete conditions may infer latches                    | Incomplete cases may infer latches                               |

**Key Points:**

* Use **`if`** for **priority conditions** (e.g., enable signals, resets).
* Use **`case`** for **multi-way selection** (e.g., decoders, multiplexers).
* Always ensure **all outputs are assigned** to avoid **inferred latches**.

