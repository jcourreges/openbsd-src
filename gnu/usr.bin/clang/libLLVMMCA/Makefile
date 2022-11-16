# $OpenBSD: Makefile,v 1.10 2021/12/17 14:55:45 patrick Exp $

LIB=	LLVMMCA
NOPROFILE=

CPPFLAGS+=	-I${LLVM_SRCS}/include/llvm/MCA

SRCS+=	CodeEmitter.cpp \
	Context.cpp \
	CustomBehaviour.cpp \
	HWEventListener.cpp \
	HardwareUnit.cpp \
	LSUnit.cpp \
	RegisterFile.cpp \
	ResourceManager.cpp \
	RetireControlUnit.cpp \
	Scheduler.cpp \
	IncrementalSourceMgr.cpp \
	InstrBuilder.cpp \
	MCAInstruction.cpp \
	Pipeline.cpp \
	DispatchStage.cpp \
	EntryStage.cpp \
	ExecuteStage.cpp \
	InOrderIssueStage.cpp \
	InstructionTables.cpp \
	MicroOpQueueStage.cpp \
	RetireStage.cpp \
	Stage.cpp \
	Support.cpp \
	View.cpp

MCAInstruction.cpp:
	ln -s ${LLVM_SRCS}/lib/MCA/Instruction.cpp $@

.PATH:	${.CURDIR}/../../../llvm/llvm/lib/MCA
.PATH:	${.CURDIR}/../../../llvm/llvm/lib/MCA/HardwareUnits
.PATH:	${.CURDIR}/../../../llvm/llvm/lib/MCA/Stages

CLEANFILES+=	MCAInstruction.cpp
