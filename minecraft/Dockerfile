# docker
# docker run -d -p 25565:25565 minecraft
FROM ubuntu:21.10

RUN apt-get update

RUN apt-get install -y systemctl
RUN apt-get install -y openjdk-8-jdk
RUN apt install -y git
RUN git clone https://github.com/Prefect1109/minecraft-2021-server.git
RUN echo DEAMON_CONFIG >> /etc/systemd/system/minecraft.service

EXPOSE 25565
WORKDIR /minecraft-2021-server/minecraft
CMD ["java", "-Xmx8G", "-Xms6G", "-jar", "forge-1.12.2-14.23.5.2855.jar"]
# CMD systemctl start minecraft
