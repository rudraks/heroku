* move my.buildpacks to root as .buildpacks
* Gemfile,Gemfile.lock & Procfile to root as well
* in composer.json update like require-dev and scrips as in samplecomposer.json
```
	"require-dev": {
		"codegyre/robo": "*",
		"heroku/heroku-buildpack-php": "*"
	},
	"scripts": {
		"post-update-cmd": "RudraX\\Project::setup",
		"compile": [
			"my_command"
		]
	}
``` 

* Run command
```
 $ heroku login
 $ heroku create app_name
 $ heroku config:add BUILDPACK_URL=https://github.com/ddollar/heroku-buildpack-multi.git
 $ git push heroku master
```