#Layered System Architecture

Using a connectionless protocol can be efficient, but it is not easy to make the protocol resistant to occasional transmission failures. If a message is lost or 
corrupted, the client may need to resend the request. However, this can cause problems if the original request was already processed. If the request is idempotent, 
meaning it can be repeated without harm, it is okay to resend the request. But for non-idempotent requests, it is better to report an error instead of repeating the 
operation. There is no single solution for dealing with lost messages, and further discussion on handling transmission failures is deferred to another section.
