# Darknet

<br/>
##  설치
Git으로 부터 해당 프로젝트를 다운받고 해당 프로젝트 폴더로 이동합니다.
```sh
$ git clone https://github.com/Deeptector/Darknet.git
$ cd Darknet
```
  
OpenCV와 GPU를 사용할 수 있도록 Makefile을 수정합니다.
```sh
$ vi Makefile
```
```sh
GPU=0
CUDNN=0
OPENCV=0
OPENMP=0
DEBUG=0
...
```

편집기 모드로 들어가면 위와 같이 CPU, CUDNN, OPENCV가 모두 0으로 되어있습니다.  
GPU, CUDNN, OPENCV를 1로 변경합니다.

다음은 변경 후 Makefile입니다.
```sh
GPU=1
CUDNN=1
OPENCV=1
OPENMP=0
DEBUG=0
...
```

make 명령어를 통하여 빌드를 진행합니다.
```sh
$ make
```