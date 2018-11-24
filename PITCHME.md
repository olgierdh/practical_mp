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
@snap[west span-50]
#### The bad
@ul
- Code complexity
- Error reporting
- Compile times
@ulend
@snapend

@snap[east span-50]
#### The good
@ul
- Type safety 
- Code correctness
- More optimizations 
@ulend
@snapend

---

```cpp
int test( int a )
{
    return a;
}
```
