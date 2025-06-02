# 🎬 Redis Practical Exercise – Movies & Actors

This repository contains a practical Redis-based project completed for a NoSQL course. The goal is to explore Redis's capabilities by managing and querying data related to actors and movies.

## 📁 Project Structure

├── data/<br>
│ ├── actors.redis # Redis HSET commands to insert actors<br>
│ └── movies.redis # Redis HSET commands to insert movies<br>
├── redis_notebook.ipynb # Jupyter notebook for querying and manipulating Redis data<br>
├── docker-compose.yml # Docker services: Redis, RedisInsight<br>
├── results.pdf # Answers to data queries (submitted as part of the exercise)<br>
└── README.md # Project documentation (this file)<br>

## ⚙️ Setup Instructions

1. Clone the Repository
  ```
  git clone https://github.com/yourusername/redis-practical-exercise.git
  cd redis-practical-exercise
```

3. Start Redis and RedisInsight
   ```
     docker-compose up -d
   ```

4. Load the Data into Redis

 ```
 Get-Content data/actors.redis | docker exec -i redis-server redis-cli
 Get-Content data/movies.redis | docker exec -i redis-server redis-cli
```

4. Install Python Dependencies for Jupyter
```
pip install redis jupyter
```

6. Start Jupyter Notebook

   ```
   jupyter notebook

🧪 Exercise Tasks
  1. Count how many actors and movies are stored in Redis.
  2. Query actors born before 1980.
  3. Retrieve genre and rating of "The Imitation Game".
  4. List top 5 highest-rated movies.
  5. Count movies with rating above 7.5.
  6. Update rating of "The Imitation Game" to 8.5.
  7. Add a new actor "Zendaya".
  8. Delete the movie "The Room".


## 👨‍💻 Author
Akshay – NoSQL course submission
