# Tasks
A list of tasks to modernize old Fortran code.

1. Change type*n to type( ktp ).
2. Common blocks to Fortran modules.
   Also must work with equivalance
3. Cray pointers to Fortran pointers.

I'd like to suggest that items to change be categorized
according to whether it ever was standard or not.
So type*n was never standard and common/equivalance was.

Archaic (was standard but now yucky)
1. common/equivalance
2. pause
3. hollerith
4. anything to do with statement labels
   three-way ifs, alternate return, error branchs

Extensions (was never standard and now still yucky)
1. type*n
2. cray pointers to standard pointers
3. encode/decode
4. buffer in/buffer out

I think that any tool a user sees should have a basic workflow
of test-->change-->test
so there's a basis for user confidence.
Of course, the flip side is that a user may have a lot of files to process,
and so isn't interested in a manual, interactive approach.  So there should
also be a batch mode.

