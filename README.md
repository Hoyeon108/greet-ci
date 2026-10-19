# greet-ci

인사말 프로그램과 GitHub Actions CI 실습 프로젝트입니다.

## 요구사항

- Python >= 3.11
- uv >= 0.8.14

## 설치 및 실행

프로젝트 의존성을 잠그고 가상 환경을 동기화합니다.

```bash
uv lock
```

인사말 프로그램을 실행합니다.

```bash
# 이름을 인수로 전달할 때
uv run --locked python greet.py Hee
# 출력: Hello, Hee!

# 인수가 없을 때
uv run --locked python greet.py
# 출력: Hello, world!
```

## 테스트 및 검사

```bash
# 단위 테스트
uv run --locked pytest -q greet.py

# 코드 포맷 검사
uv run --locked black --check greet.py

# 린트 검사
uv run --locked flake8 greet.py

# 정적 타입 검사
uv run --locked mypy greet.py

# 배포 패키지 빌드
uv build
```
