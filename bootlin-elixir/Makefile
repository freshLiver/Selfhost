ERR_URL		= GIVE_ME_URL
ERR_TAG		= GIVE_ME_TAG
ERR_NAME	= GIVE_ME_NAME

URL	:= ${ERR_URL}
TAG	:= ${ERR_TAG}
NAME	:= ${ERR_NAME}

all: check
	docker build -t elixir:${NAME} --build-arg GIT_REPO_URL=${URL} --build-arg GIT_TAG=${TAG} --build-arg PROJECT=${NAME} .

check:
ifeq (${URL},${ERR_URL})
	$(error ADD ARG: "URL=$$TARGET_REPO_URL")
endif

ifeq (${TAG},${ERR_TAG})
	$(error ADD ARG: "TAG=$$TARGET_REPO_TAG_OR_BRANCH")
endif

ifeq (${NAME},${ERR_NAME})
	$(error ADD ARG: "NAME=$$TARGET_PROJ_NAME")
endif
