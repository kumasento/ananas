# ananas
Ananas is a key-value framework just like the VFS on Linux, it is supposed to manage the various key-value stores and provide the user a uniform key-value interface.

Key Value Framework
============================

http://

Overview
--------
  Key Value Framework defined a programming frame work according to generic key-value storage data model, 
storage provides pools, and pool provides objects. Actually there are lots of key-value storage open 
source project among different domains, from HDD/Flash to NOSQL, and almost everyone has its own API 
definitions, applications need write lots of adaptive layer to use these key value storage even they 
has the same semantics. Key Value Framework provides the APIs semantics definition based on the generic 
key value storage data model, including the function name and parameters. Then applications will use 
unified API to access different key value storage, just like applications access different file system 
by virtual file system. As a result, it makes the key value based application programming simple.


Requirements for End Users
--------------------------
### Linux Requirements ###
  * GNU-compatible Make or gmake
  * libtools

Install
--------------------------
### Linux Install ###
For linux user, just simply run:

 autoconf
 ./configure
 make & make install

Limitation
--------------------------
 *Currently, KVF can only run on linux, for other platforms could be supported later.
 *Some common mechanism will be implemented soon. 
 
Guide to header files
--------------------------
include/kvf/kvf_api.h
    Main interface to kvf.

include/kvf/kvf.h
    The data structures defined in kvf.

include/kvf/kvf_err_code.h
    Common error codes are all put here.

include/kvf/kvf_type.h
    Basic typedefs.

include/kvf_list.h
	A simple list implementation.