# TLS/SSL Demo

## Introduction

SSL server/client programming using OpenSSL in C



## Dependencies

- libssl

- libcrypto

  

## How to build

`mkdir build`

`cd build`

`cmake ..`

`make`



## How to run

1. Generate certificate

   `cd build`  

   `openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout mycert.pem -out mycert.pem`

2. Start server 

   `cd build`

   `./tlsDemoServer <port_number>`

3. Start client

    `cd build`

    `./tlsDemoClient 127.0.0.1 <port_number>`

NOTE: One must start server and client in different terminals

int main()
{
	cout<<"hi"<<endl;
	return 0;
}
