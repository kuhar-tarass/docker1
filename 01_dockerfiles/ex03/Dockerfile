FROM ubuntu
RUN  apt-get update -y && apt-get install -y curl openssh-server ca-certificates && apt-get install -y postfix

RUN curl https://packages.gitlab.com/install/repositories/gitlab/gitlab-ee/script.deb.sh | bash

RUN EXTERNAL_URL="http://gitlab.example.com" apt-get install gitlab-ee

EXPOSE 443 80 22

ENTRYPOINT (/opt/gitlab/embedded/bin/runsvdir-start &) && gitlab-ctl reconfigure && tail -f /dev/null
