BEAT_NAME=winlogbeat
BEAT_TITLE=Winlogbeat
SYSTEM_TESTS=true
TEST_ENVIRONMENT=false
GOX_OS=windows
EXCLUDE_COMMON_UPDATE_TARGET=true

include ../libbeat/scripts/Makefile

.PHONY: update
update: mage
	mage update

.PHONY: gen
gen:
	GOOS=windows GOARCH=amd64 go generate -v -x ./...

gen-arm:
	GOOS=windows GOARCH=arm64 go generate -v -x ./...
