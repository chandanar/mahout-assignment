# mahout-assignment
CS5229-Mahout Assignment

Running Steps:

1. wget http://files.grouplens.org/datasets/movielens/ml-1m.zip
2. pwd
3. ls
4. unzip ml-1m.zip
5. cat ml-1m/ratings.dat | sed 's/::/,/g' | cut -f1-3 -d, > ratings.csv
6. head ratings.csv
7. hadoop fs -put ratings.csv /ratings.csv
8. mahout recommenditembased --input /ratings.csv --output recommendations --numRecommendations 10 --outputPathForSimilarityMatrix similarity-matrix --similarityClassname SIMILARITY_COSINE
9. hadoop fs -ls recommendations
10. hadoop fs -cat recommendations/part-r-00000 | head
11. sudo easy_install twisted
12. sudo easy_install klein
13. sudo easy_install redis
14. wget http://download.redis.io/releases/redis-2.8.7.tar.gz
15. ls
16. tar xzf redis-2.8.7.tar.gz
17. cd redis-2.8.7
18. make
19. ./src/redis-server &
20. cd /home/hadoop/
21. vim hello.py
22. twistd -noy hello.py &
23. curl localhost:8090/37
24. curl localhost:8090/35


