# YOLOv11 with Knowledge Distillation

<div align="center">
  <p>
    <a href="https://www.ultralytics.com/events/yolovision" target="_blank">
      <img width="100%" src="https://raw.githubusercontent.com/ultralytics/assets/main/yolov8/banner-yolov8.png" alt="YOLO Vision banner">
      </a>
  </p>
</div>



## How to Run

Example:

```
pip install -r requirements.txt
```

```
from ultralytics import YOLO

teacher_model = YOLO("<teacher-path>")

student_model = YOLO("yolo11n.pt)

student_model.train(
    data="<data-path>",
    teacher=teacher_model.model, # None if you don't wanna use knowledge distillation
    distillation_loss="cwd",
    epochs=100,
    batch=16,
    workers=0,
    exist_ok=True,
)
```

## Credits
```
@software{Jocher_Ultralytics_YOLO_2023,
  author = {Jocher, Glenn and Qiu, Jing and Chaurasia, Ayush},
  license = {AGPL-3.0},
  month = jan,
  title = {{Ultralytics YOLO}},
  url = {https://github.com/ultralytics/ultralytics},
  version = {8.0.0},
  year = {2023}
}
```