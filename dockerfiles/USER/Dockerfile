FROM almalinux
RUN dnf install nginx -y
#root acces required to create user or install packages
RUN useradd roboshop

USER roboshop
CMD ["sleep","100"]