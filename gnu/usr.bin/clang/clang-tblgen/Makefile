# $OpenBSD: Makefile,v 1.9 2021/12/17 14:55:44 patrick Exp $

PROG=	clang-tblgen
NOMAN=

CPPFLAGS+=	${CLANG_INCLUDES}

.include <bsd.own.mk>
SRCS=	ASTTableGen.cpp \
	ClangASTNodesEmitter.cpp \
	ClangASTPropertiesEmitter.cpp \
	ClangAttrEmitter.cpp \
	ClangCommentCommandInfoEmitter.cpp \
	ClangCommentHTMLNamedCharacterReferenceEmitter.cpp \
	ClangCommentHTMLTagsEmitter.cpp \
	ClangDataCollectorsEmitter.cpp \
	ClangDiagnosticsEmitter.cpp \
	ClangOpcodesEmitter.cpp \
	ClangOpenCLBuiltinEmitter.cpp \
	ClangOptionDocEmitter.cpp \
	ClangSACheckersEmitter.cpp \
	ClangSyntaxEmitter.cpp \
	ClangTypeNodesEmitter.cpp \
	MveEmitter.cpp \
	NeonEmitter.cpp \
	RISCVVEmitter.cpp \
	RISCVVIntrinsicUtils.cpp \
	SveEmitter.cpp \
	TableGen.cpp

.PATH:	${.CURDIR}/../../../llvm/clang/lib/Support
.PATH:	${.CURDIR}/../../../llvm/clang/utils/TableGen

LLVM_LIBDEPS=	LLVMTableGen LLVMSupport

install:
	@# Nothing here so far ...

.include <bsd.prog.mk>
