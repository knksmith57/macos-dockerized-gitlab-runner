# macOS dockerized `gitlab-runner`

## quickstart

```bash
$ git clone https://github.com/knksmith57/macos-dockerized-gitlab-runner.git macos-dockerized-gitlab-runner \
    && cd $_

$ docker-compose run gitlab-runner register \
  --non-interactive \
  --executor 'docker' \
  --docker-image alpine:latest \
  --url '<gitlab URL here>' \
  --registration-token '<registration token here>' \
  --description '<description of runner>' \
  --tag-list 'docker' \
  --run-untagged \
  --locked='false'

$ docker-compose up -d
```

## references

- https://docs.gitlab.com/runner/register/index.html#one-line-registration-command
- https://docs.gitlab.com/runner/install/docker.html
- https://docs.gitlab.com/runner/configuration/advanced-configuration.html
- https://gitlab.com/gitlab-org/gitlab-runner/blob/master/config.toml.example
