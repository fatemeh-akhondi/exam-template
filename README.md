# Scenario 1

Use one heading for each problem.
Write what was wrong and how you fixed it.
Paste the config you changed (only the changed part).
Paste the commands you used.
Write every step you tried, even guesses.

English is better. Persian is OK.

## Problem 1: (short name)

What was wrong:

How I fixed it:
resolvectl didn't work -> 
```
sudo systemctl start systemd-resolved
```
couldn't edit /etc/resolved.conf
```
chattr -i /run/systemd/resolve/stub-resolv.conf
```
restarted resolved again so i would change

then i installed docker compose!

backend-db network was not in the docker compose for backend


Config I changed (only the changed part):

in docker-compose.yml
```
  networks:
      - backend-db-net
      - nginx-backend-net

```
/etc/resolved.conf was also changed by system not me:)

Commands I used:

i put both problems and fixed in the first part!


# Extra problems
docker compose wouldn't install
docker compose versions interfered with each other and i had to ask ai what to do
this was the error
```
KeyError: 'ContainerConfig'
```
so i did this
```
docker compose up -d --build --force-recreate
docker compose logs --tail=100 backend
docker-compose stop backend
docker-compose rm -f backend
docker-compose up -d --build backend
docker-compose logs --tail=100 backend
```

For example:
+ Weak Internet connection (10 min)

