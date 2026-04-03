FROM python:3.11-slim
RUN apt-get update && apt-get install -y ffmpeg nodejs
WORKDIR /app
COPY . .
RUN pip install --no-cache-dir -r requirements.txt
RUN pip install -U --pre yt-dlp
EXPOSE 499
CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "499"]
