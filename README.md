# Setup


## Build and run api-playground

git clone https://github.com/bestbuy/api-playground/
cd api-playground
npm install
npm start
- Best Buy API Playground started at http://localhost:3030


## Build and run bestbuy_n26_test

Tests are developed using [Gauge](http://getgauge.io/index.html).

- Clone the project
```
git clone git@github.com:maristn/bestbuy_n26_test.git && cd bestbuy_n26_test
```

- Change the environment from [main.properties](https://github.com/maristn/bestbuy_n26_test/blob/master/env/default/main.properties) to your IP address
Example: 
```
LOCAL = http://192.168.15.11:3030
```

- Build the project
```
docker-compose build
```

- Execute all the tests
```
docker-compose run --rm gauge run --verbose specs
```

## Examples

#### Execute a set of specs
```
docker-compose run --rm gauge run --verbose specs/product.md
```

#### Execute tests by flag
```
docker-compose run --rm gauge run --verbose --tags regression specs
```

#### Rerun failed tests
Just add `--failed` before the specs, ex.:
```
docker-compose run --rm gauge run --failed
```
