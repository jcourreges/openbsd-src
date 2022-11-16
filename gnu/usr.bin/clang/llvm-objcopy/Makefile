# $OpenBSD: Makefile,v 1.2 2021/12/17 14:55:47 patrick Exp $

.include <bsd.own.mk>

PROG=	llvm-objcopy
BINDIR=	/usr/bin
LIBEXECDIR=/usr/libexec

SRCS=	ObjcopyOptions.cpp \
	llvm-objcopy.cpp \
	main.cpp

CPPFLAGS+=	-I${.OBJDIR}/../include/llvm-objcopy
CPPFLAGS+=	-I${.CURDIR}/../../../llvm/llvm/tools/llvm-objcopy
CPPFLAGS+=	${CPPFLAGS_$*}

.PATH:	${.CURDIR}/../../../llvm/llvm/tools/llvm-objcopy

LLVM_LIBDEPS=	LLVM LLVMObjCopy

LDADD+= -L ${.OBJDIR}/../libLLVM -lLLVM

.include <bsd.prog.mk>
