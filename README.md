# docker-truffle-develop
smart contract develop enviroment

## Setup
copy `.env.example` to `.env`
and dont forget setting your `TRUFFLE_PROJECT_FOLDER` location

## install
```
$ docker-compose build
$ docker-compose up -d ganach-cli
```

## set network info
in your project, edit your truffle.js
```
module.exports = {
  networks: {
    development: {
      host: "ganache-cli",
      port: 6666,
      network_id: "6666"
    }
  }
};
```

## test smart contract
```
$ docker-compose run truffle ash
```

you will get into truffle container, and go to your project
```
## in container
$ cd /root/truffle/YOUR_PROJECT

## run test
$ trufffle test
```