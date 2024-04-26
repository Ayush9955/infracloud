#solutions

cd CSVSERVER

chmod +x gencsv.sh

./gencsv.sh 2 8

export CSVSERVER_BORDER=Orange

docker run -d --name csvserver -v "$(pwd)/solution/inputFile:/csvserver/inputdata" -e CSVSERVER_BORDER=Orange -p 9393:9300 infracloudio/csvserver:latest