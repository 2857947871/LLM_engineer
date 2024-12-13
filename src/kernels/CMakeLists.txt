add_library(embeddingFunctor STATIC input_embedding.cu)
set_property(TARGET embeddingFunctor PROPERTY CUDA_SEPARABLE_COMPILATION   ON)
set_property(TARGET embeddingFunctor PROPERTY POSITION_INDEPENDENT_CODE  ON)
set_property(TARGET embeddingFunctor PROPERTY CUDA_RESOLVE_DEVICE_SYMBOLS  ON)

add_library(rmsnorm STATIC rmsnorm_kernel.cu)
set_property(TARGET rmsnorm PROPERTY CUDA_SEPARABLE_COMPILATION   ON)
set_property(TARGET rmsnorm PROPERTY POSITION_INDEPENDENT_CODE  ON)
set_property(TARGET rmsnorm PROPERTY CUDA_RESOLVE_DEVICE_SYMBOLS  ON)

add_library(cal_paddingoffset STATIC cal_paddingoffset.cu)
set_property(TARGET cal_paddingoffset PROPERTY CUDA_SEPARABLE_COMPILATION   ON)
set_property(TARGET cal_paddingoffset PROPERTY POSITION_INDEPENDENT_CODE  ON)
set_property(TARGET cal_paddingoffset PROPERTY CUDA_RESOLVE_DEVICE_SYMBOLS  ON)

add_library(build_casual_mask STATIC build_casual_mask.cu)
set_property(TARGET build_casual_mask PROPERTY CUDA_SEPARABLE_COMPILATION   ON)
set_property(TARGET build_casual_mask PROPERTY POSITION_INDEPENDENT_CODE  ON)
set_property(TARGET build_casual_mask PROPERTY CUDA_RESOLVE_DEVICE_SYMBOLS  ON)

add_library(cublas_utils STATIC cublas_utils.cc)
set_property(TARGET cublas_utils PROPERTY POSITION_INDEPENDENT_CODE  ON)
set_property(TARGET cublas_utils PROPERTY CUDA_RESOLVE_DEVICE_SYMBOLS  ON)

add_library(linear_lib STATIC linear.cu)
set_property(TARGET linear_lib PROPERTY CUDA_SEPARABLE_COMPILATION   ON)
set_property(TARGET linear_lib PROPERTY POSITION_INDEPENDENT_CODE  ON)
set_property(TARGET linear_lib PROPERTY CUDA_RESOLVE_DEVICE_SYMBOLS  ON)
target_link_libraries(linear_lib PUBLIC -lcudart -lcublas cublas_utils)

add_library(qkv_bias_and_rope STATIC qkv_bias_and_RoPE.cu)
set_property(TARGET qkv_bias_and_rope PROPERTY CUDA_SEPARABLE_COMPILATION   ON)
set_property(TARGET qkv_bias_and_rope PROPERTY POSITION_INDEPENDENT_CODE  ON)
set_property(TARGET qkv_bias_and_rope PROPERTY CUDA_RESOLVE_DEVICE_SYMBOLS  ON)

add_library(concat_kv STATIC concat_past_kv.cu)
set_property(TARGET concat_kv PROPERTY CUDA_SEPARABLE_COMPILATION   ON)
set_property(TARGET concat_kv PROPERTY POSITION_INDEPENDENT_CODE  ON)
set_property(TARGET concat_kv PROPERTY CUDA_RESOLVE_DEVICE_SYMBOLS  ON)

add_library(repeat_kv STATIC repeat_kv.cu)
set_property(TARGET repeat_kv PROPERTY CUDA_SEPARABLE_COMPILATION   ON)
set_property(TARGET repeat_kv PROPERTY POSITION_INDEPENDENT_CODE  ON)
set_property(TARGET repeat_kv PROPERTY CUDA_RESOLVE_DEVICE_SYMBOLS  ON)

add_library(mask_softmax STATIC attn_softmax_kernel.cu)
set_property(TARGET mask_softmax PROPERTY CUDA_SEPARABLE_COMPILATION   ON)
set_property(TARGET mask_softmax PROPERTY POSITION_INDEPENDENT_CODE  ON)
set_property(TARGET mask_softmax PROPERTY CUDA_RESOLVE_DEVICE_SYMBOLS  ON)

add_library(fused_transpose_and_remv_pad STATIC fused_transpose_and_remv_pad.cu)
set_property(TARGET fused_transpose_and_remv_pad PROPERTY CUDA_SEPARABLE_COMPILATION   ON)
set_property(TARGET fused_transpose_and_remv_pad PROPERTY POSITION_INDEPENDENT_CODE  ON)
set_property(TARGET fused_transpose_and_remv_pad PROPERTY CUDA_RESOLVE_DEVICE_SYMBOLS  ON)

add_library(fused_addresidual_norm STATIC fused_addresidual_norm.cu)
set_property(TARGET fused_addresidual_norm PROPERTY CUDA_SEPARABLE_COMPILATION   ON)
set_property(TARGET fused_addresidual_norm PROPERTY POSITION_INDEPENDENT_CODE  ON)
set_property(TARGET fused_addresidual_norm PROPERTY CUDA_RESOLVE_DEVICE_SYMBOLS  ON)

add_library(act_kernel STATIC act_kernel.cu)
set_property(TARGET act_kernel PROPERTY CUDA_SEPARABLE_COMPILATION   ON)
set_property(TARGET act_kernel PROPERTY POSITION_INDEPENDENT_CODE  ON)
set_property(TARGET act_kernel PROPERTY CUDA_RESOLVE_DEVICE_SYMBOLS  ON)

add_library(topk STATIC topK.cu)
set_property(TARGET topk PROPERTY CUDA_SEPARABLE_COMPILATION   ON)
set_property(TARGET topk PROPERTY POSITION_INDEPENDENT_CODE  ON)
set_property(TARGET topk PROPERTY CUDA_RESOLVE_DEVICE_SYMBOLS  ON)

add_library(fused_decoder_self_attention STATIC fused_decoder_self_attention.cu)
set_property(TARGET fused_decoder_self_attention PROPERTY CUDA_SEPARABLE_COMPILATION   ON)
set_property(TARGET fused_decoder_self_attention PROPERTY POSITION_INDEPENDENT_CODE  ON)
set_property(TARGET fused_decoder_self_attention PROPERTY CUDA_RESOLVE_DEVICE_SYMBOLS  ON)

add_library(sampling STATIC sampling.cu)
set_property(TARGET sampling PROPERTY CUDA_SEPARABLE_COMPILATION   ON)
set_property(TARGET sampling PROPERTY POSITION_INDEPENDENT_CODE  ON)
set_property(TARGET sampling PROPERTY CUDA_RESOLVE_DEVICE_SYMBOLS  ON)

add_library(add_residual STATIC add_residual.cu)
set_property(TARGET add_residual PROPERTY CUDA_SEPARABLE_COMPILATION   ON)
set_property(TARGET add_residual PROPERTY POSITION_INDEPENDENT_CODE  ON)
set_property(TARGET add_residual PROPERTY CUDA_RESOLVE_DEVICE_SYMBOLS  ON)