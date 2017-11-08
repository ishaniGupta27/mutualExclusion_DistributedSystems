Lamport Mutual Exclusion Protocol

Social media are an important part of our social life these days. In this first project, We will implemented a common function in most apps: LIKE. We only have one post in the whole system which can be seen by all users. Each user could LIKE the post and you will need to keep track of the number of LIKEs. In other words, a user needs to get mutual exclusion over the counter for LIKE. We developed the application logic that uses Lamport’s Distributed Solution to achieve mutual exclusion.

Getting Started

1. Run application_for_post.py: This is the application containing the Post to be liked
2. Run multiple client.py with unique client number(python client.py 1): This is the clients trying to access the post

config.json maintains the config details about the number of clients and ports to be used for the application.


Prerequisites

Python 2.7

Application Components:

Clients are always curious about the number of likes associated with the post, and do so by reading numOfLikes. Clients need to communicate with each other to maintain the correct number of LIKEs.

Implementation:

1. Each client should store its own view of numOfLikes.
2. Each client should maintain a Lamport logical clock. We used the Totally-Ordered Lamport Clock, ie,h(Lamportclock, clientId) to break ties and each client should maintain its request queue.


Authors

Ishani Gupta
Vivek Pradhan



Acknowledgments

Thanks to Prof. Amr El Abbadi, Computer Science Department, UCSB
