# $OpenBSD: Makefile,v 1.3 2020/08/03 14:45:28 patrick Exp $

LIB=	clangExtractAPI
NOPIC=
NOPROFILE=

CPPFLAGS+=	${CLANG_INCLUDES}

.include <bsd.own.mk>
SRCS=	API.cpp \
	ExtractAPIConsumer.cpp \
	DeclarationFragments.cpp \
	SerializerBase.cpp \
	SymbolGraphSerializer.cpp \
	TypedefUnderlyingTypeResolver.cpp

.PATH:	${.CURDIR}/../../../llvm/clang/lib/ExtractAPI
.PATH:	${.CURDIR}/../../../llvm/clang/lib/ExtractAPI/Serialization

install:
	@# Nothing here so far ...

.include <bsd.lib.mk>
