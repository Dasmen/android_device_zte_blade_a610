# ���������� �� ������� ���������� 

## ��������� JAVA

#### ������������� "java" ��������:
```
sudo apt-add-repository ppa:openjdk-r/ppa
sudo apt-get update
sudo apt-get install openjdk-8-jdk
```
#### ��������� ������ ��� "java" ��������:
```
sudo apt-get update && sudo apt-get install git-core gnupg flex bison gperf libsdl1.2-dev libesd0-dev libwxgtk2.8-dev squashfs-tools build-essential zip curl libncurses5-dev zlib1g-dev openjdk-8-jre openjdk-8-jdk pngcrush schedtool libxml2 libxml2-utils xsltproc lzop libc6-dev schedtool g++-multilib lib32z1-dev lib32ncurses5-dev lib32readline-gplv2-dev gcc-multilib maven tmux screen w3m ncftp
```
## ��������� �����������

#### ������� ����� "bin" ��������:
```
mkdir ~/bin
```
#### ������ ����� "bin" ��������:
```
PATH=~/bin:$PATH
```
#### ��������� "repo" ��������:
```
curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
```
#### ������ ���������� ��� "repo" ��������:
```
chmod a+x ~/bin/repo
```
## �������� ���������� � ���������

#### ������� ����� "BLADE" � � ��� ��������� ��������� ������:
```
mkdir ~/BLADE
cd ~/BLADE
```
#### ��������� � "git" (���� ������ ����, ��� ���� "https://github.com/" ):
```
git config --global user.email "aaa@bbbbbb.com" (����� �� ������� ���� ���������������� ������ �������) 
git config --global user.name "NAME" (����� �� �������)
```
#### ��������� ��������� ��� ������ �������:
```
repo init -u (������ �������e� ������ �� ��������, ������ ������ �������)
```
#### ��������, ��� ������ Resurrection Remix 5.8.x ������� �������� ��������� �������:
```
repo init -u https://github.com/ResurrectionRemix/platform_manifest.git -b nougat
```
#### C�������� ��������� ��� ������ �������:
```
repo sync -f --force-sync --no-clone-bundle
``` 
## ��������� "������" � "�������" ����������

### ������

#### ������� � ����� "BLADE" ��������:
```
cd ~/BLADE
```
#### ������� � ����� "device" ��������:
```
cd device
```
#### ������� ����� "zte" ��������:
```
mkdir zte
```
#### ������� � ����� "zte ��������":
```
cd zte
```
#### ��������� "������" ��������:
```
git clone https://github.com/mosya234/android_device_zte_blade_a610.git a610
```
### ������

#### ������� � ����� "BLADE" ��������:
```
cd ~/BLADE
```
#### ������� � ����� "vendor" ��������:
```
cd vendor
```
#### ������� ����� "zte" ��������:
```
mkdir zte
```
#### ��������� "������" ��������:
```
git clone https://github.com/mosya234/android_vendor_zte_blade_a610.git a610
```
## ������ ���������

#### ������ ��������:
```
cd ~/BLADE/device/zte/a610/patches_mtk && . apply-patches.sh
```
## ���

### ������������� "���" ��� ������ (� ����� � ������ ������ ��� ��� ��������)

#### ������� ����� ��������� ������ ���� �������� ����� (HOME), �������� "Ctrl+H", ��������� ���� ".bashrc" � � ����� ��� ���������:
```
export USE_CCACHE=1
export ANDROID_JACK_VM_ARGS="-Xmx4096m -Xms512m -Dfile.encoding=UTF-8 -XX:+TieredCompilation"
```
#### (��� "Xmx4096m" - ��� ���������� ����������� ������)

## ����-������

#### ����� ������� � ����� ����� "BLADE":
```
./prebuilts/sdk/tools/jack-admin kill-server
```
##### (��� ������� ������� ������� �������� ������� "���K", ���� �� ����� ������ ��������) ���������� ����� (�������� ��� �������� �� ����):
```
/android/system$ ./prebuilts/sdk/tools/jack-admin kill-server
Writing local settings in /home/hard/.jack
Killing background server
ERROR: No Jack server to kill
```
#### ��������� ������ �������� �� ����� "BLADE":
```
./prebuilts/sdk/tools/jack-admin start-server
```
## ������

#### ������� � ����� "BLADE" ��������:
```
cd ~/BLADE
```
#### ������ �������:
```
. build/envsetup.sh && brunch a610
```

## ���������� ������!!!

#### ������ ����� �� ���� �� �������������

## ������� � ������!!!

