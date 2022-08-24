# Difference between API Types


## There are four main types of APIs

### RPC
- Stands for `Remote Procedure Call`
- Originating type of API based on simple client server architecture.
- Both, client and server use different call parameters.
- The conversion is needed to understand on the other side.
- This conversion is performed by dedicated pieces of code called `STUBS`.
- If the client calls the server in RPC API, a client STUB converts the parameters used in the function of the call.
- The server the decodes the parameters.
- RPC is around since the 80s.
- Today most of the big tech including Facebook, are using Google's RPC, called `gRPC` for their internal microservice architecture. 

### SOAP
- Released in 1999.
- Stands for `Simple Object Access Protocol`.
- It addresses the problem with XML based PRC APIs, which did not differentiate between data types.
- It uses SOAP messages, enclosed in SOAP envelope tag.
- Envelope contains a header and body.
- Header contains the metadata including `security token`.
- Body contains the response.
- SOAP has tight coupling, the changes made on client side should also be made on server side.

### REST
- `Representational State Transfer`.
- Initially, was used with SOAP.
- It uses HTTP methods.
- REST has supports constraints, defining the limits, which should not be crossed.
- Has `Client-Server Autonomy`, means teh client and the server don't care about each other's internal parts.
- REST provides session independence.
- States of prior requests are not stored since each request is considered to be the new request.
- REST is `chatty`, means the API which request the tremendous amount of distinct API calls.

### GraphQL
- Due to huge number of calls requirements of REST, `Facebook` came up with the alternative.
- GraphQL was launched in 2015.
- In REST, there are lot of endpoints to take care of.
- GraphQL endpoints can be customized by the clients. 
- Client decides how the data should be structured.