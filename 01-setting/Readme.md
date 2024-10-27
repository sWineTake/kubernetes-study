## 설치 
경로 : https://github.com/sysnet4admin/_Lecture_k8s_starter.kit
1. `uname -m` 명령어를 통해 `arm64`를 확인합니다.
2. `brew install --cask ./vmware-fusion-v13.5.2/vmware-fusion.rb`
    - 파일은 같은 경로에 배치
    - 만약 설치 후에도 실행되지않았다면 강제실행 
    - `sudo /opt/vagrant-vmware-desktop/bin/vagrant-vmware-utility service start` : 서비스 실행
    - `launchctl start com.vagrant.vagrant-vmware-utility` : 서비스 강제 실행
    -  `ps aux | grep vagrant-vmware-utility` : 서비스 확인 
    - `sudo /opt/vagrant-vmware-desktop/bin/vagrant-vmware-utility service uninstall` : 서비스 제거 
    - `sudo /opt/vagrant-vmware-desktop/bin/vagrant-vmware-utility service install` : 서비스 재설치
----
```text
그럼에도 설치가 정상적으로 되지않아
`brew install --cask vmware-fusion` 명령어로 설치진행
vmware 13프로 버전은 개인적인 용도로 사용한다고 하면 무료로 사용가능
```
----
3. `brew install --cask ./vagrant-vmware-utility-1.0.22/vagrant-vmware-utility.rb` : 유틸리티 설치
4. [scripts](scripts) 경로에 실행
   - `sudo sh scripts/copy_launchctl-all-vmware-utility.sh` 파일 먼저 실행
   - `sudo sh scripts/copy_netstat-anvp.sh` 파일 실행
   - `netstat-anvp` 명령어를 통해 어떤 포트가 실행중인지 확인할 수 있음
   - `sudo sh scripts/vf_net_create_vnet2.sh` : 네트워크 생성
   ```text
    Started NAT service on vmnet7 Enabled hostonly virtual adapter on vmnet7
    7번 네트워크로 쿠버네티스를 구성하기에 잘살아있으면 됨
   ```
   - `ls /Library/Preferences/VMware\ Fusion` : 7번 확인
   - 
5. 
