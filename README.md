## **DjangoApp 배포 : be-lb-staging-19474257-8dedf138b448.kr.lb.naverncp.com**

### 라이브러리 버전
Django 4.2.3  
postgresql 13  
gunicorn 21.2.0  
psycopg2-binary 2.9.7  
djangorestframework 3.14.0  
drf-spectacular 0.26.4  
python-dotenv 0.19.1  

### **1. 백엔드 DB 설계**  
  
- Django 모델을 사용하여 게시글과 유저를 생성합니다.  
- Django의 ORM을 사용하여 모델 간의 관계를 정의하고 데이터베이스를 마이그레이션합니다.  
  
### **2. 백엔드 API 개발**  
  
- Django REST framework를 사용하여 필요한 API 엔드포인트를 개발합니다.  
- 사용자, 게시글과 관련된 API를 구현합니다.  
- API에 대한 권한과 인증을 설정하여 사용자만이 해당 기능을 사용할 수 있도록 합니다.  
  
### **3. 더미데이터 추가**  

- 5명 이상의 사용자와 각 사용자당 3개 이상의 게시글을 생성합니다.  
  
### **4. 테스트 코드 작성**    

### **5. 배포**  
  
- Django 프로젝트를 NCP 클라우드 서비스에 배포합니다. 
- 웹 서버 Gunicorn, 리버스 프록시 Nginx를 설정하여 프로덕션 환경에 배포합니다.  
- 서버에서 환경 변수를 설정하여 중요한 정보를 안전하게 관리합니다.  
  
### **6. CICD Pipeline 작성**  

#### **CICD 확인 : https://github.com/bainaryho/DjangoSNS/commits/master**
  
- GitHub Actions CI/CD 도구를 사용하여 CI/CD 파이프라인을 설정합니다.  
- 코드가 GitHub 리포지토리에 푸시될 때 테스트를 자동으로 실행하도록 설정합니다.  
- 테스트가 성공하면 자동으로 서버에 새로운 버전을 배포하도록 설정합니다.   
