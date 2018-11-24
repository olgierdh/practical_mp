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

### The good and the bad ( no ugly yet )

@snap[east]
- Code complexity
- Error reporting
- Compile times
@snapend

@snap[west]
- Type safety 
- Code correctness ( fail early )
- More optimizations 
@snapend

---

```cpp
int test( int a )
{
    return a;
}
```
