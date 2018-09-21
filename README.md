## yarn-check, npm-check
  1. options
    # -u, --update          Interactive update.
    # -y, --update-all      Uninteractive update. Apply all updates without prompting.
    - -g, --global          Look at global modules.
    - -s, --skip-unused     Skip check for unused packages.
    - -p, --production      Skip devDependencies.
    - -d, --dev-only        Look at devDependencies only (skip dependencies).
    - -i, --ignore          Ignore dependencies based on succeeding glob.
    - -, --save-exact      Save exact version (x.y.z) instead of caret (^x.y.z) in package.json.
  2. ex)
    npm-check
    npm-check -u
    npm-check -gu
  
## yarn
  1. 설치된 모듈 리스트
    - global 모듈 리스트
      - yarn global list

  2. 현재 프로젝트 모듈
    - yarn list --depth=0
  
  
## npm
  1. 설치된 모듈 리스트
    - global 모듈 리스트
    - npm list -g --depth=0

  2. 현재 프로젝트 모듈
    - npm list --depth=0
  
  
   
