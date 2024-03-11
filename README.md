Networks and Distributed Systems Project 4 - Reliable Transport

HIGH-LEVEL APPROACH ----------------------------------------------------------------------------------------------------------------

Our high-level approach builds off of the starter code that we were given. We got annoyed of parsing out the data individually, so we just decided to parse all the data at the start and then pop it off the list as we needed to. Our approach included using a map to store the sequence number to the message and so we could access from the map without having to loop over a list every time. Our window size implemented TCP Tahoe congestion avoidance strategy and to handle the RTT we decided to use the formula from the slides to calculate it.

CHALLENGES ----------------------------------------------------------------------------------------------------------------

Most of the challenges that we faced dealt with how to implement certain things. To name a few, we got stuck on how to implement a sliding window, how to check for corrupted packets, and how to implement the changing window size. We were able to solve these issues by reading over the slides and doing external research on the TCP protocol. So, we realized that we needed to do a checksum for corrupted packets, a list/map to implement the sliding window, and also implement a formula to increase/decrease window size based on outputs.

GOOD FEATURES ----------------------------------------------------------------------------------------------------------------

We think that one of our best features that we implemented is the way we handle resends and calculate RTT. To handle resends while making sure our RTT wasn't too low, we had to use two dictionaries. One to handle the original time that the packet was sent, and one to handle the time the packet was resent. This ensured that our RTT calculations weren't messed up after resending a packet and it also allowed us to ensure we weren't resending packets right after another one.

TESTS ----------------------------------------------------------------------------------------------------------------

We tested our code by running the tests in the configs folder very often. This would let us know if we were on the right track, or we were completely wrong. Also, sometimes tests that were previously working, stopped working after some changes so it was helpful to keep our code correct. Alongside that, we also used print statements wherever we needed so that we could see what was going on with the internal workings of our code.
