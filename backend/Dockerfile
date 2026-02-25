FROM ubuntu:22.04

WORKDIR /app

RUN apt update && apt install -y g++

COPY app.cpp .

RUN g++ app.cpp -o app

CMD ["./app"]
