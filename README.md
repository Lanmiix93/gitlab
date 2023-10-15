# gitlab
https://github.com/Lanmiix93/gitlab/blob/main/Задание-1.1.png
https://github.com/Lanmiix93/gitlab/blob/main/Задание-1.2.png
https://github.com/Lanmiix93/gitlab/blob/main/Задание-2.1.png
https://github.com/Lanmiix93/gitlab/blob/main/Задание-2.2.png
# gitlab-ci.yml
stages:
  - test
  - build

test:
  stage: test
  image: golang:1.17
  script: 
   - go test .

build:
  stage: build
  image: docker:latest
  script:
   - docker build .
