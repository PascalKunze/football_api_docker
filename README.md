1. Erstelle ein Ordner in einem passenden Verzeichniss mit einem passenden Name Bsp.:
  - cd /var/www/html
  - mkdir fußball_api_projekt
2. Erstelle in diesem Ordner  weiter Ordner:
  - mkdir html
  - mkdir mysql
3. Bleib im "fußball_api_projekt" Verzeichniss und kopiere das git repo: PascalKunze/fußball_api_docker
  -cd /var/www/html/fußball_api_projekt/
  -git clone git@github.com:PascalKunze/football_api_docker.git
4. Bearbeite die docker-compose-yml:
  -cd /var/www/html/fußball_api_projekt/football_api_docker
  -vi docker-compose.yml
  -Dücke "i" zum bearbeiten
  -ändere "container_name" für http-php Bsp.: "fussball-php" (kein ß)
  -ändere "volumes" für http-php aber nur den Pfad Bsp.:
  var/www/html/fußball_api_projekt/html:/var/www/html/ -> var/www/html/{dein Ordner}/html:/var/www/html/
  -ändere "volumes" für mysql aber nur den Pfad Bsp.:
  var/www/html/fußball_api_projekt/mysql:/var/lib/mysql -> var/www/html/{dein Ordner}/mysql:/var/lib/mysql
  --ändere "container_name" für mysql Bsp.: "fussball-mysql" (kein ß)
5. Füge die ports in die hosts Datei
  -vi /etc/hosts
  -drücke "i" zum bearbeiten
  -füge ein an einem Freien Platz: 127.0.0.1 fußball.local
  -speichern
