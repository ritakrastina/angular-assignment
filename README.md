# Currency Exchange Rates

Angular based single page application for currency exchange rates (current and historical).

Data source from [Foreign exchange rates API](https://exchangeratesapi.io/).
UPDATE: To get data from this API, you must subscribe to it and replace `YOUR_API_KEY` with your access key in `ExchangeRatesService`.

## Built with

- HTML5, CSS
- [Angular CLI](https://github.com/angular/angular-cli) version 9.0.6
- [Bootstrap](https://getbootstrap.com/) version 4.3.1
- [ngx-bootstrap](https://valor-software.com/ngx-bootstrap) version 5.5.0

## Development

To run application, clone `master` branch locally, execute following commands and open browser on http://localhost:4200/.
```
npm install -g @angular/cli
npm install
ng serve
```

## Building

Run `ng build` to build the project. Result will be stored in the `dist/currency-exchange-rates` directory. Use the `--prod` flag for a production build.

## Development in docker

To run application in docker container, have installed [Docker](https://www.docker.com/).

Create application production build using command `ng build --prod`.

Then locate to docker terminal, change directory to application location using `cd` command and execute following commands to build an image and run it in a container.
```
docker build -f Dockerfile -t currency-exchange-rates-image .
docker run --name currency-exchange-rates-container -d -p 8080:80 currency-exchange-rates-image
```

To check if the image and container was created, use `docker image ls` and `docker container ls`.

Open browser on http://localhost:8080/ where the application should be running in docker container.
