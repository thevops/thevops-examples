.ONESHELL:
SHELL:=/bin/bash


.PHONY: start
start: ## Start docker-compose
	docker-compose up -d

.PHONY: stop
stop: ## Stop docker-compose
	docker-compose down

.PHONY: logs
logs: ## Get docker-compose logs
	docker-compose logs --tail 10 -f

help:
	@grep -E '^[a-zA-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | awk 'BEGIN {FS = ":.*?## "}; {printf "\t\033[36m%-30s\033[0m %s\n", $$1, $$2}'


.DEFAULT_GOAL := help
