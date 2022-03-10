# NodejsExpressMovieLists
NodejsExpressMovieLists <br />

# Database DDL ( Mysql Localhost )
CREATE DATABASE `dbmovie`;  <br />
Use dbmovie;   <br />
CREATE TABLE `movies` (  <br />
  `id` bigint(20) unsigned NOT NULL AUTO_INCREMENT,  <br />
  `judul` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL,  <br /> 
  `rating` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL,  <br />
  `deskripsi` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL,  <br />
  `foto` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL, <br />
  `rilis` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL,  <br />
  `durasi` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL,  <br />
  `sutradara` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL, <br /> 
  `pemain` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL, <br />
  `created_at` timestamp NULL DEFAULT NULL,  <br />
  `updated_at` timestamp NULL DEFAULT NULL,  <br />
  PRIMARY KEY (`id`)  <br />

);  <br />


# Postman CRUD for Movies Collection
{<br />
	"info": {<br />
		"_postman_id": "91a7e2d5-7987-4ae1-b488-ed23bcf4bbb9",<br />
		"name": "LatihanNodejsMovies",<br />
		"schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json"<br />
	},<br />
	"item": [<br />
		{<br />
			"name": "add",<br />
			"request": {<br />
				"method": "POST",<br />
				"header": [],<br />
				"body": {<br />
					"mode": "raw",<br />
					"raw": "{\"judul\":\"the bat\",\n\"rating\":\"5\",\n\"deskripsi\":\"oke\",\n\"foto\":\"batman.jpg\"\n}",<br />
					"options": {<br />
						"raw": {<br />
							"language": "json"<br />
						}<br />
					}<br />
				},<br />
				"url": {<br />
					"raw": "localhost:5000/api/movies?",<br />
					"host": [ <br />
						"localhost" <br />
					], <br />
					"port": "5000",<br />
					"path": [<br />
						"api",<br />
						"movies"<br />
					],<br />
					"query": [<br />
						{<br />
							"key": "",<br />
							"value": null<br />
						}<br />
					]<br />
				}<br />
			},<br />
			"response": []<br />
		},<br />
		{<br />
			"name": "Get",<br />
			"request": {<br />
				"method": "GET",<br />
				"header": [],<br />
				"url": {<br />
					"raw": "localhost:5000/api/movies",<br />
					"host": [<br />
						"localhost"<br />
					],<br />
					"port": "5000",<br />
					"path": [<br />
						"api",<br />
						"movies"<br />
					]<br />
				}<br />
			},<br />
			"response": []<br />
		},<br />
		{<br />
			"name": "Update",<br />
			"request": {<br />
				"method": "PUT",<br />
				"header": [],<br />
				"body": {<br />
					"mode": "raw",<br />
					"raw": "{\"judul\":\"the batman\",\n\"rating\":\"5\",\n\"deskripsi\":\"oke\",\n\"foto\":\"batman.jpg\"\n}",<br />
					"options": {<br />
						"raw": {<br />
							"language": "json"<br />
						}<br />
					}<br />
				},<br />
				"url": {
					"raw": "localhost:5000/api/movies/10",<br />
					"host": [<br />
						"localhost"<br />
					],<br />
					"port": "5000",<br />
					"path": [<br />
						"api",<br />
						"movies",<br />
						"10"<br />
					]<br />
				}<br />
			},<br />
			"response": []<br />
		},<br />
		{<br />
			"name": "Delete",<br />
			"request": {<br />
				"method": "DELETE",<br />
				"header": [],<br />
				"url": {<br />
					"raw": "localhost:5000/api/movies/10",<br />
					"host": [<br />
						"localhost"<br />
					],<br />
					"port": "5000",<br />
					"path": [<br />
						"api",<br />
						"movies",<br />
						"10"<br />
					]<br />
				}<br />
			},<br />
			"response": []<br />
		}<br />
	]<br />
}
