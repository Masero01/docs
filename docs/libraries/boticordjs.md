# JavaScript
BotiCord.js - это библиотека для взаимодействия с сервисом BotiCord.top на языке JavaScript (TypeScript).

____

### Полезные ссылки:

- [Github-Репозиторий](https://github.com/boticord/boticord.js) 
- [NPM](https://www.npmjs.com/package/boticord.js) 
- [Документация](https://js.boticord.top/)


!!! note "Важная информация!"

    - boticord.js поддерживает `discord.js`, `Eris`, `Discordoo`, а также прямые обращения.
    - Если в вашем проекте есть TypeScript, пожалуйста, включите свойство `skipLibCheck` в `tsconfig.json`


## Установка
```
npm i boticord.js
```

## Примеры работы:

**Автоматическая публикация статистики (discord.js)**

```ts
import { Client as BotiCord, DjsAdapter } from 'boticord.js'
const client: any = {} // Discord.js client

const adapter = new DjsAdapter(client) // pass djs client to adapter

const boticord = new BotiCord({
  token: 'Bot YOUR_BOTICORD_API_TOKEN',
  apiVersion: 2
}, adapter)

boticord.botStatsAutopost()
  .then(success => {
    if (success) console.log('autopost started successfully!')
    else console.log('autopost already running')
  })
  .catch(error => {
    console.log('whoops, some error occurred!', error)
  })
```

**Простая публикация статистики**

```ts
import { Client as BotiCord } from 'boticord.js'

const boticord = new BotiCord({
  token: 'Bot YOUR_BOTICORD_API_TOKEN',
  apiVersion: 2
})

boticord.bots.postStats({ servers: 123, users: 12345, shards: 1 })
  .then(success => {
    console.log('posted bot stats! success?', success)
  })
```

Остальные примеры использования располагаются [здесь](https://github.com/boticord/boticord.js/tree/master/examples).

## Нужна помощь?

Если Вам нужна какая-либо помощь, то мы рекомендуем еще раз прочитать [документацию библиотеки](https://js.boticord.top/).

Вы можете найти нас на [сервере поддержки сервиса](https://boticord.top/discord). 
Разработчик библиотеки: [`@san4ouZ#8649`](https://boticord.top/profile/607148903833403422)
