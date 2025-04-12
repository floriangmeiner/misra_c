# Short Notes on MISRA C Rulesa

These notes come from a review of the document [MISRA-C:2004 - Guidelines for
the use of the C language in critical systems](./ebook/misra-c-2004.pdf) and 
an attempt to oversimplify the "rules" for quick ingestion. 

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
**REQUIRED** 