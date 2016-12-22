docker-image-h2o
----

```bash
$ docker build --no-cache --tag fukata/docker-image-h2o:v2.1.0-beta4 .
$ docker run -p 18080:80 -v $(pwd)/examples/h2o:/etc/h2o -v $(pwd)/examples/www:/var/www fukata/docker-image-h2o:v2.1.0-beta4
start_server (pid:1) starting now...
starting new worker 7
[INFO] raised RLIMIT_NOFILE to 1048576
h2o server (pid:7) is ready to serve requests
$ curl http://localhost:18080/index.html
<!DOCTYPE HTML>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Hello h2o on docker</title>
</head>
<body>
  <h1>Hello h2o on docker</h1>
</body>
</html>

```
