FROM amazonlinux:latest
RUN amazon-linux-extras install -y python3
RUN yum install -y groff less mailcap
RUN pip3 install awscli
ADD https://s3.amazonaws.com/session-manager-downloads/plugin/latest/linux_64bit/session-manager-plugin.rpm session-manager-plugin.rpm
RUN yum install -y session-manager-plugin.rpm
RUN rm session-manager-plugin.rpm
RUN yum clean all

LABEL io.whalebrew.name aws
LABEL io.whalebrew.config.environment '["AWS_ACCESS_KEY_ID", "AWS_SECRET_ACCESS_KEY", "AWS_SESSION_TOKEN", "AWS_DEFAULT_REGION", "AWS_DEFAULT_PROFILE", "AWS_PROFILE", "AWS_CONFIG_FILE"]'
LABEL io.whalebrew.config.volumes '["~/.aws:/.aws"]'
ENTRYPOINT ["aws"]
