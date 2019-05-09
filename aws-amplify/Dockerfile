FROM node:latest

RUN npm install -g @aws-amplify/cli

ENTRYPOINT ["amplify"]

LABEL io.whalebrew.config.environment '["AWS_ACCESS_KEY_ID", "AWS_SECRET_ACCESS_KEY", "AWS_SESSION_TOKEN", "AWS_DEFAULT_REGION", "AWS_DEFAULT_PROFILE", "AWS_PROFILE", "AWS_CONFIG_FILE"]'

LABEL io.whalebrew.config.volumes '["~/.aws:/.aws"]'
