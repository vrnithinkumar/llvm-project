add_llvm_library(MLIRStandardToLLVM
  ConvertStandardToLLVM.cpp

  ADDITIONAL_HEADER_DIRS
  ${MLIR_MAIN_INCLUDE_DIR}/mlir/Conversion/StandardToLLVM
)
add_dependencies(
  MLIRStandardToLLVM

  MLIRLLVMIR
  MLIRTransforms
  LLVMCore
  LLVMSupport
)
target_link_libraries(
  MLIRStandardToLLVM

  MLIRLLVMIR
  MLIRTransforms
  LLVMCore
  LLVMSupport
)
