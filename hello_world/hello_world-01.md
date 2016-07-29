**hello-world-0.c**: A program that prints <code>Hello, World!</code>.

    /* hello-world-0.c: basically just prints "Hello, world!" */
    /* Imports required library to use printf(); */
    /* #include <stdio.h> */
    #include <stdio.h>
    
    /* main function */
    int main(void) { /* int main(void) { */
        /* displays "Hello, world!" */
        printf("Hello, world!\n"); /* printf("Hello, world!"); */
  
        /* Tells the computer that the program ran as intended */
        return 0; /* return 0; */
    } /* } */

**hello-world-0_generic**: A program converted to generic *Assembly* that prints <code>Hello, World!</code>.

    	.file	"hello-world-0.c"
    	.section	.rodata
    .LC0:
    	.string	"Hello, world!"
    	.text
    	.globl	main
    	.type	main, @function
    main:
    .LFB0:
    	.cfi_startproc
    	pushq	%rbp
    	.cfi_def_cfa_offset 16
    	.cfi_offset 6, -16
    	movq	%rsp, %rbp
    	.cfi_def_cfa_register 6
    	movl	$.LC0, %edi
    	call	puts
    	movl	$0, %eax
    	popq	%rbp
    	.cfi_def_cfa 7, 8
    	ret
    	.cfi_endproc
    .LFE0:
    	.size	main, .-main
    	.ident	"GCC: (Ubuntu 5.3.1-14ubuntu2.1) 5.3.1 20160413"
    	.section	.note.GNU-stack,"",@progbits
