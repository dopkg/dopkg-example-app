# dopkg-example-app

> Example [zeit/micro](https://github.com/zeit/micro) app running in small docker container using [dopkg](https://github.com/dopkg/dopkg)


### Step 1: Clone the repository, install dependencies

```bash
$ git clone https://github.com/dopkg/dopkg-example-app.git
$ cd dopkg-example-app
$ npm install
```

### Step 2: Run the build command

```bash
$ npm run build
```

This will do 2 things:

- Build the `app.bin` file using the [dopkg/builder](https://hub.docker.com/r/dopkg/builder/) container
- Build a new Docker container based of the [dopkg/runner](https://hub.docker.com/r/dopkg/runner/) container

### Step 3: There is no Step 3!

You have just created a <50 MB Docker image that runs your application.

Run the container using this command:

```bash
$ docker run -p 3000:3000 -it --name dopkg-example-app --rm dopkg/dopkg-example-app:latest
```

or

```bash
$ npm start
```    

Verify that it works:
```bash
$ curl localhost:3000
```

You can stop the running container using this command:

```bash
$ docker stop dopkg-example-app
```

or

```bash
$ npm stop
```

# Credits

- [zeit/pkg](https://github.com/zeit/pkg)
- [zeit/micro](https://github.com/zeit/micro)

# License

MIT
