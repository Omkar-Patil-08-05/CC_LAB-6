FROM ubuntu:22.04

WORKDIR /app

RUN apt-get update -o Acquire::Check-Valid-Until=false && \
    apt-get install -y g++

COPY app.cpp .

RUN g++ app.cpp -o app

CMD ["./app"]
