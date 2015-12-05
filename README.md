Liferay with tweaked configuration

#Build
sudo docker build -t calavera/liferay .

#First run
sudo docker run -p 8080:8080 --name liferay calavera/liferay

#Subsequent run
sudo docker run --volumes-from liferay -p 8080:8080 calavera/liferay

#Deploy
sudo docker run --rm --volumes-from liferay -v `pwd`:`pwd` -w `pwd` --entrypoint /bin/cp calavera/liferay ./target/*.war /var/liferay-home/deploy
