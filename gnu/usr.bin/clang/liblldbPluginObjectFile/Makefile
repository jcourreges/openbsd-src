# $OpenBSD: Makefile,v 1.5 2021/12/17 14:55:46 patrick Exp $

LIB=	lldbPluginObjectFile
NOPIC=
NOPROFILE=

.include <bsd.own.mk>
SRCS=	BreakpadRecords.cpp \
	ELFHeader.cpp \
	MinidumpFileBuilder.cpp \
	ObjectFileBreakpad.cpp \
	ObjectFileELF.cpp \
	ObjectFileJIT.cpp \
	ObjectFileMachO.cpp \
	ObjectFileMinidump.cpp \
	ObjectFilePDB.cpp \
	ObjectFilePECOFF.cpp \
	PECallFrameInfo.cpp \
	WindowsMiniDump.cpp \
	ObjectFileWasm.cpp

ObjectFilePECOFF.o: ObjectFilePECOFFProperties.inc
ObjectFilePECOFFProperties.inc: ObjectFilePECOFFProperties.td
	${.OBJDIR}/../lldb-tblgen/lldb-tblgen -gen-lldb-property-defs \
		-I ${LLDB_SRCS}/source/Plugins/ObjectFile/PECOFF \
		-o ${.TARGET} ${.ALLSRC}

ObjectFilePECOFF.o: ObjectFilePECOFFPropertiesEnum.inc
ObjectFilePECOFFPropertiesEnum.inc: ObjectFilePECOFFProperties.td
	${.OBJDIR}/../lldb-tblgen/lldb-tblgen -gen-lldb-property-enum-defs \
		-I ${LLDB_SRCS}/source/Plugins/ObjectFile/PECOFF \
		-o ${.TARGET} ${.ALLSRC}

.PATH:	${.CURDIR}/../../../llvm/lldb/source/Plugins/ObjectFile/Breakpad
.PATH:	${.CURDIR}/../../../llvm/lldb/source/Plugins/ObjectFile/ELF
.PATH:	${.CURDIR}/../../../llvm/lldb/source/Plugins/ObjectFile/Mach-O
.PATH:	${.CURDIR}/../../../llvm/lldb/source/Plugins/ObjectFile/Minidump
.PATH:	${.CURDIR}/../../../llvm/lldb/source/Plugins/ObjectFile/PDB
.PATH:	${.CURDIR}/../../../llvm/lldb/source/Plugins/ObjectFile/PECOFF
.PATH:	${.CURDIR}/../../../llvm/lldb/source/Plugins/ObjectFile/JIT
.PATH:	${.CURDIR}/../../../llvm/lldb/source/Plugins/ObjectFile/wasm

CLEANFILES+=	ObjectFilePECOFFProperties.inc ObjectFilePECOFFPropertiesEnum.inc

install:
	@# Nothing here so far ...

.include <bsd.lib.mk>

CPPFLAGS+=	${LLDB_INCLUDES}
CPPFLAGS+=	${CLANG_INCLUDES}
