# Java
BotiCordJava - это библиотека для взаимодействия с сервисом BotiCord.top на языке Java.

____

### Полезные ссылки:

- [Github-Репозиторий](https://github.com/boticord/boticordjava) 
- [Jitpack.io](https://jitpack.io/#megoRU/boticordjava)


## Установка

### Maven

Просто добавьте это в свой `pom.xml`.

```xml
<repositories>
 <repository>
    <id>jitpack.io</id>
    <url>https://jitpack.io</url>
 </repository>
</repositories>

<dependency>
    <groupId>com.github.megoRU</groupId>
    <artifactId>boticordjava</artifactId>
    <version>v3.3</version>
</dependency>
```

Другие методы установки можно найти [тут](https://jitpack.io/#megoRU/boticordjava).

## Примеры работы:
**Простая публикация статистики**

```java
public static void main(String[] args) {

    BotiCordAPI api = new BotiCordAPI.Builder()
        .token("YOUR_TOKEN")
        .build();
        
    int servers = ...; // the server count
    int shards = ...; // shards count
    int users = ...; // the amount of users

    api.setStats(servers, shards, users);
}    
```

## How to use API v2
```java
public static void main(String[] args) {

    BotiCordAPI api = new BotiCordAPI.Builder()
        .token("YOUR_TOKEN")
        .tokenEnum(TokenEnum.PROFILE) //This enable API v2
        .build();
    
    api.createShortLink("boticordjava", "https://docs.boticord.top/libraries/boticordjava");
}    
```

Остальные примеры использования располагаются [здесь](https://github.com/boticord/boticordjava).

## Нужна помощь?

Если Вам нужна какая-либо помощь, то мы рекомендуем подробнее поискать ответы
на ваши вопросы в [репозитории проекта](https://github.com/boticord/boticordjava).

Разработчик библиотеки: [`@mego#5338`](https://boticord.top/profile/250699265389625347)

