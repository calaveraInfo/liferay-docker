Liferay with tweaked configuration

#Build
sudo docker build -t calavera/liferay .

#Run
sudo docker run -p 8080:8080 --name liferay calavera/liferay
