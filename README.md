
# yarn-check, npm-check

## options

> -u, --update Interactive update.
    -y, --update-all Uninteractive update. Apply all updates without prompting.
    -g, --global Look at global modules.
    -s, --skip-unused Skip check for unused packages.
    -p, --production Skip devDependencies.
    -d, --dev-only Look at devDependencies only (skip dependencies).
    -i, --ignore Ignore dependencies based on succeeding glob.
    -e, --save-exact Save exact version (x.y.z) instead of caret (^x.y.z) in package.json.

	ex)
    npm-check
    npm-check -u
    npm-check -gu

## yarn

-   설치된 모듈 리스트

	- global 모듈 리스트

		`yarn global list`
		

	- 현재 프로젝트 모듈
	
		`yarn list --depth=0`

## npm

-   설치된 모듈 리스트

	- global 모듈 리스트

		`npm list -g --depth=0`

    - 현재 프로젝트 모듈

        `npm list --depth=0`

# 명령어 비교

- install이 add로, uninstall이 remove로, update가 upgrade로 바뀐게 사실상 끝이다.
- 자세한 옵션은 CLI Docs를 참조하자.

	|npm															|Yarn|
	|----------------------------------------------|--|
	|npm install												|yarn install|
	|(N/A)															|yarn install –flat|
	|(N/A)															|yarn install –har|
	|(N/A)															|yarn install –no-lockfile|
	|(N/A)															|yarn install –pure-lockfile|
	|npm install [package]								|(N/A)|
	|npm install –save [package]					|yarn add [package]|
	|npm install –save-dev [package]				|yarn add [package] [–dev/-D]|
	|(N/A)															|yarn add [package] [–peer/-P]|
	|npm install –save-optional [package]		|yarn add [package] [–optional/-O]|
	|npm install –save-exact [package]			|yarn add [package] [–exact/-E]|
	|(N/A)															|yarn add [package] [–tilde/-T]|
	|npm install –global [package]					|yarn global add [package]|
	|npm update –global									|yarn global upgrade|
	|npm rebuild												|yarn install –force|
	|npm uninstall [package]							|(N/A)|
	|npm uninstall –save [package]				|yarn remove [package]|
	|npm uninstall –save-dev [package]		|yarn remove [package]|
	|npm uninstall –save-optional [package]	|yarn remove [package]|
	|npm cache clean										|yarn cache clean|
	|rm -rf node_modules && npm install		|yarn upgrade|

- Global 경로

	`Windows: %LOCALAPPDATA%/Yarn/config/global`

- config 리스트
	>$ yarn config list

- `yarn-check` 시 경로를 찾을 수 없다고 나올 때
    - yarn-check -g
    - 아래와 같은 메시지 나옴
        ```
        Path "C:\Users\chane\AppData\Local\npm" does not exist. Please check the NODE_PATH environment variable.
        For more detail, add `--debug` to the command
        ```

    - 실제 global 모듈 경로로 수정
        > set NODE_PATH=C:\Users\chane\AppData\Local\Yarn\Data\global\node_modules