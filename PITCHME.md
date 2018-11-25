## Practical Metaprogramming 
#### for everyone\*
##### Olgierd Humeńczuk 

---

### C++ evolution

- Derived from C language
- Reasons for having templates
- DRY ( Do not Repeat Yourself )

---
@snap[north span-100]
### How about metaprogamming ?
@snapend

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

### Language

Basics of metaprogramming

* S.F.I.N.A.E. [example](https://godbolt.org/z/sA01si)
* Parameter packs
* Template variables 

---

```cpp
int test( int a )
{
    return a;
}
```
