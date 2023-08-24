## 环境
segformer_pt1.11  

## onnx模型 包含nms
    python export.py --weights yolov7-e6.pt --grid --end2end --simplify --topk-all 100 --iou-thres 0.65 --conf-thres 0.25 --img-size 640 640 --max-wh 640  
    model是  yolov7-e6_with_nms.onnx  
    推理运行  test_onnx_with_nms.py  

## onnx模型 不包含nms
    python export.py --weights yolov7-e6.pt --grid --img-size 640 640  
    model是  yolov7-e6_without_nms.onnx  
    推理运行  test_onnx_without_nms.py  
    精度统计 val_onnx.py  