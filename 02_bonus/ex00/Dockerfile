FROM ubuntu

RUN apt update
RUN apt install -y make git vim gcc libncurses5-dev
RUN git clone https://github.com/kuhar-tarass/Corewar.git /home/Corewar
WORKDIR /home/Corewar
RUN make

ENTRYPOINT ./corewar && ./asm
# docker build  -t corewar .
# docker container run -it --name Corewar corewar
# docker container start -i Corewar