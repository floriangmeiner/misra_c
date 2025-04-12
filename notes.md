# Short Notes on MISRA C Rulesa

These notes come from a review of the document [MISRA-C:2004 - Guidelines for 
the use of the C language in critical systems](./resources/ebook/misra-c-2004.pdf) 
and an attempt to oversimplify the "rules" for quick ingestion. 

## Environment

### Rule 1.1:
**REQUIRED** Use an ISO/IEC compliant C standard.


### Rule 1.2:
**REQUIRED** Don't really on *UNDEFINED* or *UNSPECIFIED* behaviour.


### Rule 1.3:
**REQUIRED** Only use a single compiler and/or language. 


### Rule 1.4:
**REQUIRED** Check the compiler & linker to make sure that 31 character 
significance *and* case sensitivity are supported for external identifiers.


### Rule 1.5:
**Advised** Floating point implementations should comply with a defined standard.


## Language Extenions

### Rule 2.1
**REQUIRED** Assembly language should be encapsulated and isolated.

*aka* Put assembly in separate files, don't mix with C. 


### Rule 2.2
**REQUIRED** Source code shall only use `/* .... */` comment style.


### Rule 2.3
**REQUIRED** No nesting of comments. Don't use `/*` in a comment.


### Rule 2.4
**Advised** Don't comment out code. Use conditional compilation, if sections 
need to be exluded from compilation. (e.g. `#ifdef` `#endif`)


## Documentation

### Rule 3.1
**REQUIRED** Document all usage implementation-defined behaviours.


### Rule 3.2
**REQUIRED** Document the character set and encoding used. 


### Rule 3.3
**Advised** Document the implementation of integer division used by the chosen 
compiler. 


### Rule 3.4
**REQUIRED** Document *and* explain all uses of the `#pragma` directive. 


### Rule 3.5
**REQUIRED** If used, document that implementation-defined behaviour and packing
of bitfields. 


### Rule 3.6
**REQUIRED** All libraries using in *production code* shall be written to comply
with MISRA-C and shall be appropriately validated. 


## Character Set

### Rule 4.1
**REQUIRED** Only ISO C standard escape sequences shall be used. 


### Rule 4.2
**REQUIRED** Trigraphs shall not be used. (e.g. `??=`, `??/`, `??'`, `??(`, etc)


## Identifiers

### Rule 5.1
**REQUIRED** All names should be less than 31 characters in length. 
> Identifiers (internal and external) shall not rely on the 
> significance of more that 31 characters.


### Rule 5.2
**REQUIRED** Identifiers in an inner scope, must have a different name from 
identifiers in the outer scope. 

*aka* *Always* use unique variable names, **EVERYWHERE** (including for-loop
index values!) for clarity. 


### Rule 5.3
**REQUIRED** A `typedef` name must have a unique name (aka *identifier*).


### Rule 5.4
**REQUIRED** A *tag* of a `struct` or `union` must have a unique name (aka
*identifier*).

### Rule 5.5
**Advised** No object or function identifier with static storage duration should
be reused.

`Get clarity here`

