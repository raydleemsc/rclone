# A very minimal sftp server for integration testing rclone
FROM alpine:3.18.3

# User rclone, password password
RUN \
    apk add openssh && \
    ssh-keygen -A && \
    adduser -D rclone && \
    echo "rclone:password" | chpasswd 

ENTRYPOINT [ "/usr/sbin/sshd", "-D" ]
