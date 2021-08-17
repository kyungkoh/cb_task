# GCP 

### VM 생성 

#### 1. 계정생성 
GCP에서 구글 계정을 통해 Free tier 계정 생성이가능하다 
#### 2. 프로젝트 생성 

1) 프로젝트를 만든다. 
![](https://images.velog.io/images/kyungkoh/post/9439b66a-4adf-4f1d-86ee-55bab50ca252/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-08-17%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%208.37.23.png)
보통 기업에서는 조직을 구성해서 role이나 Biiling 관련 된 작업을 진행하지만, 해당 과제에서는 큰 영향을 미치지 않을 듯 하여 구성하지 않았다. 

2) 프로젝트 접속 후 인스턴스 생성 클릭 
#### 3. Instance 생성 (VM 생성)
![](https://images.velog.io/images/kyungkoh/post/44cf27a2-f747-4ab9-b01d-01687aa54694/FireShot%20Capture%20003%20-%20Google%20Cloud%20Platform%20-%20console.cloud.google.com.png)
![](https://images.velog.io/images/kyungkoh/post/defb5387-815f-42a5-a550-0457939ef5a9/FireShot%20Capture%20004%20-%20Google%20Cloud%20Platform%20-%20console.cloud.google.com.png)
>1) Instance 이름 기입 
2) 리전 : asia-northeast3
3) 머신 : e2-standard-2
4) OS :  Centos7
5) 부팅 디스크:  20GB

#### 4. VM 생성 완료가 되면 프로젝트 안에 vm이 보인다. 


### VM 접속

1. ssh 키를 만든다.

 ```ssh-keygen -t rsa -f ~/.ssh/[키 파일 이름] -C [UserName]```

2. 콘솔에서 Compute Engine > 메타데이터 > SSH키 에서 생성 된 ssh 키를 추가한다. 
3. 하기 명령어를 통해 vm에 접속한다 
```ssh -i ~/.ssh/[ssh key fileName] [UserName@IP주소]```


GCP는 독특하게 콘솔에서 직접 접속도 가능하다
![](https://images.velog.io/images/kyungkoh/post/7e506809-5fb8-4278-b1b0-328b48bff109/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-08-16%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%204.22.11.png)