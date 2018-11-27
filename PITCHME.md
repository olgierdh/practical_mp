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
- [Error reporting](https://godbolt.org/z/O-Fk6O)
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
* Parameter packs [example](https://godbolt.org/z/i8BeI2)
* Type lists and iteration [example](https://godbolt.org/z/p569Mp)

---

#### What kind of problems we can solve using metaprogramming ? (1/4)

Metaprogramming can be used:
* Whenever the choice or structure is limited and depends on type or types
    * Calling functions in some order described via type lists
    * Generating bindings for an API like a programming language or just a library

---

#### What kind of problems we can solve using metaprogramming ? (2/4)

Metaprogramming can be used:
* For generating data using math functions
    * Lookup tables ( trigonometric functions, textures )
    * Datastructures accessed at compile time
    * Algebraic datatypes ( tuples, variants, etc... )

---

#### What kind of problems we can solve using metaprogramming ? (3/4)

Metaprogramming can be used:
* For selecting processing path based on type qualities 
    * Using memcpy instead of assignment operator for types that are trivially copyable 
    * Auto serialization/deserialization 

---

#### What kind of problems we can solve using metaprogramming ? (4/4)

Metaprogramming can be used:
* For optimisation 
    * Small buffer
    * Static polymorphism 
    * Enabling SSE using proper data layout and accessors
* For type safe type erasure

---

### Tacit style programming

What is Tacit programming ? 

Remember pipes ? 

```bash
ls -al | grep -i "sdl" | sort
```

Functional programming approach:

```cpp
const auto result = funA( funB( funC( data ) ) );
```

---

### Tacit style metaprogramming

--- 

### Old approach vs TMP

---

### Example of using templates for debugging

OpenGL function binding

```cpp
template < typename R, typename... Args, typename... TArgs >
auto gl_call( R ( *func )( Args... ), TArgs&&... args ) -> R
{
    const auto e0 = glGetError();
    R ret{0};

    if ( e0 == GL_NO_ERROR ) { 
        ret = func( static_cast< Args >( 
            std::forward< TArgs >( args ) )... ); }
    else { report_gl_dirty( e0 ); return ret; }

    const auto e1 = glGetError();
    if ( e1 != GL_NO_ERROR ) { report_gl_error( e1 ); }
    
    return ret;
}
```

--- 

### Example of using detection idiom 

---

### Example of using type erasure

* type erasure
    * type safe void* 

---

### Example of using metaprogramming for generating bindings

---

Summary

---

Thank You!
Questions ?

