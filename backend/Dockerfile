FROM python:3.11

WORKDIR /app

COPY Pipfile Pipfile.lock ./
RUN pip install pipenv && pipenv install --deploy --system
RUN pipenv install fastapi passlib bcrypt pydantic[email] python-multipart uvicorn pymysql cryptography Pillow

COPY . .

EXPOSE 4000

CMD ["pipenv", "run", "python3", "main.py"]