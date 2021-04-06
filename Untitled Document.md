# C ++11/C ++14 features:

1) Feature: keyword “auto” ( is a feature of c++11 and is also a part of “Type inference” i.e., the data type of its variable is declared at compile time).
Directory: llvm-project/llvm/lib/Analysis/AliasAnalysis.cpp
Here, they have used the keyword “auto” (which is used to initialize the variable automatically without any keyword declaration) in line179.

2) Feature: keyword “nullptr” (is a feature of c++11 and is used to represent a null pointer value)
Directory: llvm-project/llvm/lib/Analysis/CFLGraph.h
Here, they have used nullptr to check whether the pointer “Info” points to a null pointer or not.

3) Feature: Inline function.
Directory: llvm-project/llvm/lib/Analysis/AliasAnalysisSummary.h. Hare, they have used an inline function which reduces the overload of function calls.
 

 # Class Hierarchy:
In general, the LLVM follows the class hierarchy as:
1) Module class: is the primitive class, it contains the information of functions, global variables.
2) Value class: contains information about constants, variables, etc.
3) User class: is a derived-class of Value class.
			In the directory: llvm-project/llvm/include/llvm/IR/User.h, it is clear 
			that User class is a derived class of Value class
			
4) Instruction class: is derived from User class
In the directory: llvm-project/llvm/include/llvm/IR/Instruction.h, it is clear that Instruction class is a derived class of User class
			
5) Operator class: is derived from User class
 In the directory: llvm-project/llvm/include/llvm/IR/Operator.h, it is clear that Instruction class is a derived class of User class

6) Constant class: is derived from User class
 In the directory: llvm-project/llvm/include/llvm/IR/Constant.h, it is clear that Instruction class is a derived class of User class 
			

# OOP design decisions for LLVM:

 1) Feature: Function overloading
Directory: llvm-project/llvm/lib/Analysis/AliasAnalysis.cpp
Here, they have used “function overloading” in lines 161 and 167 for the sake of easy implementation.
	
1) Feature: Inheritance
Directory: llvm-project/llvm/include/llvm/ADT/SmallSet.h
Here, they have used inheritance in line 33 and inherited the data and instruction of the class “iterator_facade_base” into class “SmallSetIterator”.

# Design Patterns:

The most observed Design pattern is the visitor pattern.
1) Visitor pattern: it is the widely used design pattern. This pattern is used when we want to traverse an entire structure and to make some modifications to each element of the structure.

# Usage of iterators and their own data structures:

1) Feature: using Iterators of data structure “DenseMap” 
Directory: llvm-project/llvm/lib/Analysis/CFLGraph.h.
Here, they have used iterators in line 110, and the declaration of ValueMap is done in line 98.
 
2)  Feature: using iterators of data structure “SetVector”
Directory:llvm-project/llvm/lib/Analysis/AliasAnalysisEvaluator.cpp
Here, they have used iterators for the data structure “SetVector” in line 139 to traverse the array “Pointers”.


