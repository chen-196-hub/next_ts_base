# next_ts_base

## 参考：
https://zenn.dev/tasuya/articles/da033574b85e6d


# docker yaml
```
version: '3'
services:
  app:
    build:
      context: .
      dockerfile: Dockerfile
    volumes:
      - ./:/usr/src/app 
    command: sh -c "cd <アプリ名> && yarn dev"
    ports:
      - "8090:8090" #port 指定
```

### port 指定方法
https://github.com/vercel/next.js/issues/102



# yarn
```bash
docker-compose run --rm app yarn add create-next-app
```

```bash
docker-compose run --rm app yarn create-next-app <アプリ名> --ts
```