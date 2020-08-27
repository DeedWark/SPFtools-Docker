# Kitterman-Docker

This is Kitterman in a Docker image
## Installation

You need docker installed on your machine -> [install](https://docs.docker.com/get-docker/)

```bash
docker build -t kitterman .
```

## Usage

```bash
#docker run --rm kitterman spf.py IP sender_address helo
docker run --rm kitterman spf.py 10.11.12.13 mail@kitterman.com smtp.kitterman.com

#Custom SPF
docker run --rm kitterman spf.py "v=spf1 include:spf.kitterman.com" 10.11.12.13 mail@kitterman.com smtp.kitterman.com
```
## Alias
Put that into your aliases file
```
alias kitterman='docker run --rm kitterman spf.py'
```

Then you can just do

- SPF
```bash
#kitterman IP sender helo
kitterman 10.11.12.13 mail@kitterman.com smtp.kitterman.com
```
- Custom SPF
```bash
#kitterman "SPF" IP sender helo
kitterman "v=spf1 include:spf.kitterman.com -all" mail@kitterman.com smtp.kitterman.com
```

# Official website
[Kitterman](https://www.kitterman.com/spf/validate.html)
