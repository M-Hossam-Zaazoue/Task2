# Task 2
## Docker Task

#### Setup

- Server VM Ubuntu with IP address `192.168.10.137`

#### Commands

1. Clone repository 
```
git clone https://github.com/M-Hossam-Zaazoue/Task2.git
```

2. Build our own Webserver Image (Note: this Step can be skipped; Image is pushed to Docker Hub)
```
docker build -t m0hossam0zaazoue/webserver ~/Task2
```

3. Run docker compose
```
docker-compose -f ~/Task2/stack.yaml up
```

4. Open host Ports to reach container Ports
```
firewall-cmd --add-port 8000/tcp --add-port 8080/tcp
firewall-cmd --permanent --add-port 8000/tcp --add-port 8080/tcp
```