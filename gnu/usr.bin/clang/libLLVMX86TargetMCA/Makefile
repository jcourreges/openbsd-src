# $OpenBSD: Makefile,v 1.6 2021/12/17 14:55:45 patrick Exp $

LIB=	LLVMX86TargetMCA
NOPROFILE=

CPPFLAGS+=	-I${.OBJDIR}/../include/llvm/X86 \
		-I${LLVM_SRCS}/lib/Target/X86

SRCS+=	X86CustomBehaviour.cpp

.PATH:	${.CURDIR}/../../../llvm/llvm/lib/Target/X86/MCA
