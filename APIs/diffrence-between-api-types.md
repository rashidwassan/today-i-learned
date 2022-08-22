# Difference between API Types


## There are four main types of APIs

### REST

### SOAP

### GraphQL

### RPC
- Stands for `Remote Procedure Call`
- Originating type of API based on simple client server architecture.
- Both, client and server use different call parameters.
- The conversion is needed to understand on the other side.
- This conversion is performed by dedicated pieces of code called `STUBS`.
- If the client calls the server in RPC API, a client STUB converts the parameters used in the function of the call.
- The server the decodes the parameters.
- RPC is around since the 80s.