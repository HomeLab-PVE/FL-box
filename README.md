# FL-box
 
### Instalare
1. Depindințe: cURL, Git, Docker-CE, Docker Compose
``` 
sudo apt install curl git

curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh

mkdir -p ~/.docker/cli-plugins/
curl -SL https://github.com/docker/compose/releases/download/v2.3.3/docker-compose-linux-x86_64 -o ~/.docker/cli-plugins/docker-compose
chmod +x ~/.docker/cli-plugins/docker-compose
```  
2. Git Clone
``` 
cd /
git clone https://github.com/HomeLab-PVE/FL-box.git
cd /FL-box
```  
3. Crează și editează fișier .env
``` 
cp .env-model .env
nano .env
```  

4. Crează foldere (dacă rulează într-un CT și sunt adăugate via .conf, nu mai este necesar)
``` 
mkdir -p /data/flbox/media/movies/hd /data/flbox/media/series/hd
mkdir -p /data/flbox/media/movies/4k /data/flbox/media/series/4k
``` 

5. Rulează docker compose
``` 
docker compose -f FL-box.yaml up -d
``` 
Pentru a opri containerele Docker:
`docker compose -f FL-box.yaml down`
