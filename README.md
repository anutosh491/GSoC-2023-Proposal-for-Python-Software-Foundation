# GSoC-2023-Proposal-for-Python-Software-Foundation
Link to my proposal - https://blogs.python-gsoc.org/media/proposals/PSF_LPython_GSoC_2023_Proposal.pdf

Title : Implementing Symbolic Algorithms as a part of ASR
Abstract
* The idea here is to provide both runtime support (preferably using the SymEngine library to provide the computation, as it is fast and robust) and compile time support (in ASR) to implement Symbolic Algorithms in LPython. 
* The runtime operation could use the SymEngine library for LLVM, C and C++ backends. For Python backend, we can simply use SymPy itself. * The algorithms would be implemented in the ASR code, which would make them independent of any specific frontend. Any frontend that uses the ASR code could then make use of the symbolic algorithms without having to reimplement them. 
* LPython, in this case, would not implement the symbolic algorithms themselves, but would instead parse the syntax used by the SymPy library, which already has a rich set of symbolic algorithms, and use the ASR representation of these expressions to perform various operations. This would allow LPython to have powerful symbolic manipulation capabilities without having to reinvent the wheel.
