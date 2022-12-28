1. `nvm use 18.12.1`
2. `npm i -g yarn`
3. cd folder project folder
4. create folder backend
5. `npm i -g @angular/cli@latest`
6. `ng new frontend --style=scss --strict`
7. add in .gitignore

    ```gitignore
     # frontend
     frontend/node_modules

     # backend
     backend/node_modules

     # angular
     .angular/
    ```

8. Зафиксировать версии пакетов в package.json, удалить символы каретки перед названием версии пакета.
9. Добавить в angular.json
    ```json
     "@schematics/angular:component": {
           "changeDetection": "OnPush",
           "style": "scss"
     }
    ```
10. [`npm i -D prettier`](https://prettier.io/docs/en/install.html)
11. add prettier config files
12. In webstorm open settings ctrl + alt + s
13. Набрать prettier и выбрать On Reformat code action
14. Обновить editorconfig file
15. Добавить команду по запуску prettier в package.json
16. Добавил использование ангуляра из node_modules `"start": "node --max-old-space-size=2048 ./node_modules/@angular/cli/bin/ng serve",`
17. `ng add @angular-eslint/schematics`
18. Зафиксировать версии пакетов в package.json, удалить символы каретки перед названием версии пакета.
19. Добавил своё правило для проверки, что все работает
20. [`npm i husky -D`](<(https://typicode.github.io/husky/#/)>)
21. [`npx husky install` в папке где лежит .git](<(https://typicode.github.io/husky/#/)>)
22. [`npm pkg set scripts.prepare="husky install"`](https://typicode.github.io/husky/#/)
23. Заменить команду "prepare": "cd .. && husky install frontend/.husky"
24. Переместить папку husky внутрь frontend
25. [npx husky add .husky/pre-commit](<(https://typicode.github.io/husky/#/)>)
26. Добавил в файл .husky/pre-commit
    ```text
    cd frontend/
    npm run prettier:fix
    npm run lint
    ```
27. `npm i -D @commitlint/cli`
28. `npm i -D @commitlint/config-conventional`
29. Добавить commitlint.config.js
30. `npx husky add .husky/commit-msg`
    ```text
    cd frontend/
    npx commitlint --edit $1
    ```
31. `npm i eslint-plugin-decorator-position -D`
32. `npm i eslint-plugin-jsdoc -D`
33. `npm i eslint-plugin-prefer-arrow -D`
34. `npm i eslint-plugin-simple-import-sort -D`
35. `npm i @ngrx/eslint-plugin -D`
36. `npm i eslint-config-airbnb-typescript -D`
37. `npm i eslint-config-prettier -D`
38. `npm i eslint-plugin-import -D`
39. `npm i eslint-plugin-prettier -D`
40. `npm i eslint-plugin-rxjs -D`
41. Зафиксировать версии пакетов в package.json, удалить символы каретки перед названием версии пакета.
42. Добавить .eslintignore
43. Обновить конфиг .eslintrc.json + запустить команду `ng lint --fix` + исправить ошибки
44. `npm i lint-staged -D`
45. `npm i stylelint stylelint-scss stylelint-config-standard stylelint-order stylelint-config-rational-order prettier stylelint-config-prettier stylelint-prettier -D`
46. Добавить файлы настройки stylelint .stylelintignore и .stylelintrc
47. Добавить настройку lint-staged в package.json
48. Изменить файл commit-msg на:
    ```text
        cd frontend/
        npx --no-install commitlint --edit "$1"
    ```
49. Изменить файл pre-commit на:
    ```text
        cd frontend/
        npx lint-staged --concurrent false
    ```
50. Зафиксировать версии пакетов в package.json, удалить символы каретки перед названием версии пакета.
51. Скопировать файлы docker-compose.yml и Dockerfile
52. Опционально: установить [docker](https://docs.docker.com/get-docker/)
53. Включить виртуализацию в bios
54. Запустить проект командой `docker-compose up --build`
