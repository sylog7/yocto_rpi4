# module autoload

https://xilinx-wiki.atlassian.net/wiki/spaces/A/pages/96960682/Linux+Loadable+Kernel+Modules
 - udev를 사용하는 방법
 - udev가 특정 모듈을 자동으로 로드하지 못하도록 하는 방법
 - udev를 사용하지 않고 자동으로 로드하도록 하는 방법:
   이 방법은 systemd를 사용하는 듯하다.

## KERNEL_MODULE_AUTOLOAD
[yocto dosc - KERNEL_MODULE_AUTOLOAD](https://docs.yoctoproject.org/2.5/ref-manual/ref-manual.html#var-KERNEL_MODULE_AUTOLOAD)

커널 레시피에 써야한다고 해서 linux-*.bbappend에 추가했으나 안됨..  
이미지 레시피 또는 local.conf에 써야하나 싶어서 찾아보니 커널 모듈 레시피에 쓰면 된다고 한다.  
[stackoverflow - yocto-load-kernel-module](https://stackoverflow.com/questions/59629344/yocto-load-kernel-module)

문서 상으로는 modulename.conf가 /etc/modules-load.d/modname.conf 경로에 생성된다고 하지만  
실제로 해보면 /usr/lib/modules-load.d/modname.conf 로 생성된다.  

## 참고
KERNEL_MODULE_AUTOLOAD 가 동작하지 않아서 찾아본 내용..
xilinx(amd)에 좋은 자료가 많다.  
https://adaptivesupport.amd.com/s/question/0D54U00008JpnnLSAR/correct-way-to-have-moduledriver-autoload-on-boot-in-petalinux-20231-using-sysvinit?language=en_US


https://embeddedguruji.blogspot.com/2019/02/yocto-recipe-for-automatically-loading.html


