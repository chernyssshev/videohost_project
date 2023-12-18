# Urfube @chernyssshev

  backend:
    build: ./services/backend
    ports:
      - 5000:80
    volumes:
      - ./services/backend:/app

  frontend:
    build: ./services/frontend
    volumes: 
      - './services/frontend:/app'
      - '/app/node_modules'
    ports: 
      - 8000:80

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).