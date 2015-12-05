Liferay with tweaked configuration

#Build
sudo docker build -t calavera/liferay .

#Run
First:
sudo docker run -p 8080:8080 --name liferay calavera/liferay

Regular:
sudo docker run --volumes-from liferay -p 8080:8080 calavera/liferay
