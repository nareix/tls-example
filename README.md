tls-example
===========

Golang TLS example. x509 certificate create and sign.

Usage:


    go run gen.go
    2013/11/25 14:47:48 write to ca.pem
    2013/11/25 14:47:48 write to ca.key
    2013/11/25 14:47:49 write to cert2.pem
    2013/11/25 14:47:49 write to cert2.key
    2013/11/25 14:47:49 check signature true
    
    go run server.go
    2013/11/25 14:49:48 server: listening
    2013/11/25 14:49:54 server: accepted from 127.0.0.1:50207
    2013/11/25 14:49:54 server: conn: waiting
    2013/11/25 14:49:54 {[China] [Fuck] [FuckU] [] [] [] []   [{[2 5 4 6] China} {[2 5 4 10] Fuck} {[2 5 4 11] FuckU}]}
    2013/11/25 14:49:54 server: conn: echo "Hello\n"
    2013/11/25 14:49:54 server: conn: wrote 6 bytes
    2013/11/25 14:49:54 server: conn: waiting
    2013/11/25 14:49:54 server: conn: read: EOF
    2013/11/25 14:49:54 server: conn: closed  
      
    go run client.go
    2013/11/25 14:49:21 client: connected to:  127.0.0.1:443
    2013/11/25 14:49:21 client: handshake:  true
    2013/11/25 14:49:21 client: mutual:  true
    2013/11/25 14:49:21 client: wrote "Hello\n" (6 bytes)
    2013/11/25 14:49:21 client: read "Hello\n" (6 bytes)
    2013/11/25 14:49:21 client: exiting  
