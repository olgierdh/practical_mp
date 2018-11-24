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
@snap[north-west]
### The bad
@snapend

@snap[north-east]
### The good
@snapend

@snap[west]
@ol
- Code complexity
- Error reporting
- Compile times
@olend
@snapend

@snap[east]
@ol
- Type safety 
- Code correctness ( fail early )
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
