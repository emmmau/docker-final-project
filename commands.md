#> docker run
		--name web
		--link mysql:mysql
		-d
		-p 8080:80
		-v /opt/www/worldapi

		--name mysql
		-e MYSQL_ROOT_PASSWORD=123456
		-e MYSQL_DATABASE=dbdemo 
		-e MYSQL_USER=devspark
		-e MYSQL_PASSWORD=dev123
		-d
		mysql:latest
