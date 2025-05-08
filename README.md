# 🎬 Redis Practical Exercise – Movies & Actors

This repository contains a practical Redis-based project completed for a NoSQL course. The goal is to explore Redis's capabilities by managing and querying data related to actors and movies.

## 📁 Project Structure

├── data/
│ ├── actors.redis # Redis HSET commands to insert actors
│ └── movies.redis # Redis HSET commands to insert movies
├── redis_notebook.ipynb # Jupyter notebook for querying and manipulating Redis data
├── docker-compose.yml # Docker services: Redis, RedisInsight
├── results.pdf # Answers to data queries (submitted as part of the exercise)
└── README.md # Project documentation (this file)

## ⚙️ Setup Instructions

1. Clone the Repository
  git clone https://github.com/yourusername/redis-practical-exercise.git
  cd redis-practical-exercise

2. Start Redis and RedisInsight
    docker-compose up -d

3. Load the Data into Redis

 Get-Content data/actors.redis | docker exec -i redis-server redis-cli
 Get-Content data/movies.redis | docker exec -i redis-server redis-cli


4. Install Python Dependencies for Jupyter
    pip install redis jupyter


5. Start Jupyter Notebook
    jupyter notebook


🧪 Exercise Tasks
Count how many actors and movies are stored in Redis.

Query actors born before 1980.

Retrieve genre and rating of "The Imitation Game".

List top 5 highest-rated movies.

Count movies with rating above 7.5.

Update rating of "The Imitation Game" to 8.5.

Add a new actor "Zendaya".

Delete the movie "The Room".


👨‍💻 Author
Akshay – NoSQL course submission
