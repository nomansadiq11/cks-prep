# Stateful vs Stateless

## Stateful

Many network protocols keep track of the session states which can be categories in 4 different

### New

Typically referes to the 3 way TCP handshake, and ca be handshek of any similar protocol

### Established

The majortity of the traffic is likely to be under the established category. Placing rule for established at the beginning of the ruleset can improve performance

### related

is a unique that not all the firewall capable of considierin a package as related to an established connection. Netfilter requires additional protocol-specfic module to track related traffice.
FTP and VOIP require extra kernal modules to be loaded, werheas replied to DNS queries will automaticallbe considered as related to a known outbound DNS request.

### Invalid

- Traffice is that which is out of sequence according tot he protocol specificiations.
- Stateful packet filtering requires more system resouces as a table of connections and their relations/stagtes in held in memory.
