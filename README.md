## WP Docker StartKit

Try for your next Project.

## How to Proceed

* Install docker from [https://www.docker.com/](https://www.docker.com/)
* Clone this repo
* Run `npm run start:docker` or `docker-compose up -d`

## Themes & plugins development

This is a really simple environment for themes & plugins development. Nothing fancy. Please be aware that:

* Your WordPress installation will be available at `http://0.0.0.0:9190`
* `wp_data` folder you'll find in this repo will be shared with the WordPress installation, put your code there.
* `wp_logs` include all the logs from your Apache
* `db_data` contains your MySQL Data

## Helpful Commands
You can place the commands in the scripts area of your `package.json` in this repository.

| Command                          | Description |
| -------------------------------- | ---         |
| `npm run docker:env`             | Sets the docker environment variables. This doesn't work exactly like you'd expect when you run it through NPM. It doesn't actually set the variables in your shell but in the environment that NPM is executing within. This is most useful when combined with other commands. NOTE: hmmmm. This needs explored.       |
| `npm run docker:pf`              | Starts the docker-pf port forwarding script in background mode. |
| `npm run docker:pf:down`         | Kills the docker-pf port forwarding script. |
| `npm run docker:build`           | Builds or rebuilds the images. Useful when you make changes to your `Dockerfile` or any of the files that are mentioned in your `Dockerfile`, like the `docker-entrypoint.sh`. |
| `npm run docker:up`              | Starts the port forwarding script and starts your servers. |
| `npm run docker:up -d`           | Starts the port forwarding script and starts your servers without log informations. |
| `npm run docker:up:daemon`       | Starts your servers as a background daemon. |
| `npm run docker:down`            | Stops the servers and stops the port forwarding script. |
| `npm run docker:down:dump`       | Dumps the DB to your local and then stops the servers. |
| `npm run docker:shell`           | Launches an interactive shell in the docker machine running WordPress. |
| `npm run docker:shell:wordpress` | Launches an interactive shell in the docker machine running WordPress. |
| `npm run docker:shell:db`        | Launches an interactive shell in the docker machine running your DB. |
| `npm run docker:db:dump`         | Zips up any existing dumps and then dumps the current schema and data to your local `data` directory. |
| `npm run docker:db:open`         | Launches Sequel Pro with an open connection to your current WordPress MySQL database. |
| `npm run docker:db:dump:schema`  | Zips up any existing schema dumps and dumps the current schema to your local `data` directory. |
| `npm run docker:db:dump:data`    | Zips up any existing data dumps and dumps the current data to your local `data` directory. |
| `npm run docker:db:roll:schema`  | Zips up any existing schema dumps and labels them with a timestamp in your local `data` directory. |
| `npm run docker:db:roll:data`    | Zips up any existing data dumps and labels them with a timestamp in your local `data` directory. |

### Enjoy your new environment! :)
