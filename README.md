mqtt-scatter : *share mqtt subscriptions across many clients*
===========================================================

**mqtt-scatter** allows many clients to subscribe to a topic on an MQTT broker and have messages published to that topic distributed on a round-robin basis to all the subscribing clients.

This allows message-handling to be shared across many processes.

It runs a a proxy, or intermediary, passing through all MQTT traffic, apart from PUBLISH messages from the broker, which are passed on *only* to the next client in cyclic pool of subscribers.
 