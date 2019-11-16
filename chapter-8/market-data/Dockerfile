# 파이썬 앱을 위한 공개 베이스 이미지를 시작한다.
FROM python:3.6
ADD . /app
WORKDIR /app
# 요구 사항을 설치한다.
RUN pip install -r requirements.txt
# 서비스의 시작 명령을 설정한다.
CMD ["gunicorn", "-c", "config.py", "app:app", "--bind", "0.0.0.0:8080"]
# 서비스의 포트를 컨테이너에 노출한다
EXPOSE 8000