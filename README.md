
# Dependencies 
1. Docker(prefelly the most current version)

# Installation.

1. Clone this protect.
1. **git clone https://github.com/dbogarin/neustartest.git**
1. Open a terminal and go to the repo folder called **neustarttest**.
1. Run **docker-compose up**, this will prepare our containers.
1. Run **docker containe ls**, to see all runing containers.
1. ![alt text](/readme/images/dockerls.jpg)
1. Run the following command **docker exec -it 63f6f9245b71  /bin/sh -c "[ -e /bin/bash ] && /bin/bash || /bin/sh"**
1. The number must match to the php container in **step 6**.
1. Now inside the container, **run composer install**.
1. ![alt text](/readme/images/composerinstall.jpg)
1. Just in case run, **composer update** and **composer dumpa**.
1. Run **php artisan migrate:refresh**.
1. Open a browser and go to localhost
1. ![alt text](/readme/images/localhost.jpg)

Now The api is ready to use!

# How to use the Client Front End

1. Go to the proyect folder and then **app-frontend**.
1. Open **index.html**
1. ![alt text](/readme/images/frontend.png)

# Unit Test
1. Run **docker containe ls**, to see all runing containers.
1. ![alt text](/readme/images/dockerls.jpg)
1. Run the following command **docker exec -it 63f6f9245b71  /bin/sh -c "[ -e /bin/bash ] && /bin/bash || /bin/sh"**
1. The big nummber must match to the php container in step .
1. Run **php artisan test**
1. ![alt text](/readme/images/unitest.jpg)
1. You will see all results runing

# Extra - Postman

If you want to test with *Postman*. You can import this [json](https://www.postman.com/collections/721d55588fa26332f0c8).

How to import a collection in postman go [here](https://kb.datamotion.com/?ht_kb=postman-instructions-for-exporting-and-importing).

![alt text](/readme/images/postman.png)

# Files to keep in mind
Just in case, there is a list of the most important files for this test.

1. routes/api.php
1. app/Http/Controllers/DomainController.php
1. app/Domains.php
1. tests/Feature/DomainsTest.php
1. database/database.sqlite
1. docker-compose.yml
1. app-frontend
1. database/migrations/2020_08_05_041635_create_domains_table.php
