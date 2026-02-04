# Telegram-Helper-Bot

docker build --no-cache -t testgroup-helper-bot:latest .

// remove the conainer and mount and run 
docker stop testgroup-helper-bot
docker rm testgroup-helper-bot

docker run -d ^
  --name testgroup-helper-bot ^
  --env-file .env ^
  -v %cd%\responses:/app/responses ^
  --restart unless-stopped ^
  testgroup-helper-bot:latest

