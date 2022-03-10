# NodejsExpressMovieLists
NodejsExpressMovieLists

# Database DDL ( Mysql Localhost )
CREATE DATABASE `dbmovie`; \n
Use dbmovie;  \n
CREATE TABLE `movies` (  \n
  `id` bigint(20) unsigned NOT NULL AUTO_INCREMENT,  \n
  `judul` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL,  \n
  `rating` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL, \n
  `deskripsi` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL, \n
  `foto` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL, \n
  `rilis` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL, \n
  `durasi` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL, \n
  `sutradara` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL, \n
  `pemain` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL, \n
  `created_at` timestamp NULL DEFAULT NULL, \n
  `updated_at` timestamp NULL DEFAULT NULL, \n
  PRIMARY KEY (`id`) \n

); \n


# Postman CRUD for Movies Collection
{
	"info": {
		"_postman_id": "91a7e2d5-7987-4ae1-b488-ed23bcf4bbb9",
		"name": "LatihanNodejsMovies",
		"schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json"
	},
	"item": [
		{
			"name": "add",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\"judul\":\"the bat\",\n\"rating\":\"5\",\n\"deskripsi\":\"oke\",\n\"foto\":\"batman.jpg\"\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "localhost:5000/api/movies?",
					"host": [
						"localhost"
					],
					"port": "5000",
					"path": [
						"api",
						"movies"
					],
					"query": [
						{
							"key": "",
							"value": null
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "Get",
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "localhost:5000/api/movies",
					"host": [
						"localhost"
					],
					"port": "5000",
					"path": [
						"api",
						"movies"
					]
				}
			},
			"response": []
		},
		{
			"name": "Update",
			"request": {
				"method": "PUT",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\"judul\":\"the batman\",\n\"rating\":\"5\",\n\"deskripsi\":\"oke\",\n\"foto\":\"batman.jpg\"\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "localhost:5000/api/movies/10",
					"host": [
						"localhost"
					],
					"port": "5000",
					"path": [
						"api",
						"movies",
						"10"
					]
				}
			},
			"response": []
		},
		{
			"name": "Delete",
			"request": {
				"method": "DELETE",
				"header": [],
				"url": {
					"raw": "localhost:5000/api/movies/10",
					"host": [
						"localhost"
					],
					"port": "5000",
					"path": [
						"api",
						"movies",
						"10"
					]
				}
			},
			"response": []
		}
	]
}
