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
@nap[north]
### The good and the bad ( no ugly yet )
@snapend

@snap[east]
@ol
- Code complexity
- Error reporting
- Compile times
@olend
@snapend

@snap[west]
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
