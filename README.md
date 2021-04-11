# Docker for Go Developers

A talk given at Gopher Melbourne (AU) in April 2020

[![Slides](./DockerForGoDev.png)](https://docs.google.com/presentation/d/e/2PACX-1vR7TkrRr92YnDQKX0H3wmfZ4uCYNCMZf1JqlBHMTegQmOKJJc3d3dCS4kdJKbVrH-RiZu6s_Tnktr2s/pub?start=false&loop=false&delayms=3000)

## Simple example of building a Go server application in a Docker container

This talk uses the following for illustrative purposes.

Go API code adapted from https://github.com/HakaseLabs/source-blog/blob/master/rest-api/main.go

From this directory build with `docker image build -t api-server .`

Run with `docker container run -p 8089:8000 --rm -d api-server:latest`

Test with `curl -v http://0.0.0.0:9089/people`

Get Health check status with `docker container inspect --format '{{.State.Health.Status}}' <ID>"`
