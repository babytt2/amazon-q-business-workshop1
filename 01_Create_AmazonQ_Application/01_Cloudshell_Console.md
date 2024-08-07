# 실습 1. Cloudshell을 통해 Amazon Q Application 생성을 위한 CloudFormation 배포하기

1. Cloudshell에 접속하여 CloudFormation 정보가 있는 Git을 Clone 합니다.
~~~
git clone https://github.com/aws-samples/support-insights-with-amazon-q.git
~~~
<img src="images/11_GitClone_CF.png">


2. src 디렉토리에서 Cloudㄹormation 배포를 위해 deploy_cfn.sh 파일에 실행 권한을 부여하고 실행합니다.
~~~
cd support-insights-with-amazon-q/src
chmod +x deploy_cfn.sh
./deploy_cfn.sh
~~~

3. Amazon Q Business Application 으로 생성될 이름과 **00_Prerequsites.md** 를 통해서 생성한 S3 명을 입력합니다.
- Enter name for the Amazon Q Business Application (Hyphens (-) can be included, but not spaces):  **myApplication**
- Enter name of the S3 Data Source Bucket:  **businesssources3**

~~~
myApplication
businesssources3
~~~

<img src="images/13_CreateApplication.png">

4. CloudFormation에서 **amazon-q-cfn** 의 Stackset이 생성된 것을 확인합니다. Stackset에서 Resource가 모두 생성되어 CREATE_COMPLETE가 되면 다음 작업으로 넘어갑니다.
<img src="images/12_CreateStackSet.png">

6. Amazon Q Business Console로 이동하여 Application이 생성되었습니다.
   3번에서 사용한 myApplication 이름으로 Amazon Q Business Application이 생성되었습니다.
<img src="images/14_ApplicationCreationo_Complete.png">

5. Application의 Data Sources에 qci-insight-datasource로 Data Source가 생성되었습니다. 
<img src="images/15_S3_Source.png">
