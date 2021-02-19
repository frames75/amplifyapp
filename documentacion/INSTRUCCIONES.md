# Introducción

Esta aplicación es el resultado de seguir el tutorial de AWS [Cree una aplicación Web React simple con AWS Amplify](https://aws.amazon.com/es/getting-started/hands-on/build-react-app-amplify-graphql/).

## Error al actualizar el repo GitHub y reconstruir el backend:

"Cannot find file './aws-exports' in './src'"

https://github.com/aws-amplify/docs/issues/503

https://stackoverflow.com/questions/61514515/missing-aws-exports-js-always-when-building-aws-amplify-react-app-with-amplify-i

```sh
As a workaround, I committed aws-exports.js for each environment and renamed it in amplify.yml.

frontend:
  phases:
    build:
      commands:
        - mv src/aws-exports.dev.js src/aws-exports.js
        - npx browserslist --update-db
        - yarn run build
```
