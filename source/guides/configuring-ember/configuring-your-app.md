O Ember CLI é vem com suporte para gerenciar todo o ambiente de desenvolvimento da sua aplicação. O Ember CLI configurará um arquivo de configuração de ambiente padrão no `config/environment`. Neste arquivo, você pode definir um objeto `ENV` para cada ambiente, atualmente é limitado a três: development, testing e production.

O objeto ENV contém três chaves importantes:

  - `EmberENV` pode ser usado para definir o Ember feature flags (veja mais em [Feature Flags guide](../feature-flags/)).
  - `APP` pode ser usado para as flags/opções para sua instância de aplicação.
  - `environment` contém o nome do ambiente atual (`develpment`,`production` ou `testing`).

Você pode acessar esta variável de ambiente no código da sua aplicação importando do `your-application-name/config/environment`.

Por exemplo:

```js
import ENV from 'your-application-name/config/environment';

if (ENV.environment === 'development') {
  // ...
}
```
