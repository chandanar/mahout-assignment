# mahout-assignment
CS5229-Mahout Assignment

Running Steps:

wget http://files.grouplens.org/datasets/movielens/ml-1m.zip
pwd
ls
unzip ml-1m.zip
cat ml-1m/ratings.dat | sed 's/::/,/g' | cut -f1-3 -d, > ratings.csv
head ratings.csv
hadoop fs -put ratings.csv /ratings.csv
mahout recommenditembased --input /ratings.csv --output recommendations --numRecommendations 10 --outputPathForSimilarityMatrix similarity-matrix --similarityClassname SIMILARITY_COSINE
hadoop fs -ls recommendations
hadoop fs -cat recommendations/part-r-00000 | head
sudo easy_install twisted
sudo easy_install klein
sudo easy_install redis
wget http://download.redis.io/releases/redis-2.8.7.tar.gz
ls
tar xzf redis-2.8.7.tar.gz
cd redis-2.8.7
make
./src/redis-server &
cd /home/hadoop/
vim hello.py
twistd -noy hello.py &
curl localhost:8090/37
curl localhost:8090/35


