1. install yarn

2. install ESLint and Prettier on VSCode

3. create nextjs project called "gem-code-like-google"

> npx create-next-app@latest --ts

4.  (donot need nextjs --ts including it) Setting up TypeScript

5.  Setting up ESLint
    1. install >npm install eslint --save-dev
    2. to configure ESLint, run:
       > npx eslint --init
    3. result:
       A.created file ".eslintrc.js"
       B."eslint-config-google": "^0.14.0", added on package.json
6.  Setting up Prettier

    1.  install >npm install --save-dev --save-exact prettier
    2.  To avoid format conflicts between ESLint and Prettier

        > npm install --save-dev eslint-config-prettier

               "eslint-config-prettier": "^8.3.0", Added

    3.  add extends: ["plugin:react/recommended", "google", "prettier"], to eslintrc.js file
    4.  To customize Prettier, create a .prettierrc file in the root of your directory.
    5.  create .prettierignore and .eslintignore
        and set both same data
        .next
        next-env.d.ts
        node_modules
        yarn.lock
        package-lock.json
        public

7.  Formatting on save
    Create a .vscode/settings.json

8.  Using husky to run checks on git commit

    1. To install husky, run:
       > npx husky-init
    2. init
       > npm install
    3. update package.json
    4. Editing the pre-commit hook

9.  fixed prettier
    > npm run check-format

> npx prettier --write .vscode\settings.json

> npx prettier --check .vscode\settings.json

> npx prettier --write .prettierrc

> git -c user.useConfigOnly=true commit --quiet --allow-empty-message --file -
> .husky/pre-commit: line 2: .husky/\_/husky.sh: No such file or directory
