# $OpenBSD: Makefile,v 1.4 2020/08/03 14:45:26 patrick Exp $

LIB=	LLVMObjCopy
NOPROFILE=

CPPFLAGS+=	-I${.OBJDIR}/../include/llvm/ObjCopy \
		-I${LLVM_SRCS}/include/llvm/ObjCopy \
		-I${LLVM_SRCS}/lib/ObjCopy

SRCS+=	Archive.cpp \
	CommonConfig.cpp \
	ObjCopy.cpp \
	ConfigManager.cpp \
	COFFObjcopy.cpp \
	COFFObject.cpp \
	COFFReader.cpp \
	COFFWriter.cpp \
	ELFObjcopy.cpp \
	ELFObject.cpp \
	MachOObjcopy.cpp \
	MachOReader.cpp \
	MachOWriter.cpp \
	MachOLayoutBuilder.cpp \
	MachOObject.cpp \
	WasmObject.cpp \
	WasmReader.cpp \
	WasmWriter.cpp \
	WasmObjcopy.cpp \
	XCOFFReader.cpp \
	XCOFFWriter.cpp \
	XCOFFObjcopy.cpp

.PATH: ${.CURDIR}/../../../llvm/llvm/lib/ObjCopy
.PATH: ${.CURDIR}/../../../llvm/llvm/lib/ObjCopy/COFF
.PATH: ${.CURDIR}/../../../llvm/llvm/lib/ObjCopy/ELF
.PATH: ${.CURDIR}/../../../llvm/llvm/lib/ObjCopy/MachO
.PATH: ${.CURDIR}/../../../llvm/llvm/lib/ObjCopy/wasm
.PATH: ${.CURDIR}/../../../llvm/llvm/lib/ObjCopy/XCOFF

install:
	@# Nothing here so far ...

.include <bsd.lib.mk>
