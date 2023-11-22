FROM ubuntu:latest
RUN apt  update && apt install openssh-server python3-apt vim sudo -y
RUN useradd -rm -d /home/john -s /bin/bash -g root -G sudo -u 1000 john
RUN echo "john:doe" | chpasswd
COPY sshd_config /etc/ssh/sshd_config
RUN mkdir /home/john/.ssh
COPY id_rsa.pub /home/john/.ssh/authorized_keys
RUN chmod 700 /home/john/.ssh
RUN chown john:root /home/john/.ssh
RUN chmod 600 /home/john/.ssh/authorized_keys
RUN chown john:root /home/john/.ssh/authorized_keys
RUN service ssh start
EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
