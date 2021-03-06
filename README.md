# HyperledgerFabric_medsys
간단 의료기록 저장 하이퍼레저 패브릭 애플리케이션입니다.
<br>
총 네가지 항목 [이름, 연락처, 증상, 날짜]를 저장할 수 있습니다.


우선 네트워크를 시작하기 위해서 medsys 디렉터리에 가서<br>
./startFabric.sh
<br>
명령어를 실행해 줍니다. 

그러면 fabric-samples의 basic network를 기반으로 네트워크가 시작이 되고,<br>
docker-compose.yml 파일에 명시된 환결설정값 (CA, 피어, 오더러, CouchDB, Cli 등) 컨테이너가 시작이 되며 <br>
채널생성 및 Join이 됩니다. 

![1](https://user-images.githubusercontent.com/22516796/75415915-6392dd80-5970-11ea-8762-97c19ff461c3.PNG)

그리고 나서 체인코드가 설치 및 인스턴스화 된 후 애플리케이션을 사용할 수 있는 상태가 됩니다. 
![2](https://user-images.githubusercontent.com/22516796/75416027-a05ed480-5970-11ea-88a4-cea0f5f79294.PNG)


정상적으로 스크립트가 실행이 되면 애플리케이션 설명과 간단한 튜토리얼이 출력됩니다.<br><br>
![3](https://user-images.githubusercontent.com/22516796/75416241-29760b80-5971-11ea-98b2-30cc0182885b.PNG)
<br>
이제 Javascript, Typescript, Java 세가지 언어로 애플리케이션을 실행할 수 있는데,<br>
예를 들어 Javascript로 애플리케이션을 돌려보려면 일단 javascript 디렉토리로 들어갑니다.<br>
<br>
enrollAdmin.js, registerUser.js, invoke.js, query.js 네가지 JS 파일들이 있는데<br>
![4](https://user-images.githubusercontent.com/22516796/75416290-4dd1e800-5971-11ea-951d-b22413069cc1.PNG)
enrollAdmin은 장부에 admin 등록, registerUser는 노드 추가, <br>
invoke.js 는 정보 입력 및 수정, query.js는 정보를 받아와 출력하는 것으로 보시면 됩니다.<br>
<br>
node enrollAdmin.js로 admin을 먼저 등록해주고, <br>
차례로 registerUser.js, invoke.js, query.js를 node 명령어로 실행시켜줍니다.<br>
여기서 registerUser.js와 invoke.js를 수정해서 새 노드를 추가하거나 새로운 정보를 추가하실 수 있습니다. <br>

query.js에서도 체인코드에 있는 다른 함수를 불러와서 한꺼번에 모든 데이터 전체 출력, 또는 한 노드의 데이터만 출력이 가능합니다.

![5](https://user-images.githubusercontent.com/22516796/75416443-a6a18080-5971-11ea-8704-7399948ee855.PNG)

<br>
정상적으로 모든 쿼리문이 실행되면 예를 들어 위와 같은 결과가 나옵니다.
