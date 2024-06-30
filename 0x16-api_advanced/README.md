# Reddit API Project

This project contains Python scripts that interact with the Reddit API to perform various tasks.

## Task 0: How many subs?

Write a function `number_of_subscribers(subreddit)` that queries the Reddit API and returns the number of subscribers for a given subreddit. If the subreddit is invalid, the function returns 0.

### Requirements:
- Prototype: `def number_of_subscribers(subreddit)`
- If not a valid subreddit, return 0.
- Use a custom User-Agent to avoid Too Many Requests errors.

### Example Usage:
```bash
$ python3 0-main.py programming
756024
$ python3 0-main.py this_is_a_fake_subreddit
0
```

## Task 1: Top Ten
- Write a function top_ten(subreddit) that queries the Reddit API and prints the titles of the first 10 hot posts listed for a given subreddit.

### Requirements:
- Prototype: `def top_ten(subreddit)`
- If not a valid subreddit, print None.
- Ensure not to follow redirects for invalid subreddits.

### Example Usage:

```bash
$ python3 1-main.py programming
Firebase founder's response to last week's "Firebase Costs increased by 7000%!"
How a 64k intro is made
HTTPS on Stack Overflow: The End of a Long Road
...
PyCon 2017 Talk Videos
$ python3 1-main.py this_is_a_fake_subreddit
None
```

## Task 2: Recurse it!
- Write a recursive function recurse(subreddit, hot_list=[]) that queries the Reddit API and returns a list containing the titles of all hot articles for a given subreddit. If no results are found for the given subreddit, the function should return None.

### Requirements:
- Prototype: `def recurse(subreddit, hot_list=[])`
- If not a valid subreddit, return None.
- Use recursion to fetch all results without using loops.

### Example Usage:
```bash
$ python3 2-main.py programming
932
$ python3 2-main.py this_is_a_fake_subreddit
None
```