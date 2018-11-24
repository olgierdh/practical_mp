## Practical Metaprogramming 
### in C++ 
#### for everyone\*
##### Olgierd Humeńczuk 

---

### C++ evolution

- Derived from C language
- Reasons for having templates
- DRY ( Do not Repeat Yourself )

---
@snap[west]
### The bad
@ol
- Code complexity
- Error reporting
- Compile times
@olend
@snapend

@snap[east]
### The good
@ol
- Type safety 
- Code correctness
- More optimizations 
@olend
@snapend

---

```cpp
int test( int a )
{
    return a;
}
```
