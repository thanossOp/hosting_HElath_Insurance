# Use a base image
FROM python:3.8-slim

ENV JSON_FOLDER=/app/JsonFiles \
    WAV_FOLDER=/app/wavFiles \
    USER_FOLDER=/app/User_Json \
    ENQUIRY_FOLDER_FOLDER=/app/Enquiry_Json \
    ENQUIRY_FOLDER=/app/Enquiry_Json \
    CURRENT_DIR=/app

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 5000

ENV FLASK_APP=app.py

CMD ["flask", "run", "--host=0.0.0.0"]

