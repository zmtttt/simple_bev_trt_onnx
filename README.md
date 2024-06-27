# simple_bev_trt_onnx
(1)simple_bev_modle to onnx, add plugin register for grdisample3d, give solutions of unrecognizing instancenormalization2d(modify model:torch.nn.instance....)；
(2)divide model to four sub-models , model2 is def, just caculating ,  so to skip it, using pth to loading it.  this method has the same performance 
(3)three sub-models to onnx, to simplify ,using trtexec to build engine ,the inference_time decreasing 10times and mantaining the same performance
(4)coding toengine.py  , the three sub-models onnx to fp16,int8 engine,and evaluting it;
(5)post process
