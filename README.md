# tensorflow_GPU_guide(텐서플로우 설치 가이드)
* 텐서플로우 GPU사용을 위해 설치하면서 많은 오류로 인해 또 설치가 성공적으로 되어 그래픽카드 인식을 하여도 다른 오류로 진행이 되지 않는 등.. 어려움을 겪었습니다. 부디 다른분들은 오류없이 바로 사용하실 수 있도록 하는 마음에 정리하여 보았습니다.


### NVIDIA GPU 드라이버 설치(install NVIDIA GPU Driver)
![NVIDIA_GPU_DRIVER](https://user-images.githubusercontent.com/39722575/204004320-f6f368a7-5d68-4a5a-9da1-1dceabbb2d25.PNG)
* 자신의 제품에 맞게 드라이버 다운로드 https://www.nvidia.co.kr/Download/index.aspx?lang=kr
## CUDA 설치
* cmd창에 nvidia-smi검색

![NVIDIA_GPU_VERSION](https://user-images.githubusercontent.com/39722575/204002507-e3ae8ad5-36f7-4162-b2aa-612ff10f4f0c.PNG)

* **CUDA : 11.7 ->  CUDA 11.7을 설치해야 한다.** - 밑에 추가는 참조 11.7 설치해야 한다.
* <추가> NVIDIA GPU driver와 CUDA호환표 https://docs.nvidia.com/cuda/cuda-toolkit-release-notes/index.html\
* <추가> NVIDIA GPU 그래픽카드 https://ko.wikipedia.org/wiki/CUDA

## CUDA Toolkit Archive 설치
![CUDA](https://user-images.githubusercontent.com/39722575/204006015-fc679c67-4d80-4228-bffc-fdaa7b083222.PNG)
* cmd창에서 확인했던 버전 다운로드 https://developer.nvidia.com/cuda-toolkit-archive 11.7 11.7.1 둘다 가능합니다.
* 저는 11.7.0으로 다운로드 받았습니다.
## cuDNN 설치
![cuDnn](https://user-images.githubusercontent.com/39722575/204006675-3f00aa63-40e8-4a9e-beba-46564462160f.PNG)
* CUDA와 버전이 맞는 cuDNN을 설치하시면 됩니다. https://developer.nvidia.com/rdp/cudnn-archive
* 저는 같은 날짜인 **Download cuDNN v8.4.1 (May 27th, 2022), for CUDA 11.x** 을 다운 받았습니다.

### cuDNN CUDA에 붙여넣기

![cudnn파일](https://user-images.githubusercontent.com/39722575/204008431-021d8631-d6e2-417a-9082-8153f3568a1f.PNG)

* 다운받으신 파일의 압축을 푸시고 

![three file](https://user-images.githubusercontent.com/39722575/204008467-61aeb7f8-c6d6-4cfd-8d1d-f5edd707a779.PNG)

* 세개의 파일을 확인합니다. - 복사합니다.

![version](https://user-images.githubusercontent.com/39722575/204008450-d91573e9-58b1-45b4-b5ff-916065135608.PNG)

* **C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.7(다운 받으신 버전)** 에 붙여넣기 하시면 됩니다.

![덮어쓰기](https://user-images.githubusercontent.com/39722575/204008918-e45c5162-1d6f-4d54-8b1f-70889ff71b25.PNG)
* 위 bin, lib, include에 덮어쓰는 것입니다.

### 시스템 환경 변수 적용
* 시작에서 시스템 환경 변수 실행시킵니다.


![시스템 변수](https://user-images.githubusercontent.com/39722575/204010255-3e0b4f4a-4114-48fe-98cd-6da3984f76c2.PNG)
* 시스템 변수 아래쪽 CUDA_PATH 두개가 잘되어있는지 확인하시고 설치시 버전에 맞게 자동으로 지정되어있습니다.
* 저희는 PATH의 경로설정을 합니다.

![three path](https://user-images.githubusercontent.com/39722575/204010261-50ed0045-7715-4729-8640-ade666379ee7.PNG)
* 다음 세개의 경로를 추가합니다.
* C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.7\lib
* C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.7\bin
* C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.7\inclue


### visual studio jupyter notebook 확인
![gpu연결확인](https://user-images.githubusercontent.com/39722575/205069902-1bb27fdb-a67b-4358-84dc-59ca1a730b73.PNG)

다음과 같이 인식하는 것을 확인하실 수 있습니다.


# 오류
### zlibwapi.dll error
![tensorflow_error_zlibwapi](https://user-images.githubusercontent.com/39722575/204003032-61b15473-0e3f-4f95-82e7-501367528247.PNG)

* 다음 오류는 bin폴더에 zlibwapi.dll 파일이 없어서 생긴 오류입니다.

### 해결

![dll](https://user-images.githubusercontent.com/39722575/204011099-21f72b54-5f68-4040-9e15-eb33e1ee1627.PNG)
* 다음 사이트를 통해 **64bit => ZLIB DLL // 32bit => 32-bit ZLIB DLL** 을 클릭하셔서 다운받으시고 zlibwapi.dll파일만 복사하여
* C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.7\bin 경로에 붙여넣기 하시면 됩니다.  
