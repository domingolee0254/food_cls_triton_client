# **Triton Client for Food Classification**

---

## Usage

### make client docker container

```bash
docker run -it --net=host -e LC_ALL=C.UTF-8 -v /media/mmlab/hdd/client:/clinet nvcr.io/nvidia/tritonserver:22.10-py3-sdk
```

### Run python script

```bash
root@mmlab-GTX1080Ti-orange:/workspace# python /home/client/src/python/image_client.py -m food_onnx -c 1 /clinet/test_data/
```

### Result for test data

```bash
======================================================================================================================================================
Request 4000th images, batch size 1
IMAGE: /home/client/test/후랑크소시지/A270408XX_30714_1.jpg
GT: 후랑크소시지
PRED: 후랑크소시지
final accuracy: 93.70%

==================================================

final accuracy: 93.70%

==================================================
```