# $OpenBSD: Makefile,v 1.6 2021/12/17 14:55:45 patrick Exp $

LIB=	LLVMAMDGPUTargetMCA
NOPROFILE=

CPPFLAGS+=	-I${.OBJDIR}/../include/llvm/AMDGPU \
		-I${LLVM_SRCS}/lib/Target/AMDGPU

SRCS+=	AMDGPUCustomBehaviour.cpp

.PATH:	${.CURDIR}/../../../llvm/llvm/lib/Target/AMDGPU/MCA
