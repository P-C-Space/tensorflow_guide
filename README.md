# tensorflow_GPU_guide(텐서플로우 설치 가이드)
* 텐서플로우 GPU사용을 위해 설치하면서 많은 오류로 인해 설치가 되었음에도 나중에 다른 오류로 진행이 되지 않았습니다.
* 부디 다른분들은 오류없이 바로 사용하실 수 있도록 하는 마음에 정리하여 보았습니다.


### NVIDIA GPU 드라이버 설치(install NVIDIA GPU Driver)
![NVIDIA_GPU_DRIVER](https://user-images.githubusercontent.com/39722575/204004320-f6f368a7-5d68-4a5a-9da1-1dceabbb2d25.PNG)
* 자신의 제품에 맞게 드라이버 다운로드
### CUDA 설치
* cmd창에 nvidia-smi검색

![NVIDIA_GPU_VERSION](https://user-images.githubusercontent.com/39722575/204002507-e3ae8ad5-36f7-4162-b2aa-612ff10f4f0c.PNG)

* **CUDA : 11.7 ->  CUDA 11.7을 설치해야 한다.** - 밑에 추가는 참조 11.7 설치해야 한다.
* <추가> NVIDIA GPU driver와 CUDA호환표 https://docs.nvidia.com/cuda/cuda-toolkit-release-notes/index.html\
* <추가> NVIDIA GPU 그래픽카드 https://ko.wikipedia.org/wiki/CUDA

#### CUDA Toolkit Archive 설치
![CUDA](https://user-images.githubusercontent.com/39722575/204006015-fc679c67-4d80-4228-bffc-fdaa7b083222.PNG)
* cmd창에서 확인했던 버전 다운로드 https://developer.nvidia.com/cuda-toolkit-archive 11.7 11.7.1 둘다 가능합니다.
* 저는 11.7.0으로 다운로드 받았습니다.
#### cuDNN 설치
![cuDnn](https://user-images.githubusercontent.com/39722575/204006675-3f00aa63-40e8-4a9e-beba-46564462160f.PNG)

<br>
* https://developer.nvidia.com/rdp/cudnn-archive


# 오류
### zlibwapi.dll error
![tensorflow_error_zlibwapi](https://user-images.githubusercontent.com/39722575/204003032-61b15473-0e3f-4f95-82e7-501367528247.PNG)
