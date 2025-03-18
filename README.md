# Django TDD 연습 프로젝트

이 프로젝트는 Django를 사용한 테스트 주도 개발(TDD) 연습을 위한 프로젝트입니다. 이 프로젝트에서는 기본적인 Django 설정과 함께 테스트 작성 방법을 연습할 수 있습니다. 주로 모델, 뷰, 시리얼라이저, 폼에 대한 테스트를 작성하는 데 집중합니다.

## 프로젝트 설정

1. **프로젝트 클론**
   
   먼저, GitHub에서 프로젝트를 클론합니다.

   ```bash
   git clone https://github.com/username/django-tdd-practice.git
   cd django-tdd-practice
   ```

2. **가상환경 설정**
   
   가상환경을 만들고 활성화합니다.

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # Linux/macOS
   venv\Scripts\activate  # Windows
   ```

3. **필수 패키지 설치**
   
   프로젝트의 종속성을 설치합니다.

   ```bash
   pip install -r requirements.txt
   ```

4. **데이터베이스 마이그레이션**

   데이터베이스 마이그레이션을 진행합니다.

   ```bash
   python manage.py migrate
   ```

## 테스트 실행

1. **테스트 작성**
   
   TDD에서는 코드를 작성하기 전에 테스트를 먼저 작성합니다. 예를 들어, `models.py`, `views.py`, `serializers.py`와 같은 파일에 대해 테스트를 작성합니다.

2. **테스트 실행**

   Django의 기본적인 테스트 프레임워크를 사용하여 테스트를 실행합니다. 아래 명령어를 사용하여 테스트를 실행할 수 있습니다.

   ```bash
   python manage.py test
   ```

   이 명령어는 `tests.py` 파일이나 각 앱 내의 `tests` 폴더에 있는 모든 테스트를 자동으로 실행합니다.

## TDD 작업 흐름

1. **테스트 작성**: 기능에 대한 테스트를 먼저 작성합니다.
2. **테스트 실패**: 작성한 테스트가 실패해야 합니다.
3. **기능 구현**: 테스트를 통과하는 최소한의 코드를 작성합니다.
4. **리팩토링**: 코드가 정상적으로 작동하면, 코드를 리팩토링하여 품질을 높입니다.
5. **테스트 통과**: 리팩토링 후 모든 테스트가 통과하는지 확인합니다.

## 주요 기능

- **모델 테스트**: `models.py`에 정의된 모델에 대한 테스트 작성
- **뷰 테스트**: REST API 엔드포인트에 대한 테스트 작성
- **시리얼라이저 테스트**: `serializers.py`에서 데이터를 변환하는 로직에 대한 테스트
- **폼 테스트**: 사용자 입력을 처리하는 폼에 대한 테스트

## 기술 스택

- Python 3.12
- Django
- Django REST Framework (DRF)
- PostgreSQL 13
