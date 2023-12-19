

## 리눅스 환경에서 OCR 서버를 구동하기 위해 필요한 환경 셋팅

ansible 사용하여 환경 구성하기  
  
  
### 1) 모니터링 컴퓨터에서 `ansible` 설치 
```bash
cd ansible_install_local
sh install_ansible.sh
# ansible 구동확인
ansible
```
### 2) 환경 셋팅
2-1) 환경을 셋팅한 서버 ip 기입
```bash 
# inventory.yaml
myhost :
    hosts :
        ocr_server :
            ansible_host : [hostname]@[ip address]
            ansible_ssh_pass : [password]
            http_port : [port number]


```

2-2) root로 접속하기 위한 password 기입
```bash
# secret.yml
ansible_become_pass : [password]

```


### 2) ansible playbook 실행
