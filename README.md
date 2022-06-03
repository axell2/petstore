# README

This README would normally document whatever steps are necessary to get the
application up and running.

Install docker in linux 
	sudo apt-get update
	sudo apt-get upgrade
	sudo apt-get install docker.io
	sudo systemctl start docker 
	sudo systemctl enable docker 
	sudo systemctl status docker 
	docker -v 
	sudo docker run hello-world 
Install docker-compose
	sudo apt-get install docker-compose 
	docker-compose version 
	sudo groupadd docker 
	sudo gpasswd -a ${USER} docker
	su - $USER
	docker container ls
Run Petstore on linux
	cd pets
	docker-compose up
	docker exec -it pets_pet_store_api_1 bash
	rails db:seed(optional)
Run Rspec test
	rspec -f documentation
POST example create a pet 
	curl -i -H "Content-Type:application/json" -X POST http://localhost:3000/v1/pets -d '{"id":400,"name":"firu", "tag": "dog"}'
GET listing of pets
	curl -i -H "Content-Type:application/json" -X GET http://localhost:3000/v1/pets?page=1
GET show pet by id
	curl -i -H "Content-Type:application/json" -X GET http://localhost:3000/v1/pets/1


