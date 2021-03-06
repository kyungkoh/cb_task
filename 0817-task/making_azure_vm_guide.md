# Azure 
## VM 생성

#### 1. 계정 생성   (git 계정과 연동 가능)
#### 2. 콘솔 접속 후 VM 생성 
![](https://images.velog.io/images/kyungkoh/post/544cc945-15a4-449c-bdd3-f38b3643e498/FireShot%20Capture%20007%20-%20%E1%84%80%E1%85%A1%E1%84%89%E1%85%A1%E1%86%BC%20%E1%84%86%E1%85%A5%E1%84%89%E1%85%B5%E1%86%AB%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%80%E1%85%B5%20-%20Microsoft%20Azure%20-%20portal.azure.com.png)


>크게 변경한 사항은 없고 인스턴스명 기입 후 
OS : CentOS 
Region : 한국 리전으로 변경 
부팅 디스크 : 20GB
Test용 VM이어서 별도의 네트워크 설정은 하지 않고 진행 했다. 


-  key 생성이 GCP와 약간 달랐는데, 콘솔 자체에서 key를 만들고 해당 파일을 로컬로 저장할 수 있었다. 
다운 받은 파일의 경로를 알고 있어야, vm 접속 시에 key파일의 경로 기입 후 접속 할 수 있다. 

- #### Azure의 독특했 던 점 
생성 된 모든 리소스들을 보여준다.
GCP의 경우 vm이 삭제 되어도 umig나 스냅샷, 네트워크 자원들을 추가로 삭제했어야 했는데, 
가시적으로 남아있는 자원들이 보여서 리소스 확인이 원활했다. 
![](https://images.velog.io/images/kyungkoh/post/d7a333e8-9f26-433a-aa1c-cac8a06743cc/FireShot%20Capture%20010%20-%20CreateVm-OpenLogic.CentOS-7_9-gen2-20210816230804%20-%20Microsoft%20Azure_%20-%20portal.azure.com.png)


#### 3. 생성한 VM 정보는 하기와 같다 

![](https://images.velog.io/images/kyungkoh/post/c3a423f7-08fe-437c-b49f-f8959a07db35/FireShot%20Capture%20011%20-%20cb-vm-azure-2108-01%20-%20Microsoft%20Azure%20-%20portal.azure.com.png)

## VM 접속
#### 1. VM 접속하는 방법

![](https://images.velog.io/images/kyungkoh/post/1c83c41a-50f9-416b-adbb-24fefa187b53/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2021-08-16_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_11.22.01.png)

key 파일을 사용해서 접속 시 permission 오류가 났다.
권한관련 오류 였는데, ```chmod 400 ./Downloads/[키파일이름]``` 을 통해서 해결했다.

#### 2. 접속 화면 

![](https://images.velog.io/images/kyungkoh/post/fadb27ab-e60f-4879-90ed-921680312812/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2021-08-16_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_11.24.29.png)
