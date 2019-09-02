# Bee Queue
A simple, fast, robust job/task queue for Node.js, backed by Redis.
Redis is a performed database.

## Installation
	yarn add bee-queue


## Documentation
https://github.com/bee-queue/bee-queue


## Settings

### Step 01
Create a new folder "jobs" inside de "app" folder.In this folder will be all the jobs thaht will execute in the queue.

### Step 02
Inside "jobs" folder create a "CancellationMail.js" class thats represent a cancellation mail job.
* [Cancellation mail class example]( https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Bee-Queue/CancellationMail.txt)

### Step 03
Create a "Queue" class inside the "lib" folder to storage all the jobs that will be executed.
* [Queue class example](https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Bee-Queue/Queue.txt)

### Step 04
Call the function add in some controller to execute the job that you want.
You need to import your Queue class.
```bash
await Queue.add(CancellationMail.key, {
  appointment,
});
```

### Step 05
Create a "queue.js" file inside "src" folder, this file is necessary to execute the queues in isolation so you can run the queues in another terminal.
```bash
# * add a "queue" script in your "package.json" to execute the queue isolated.
"queue": "nodemon src/queue.js"
```
* [queue example](https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Bee-Queue/queue.txt)





