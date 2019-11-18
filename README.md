# Aetna-devsecops-coding-test
Version 2
devsecops-coding-test

Readme.md
Royal C. Jackson Jr. blackshark37@gmail.com

Date: 11.17.2019

Prerequistes and Assumptions


Docker PHP Environment is not complete, so the dockerfile was
create for a not complete Docker PHP Containerization Environment.
Cannot create the Docker PHP Environment due to I do not have the
correct Windows 10 version.

Structuring the Docker setup for PHP Projects
Environment:
,Php
,Docker
,Phpcoder
http

Test php code: https://www.w3schools.com/php/phptryit.asp?filename=tryphp_func_array_merge

Location of Coding Test: https://github.com/aetnahealth/devsecops-coding-test

https://www.tutorialrepublic.com/faq/how-to-merge-two-or-more-arrays-into-one-array-in-php.php

https://www.php.net/manual/en/function.array-merge.php

https://www.w3schools.com/php/func_array_merge.asp

Create a new repository on github

Clone the repository to the Docker Environment

Php

phpmyadmin

php-worker

C:\Users\redvulture>php -v

PHP 7.1.6 (cli) (built: Jun  8 2017 02:06:32) ( ZTS MSVC14 (Visual C++ 2015) x86 )
Copyright (c) 1997-2017 The PHP Group
Zend Engine v3.1.0, Copyright (c) 1998-2017 Zend Technologies

Docker
Build the container

Run the environment

docker run -d --name docker-php -v "C:/Aetna-devsecops-coding-test-repository.io/":/var/www php:7.0-cli

Which means:

docker run                                    // run a container

-d                                            // in the background (detached)

--name docker-php                             // named docker-php

-v "C:/Aetna-devsecops-coding-test-repository.io/":/var/www           // sync the directory C:/codebase/docker-php/app on the windows host with /var/www in the container

                                         
php:7.0-cli                                   // use this image to build the container

In this exercise you can use any language of your choice, except shell script. 
The goal is to implement a function that combines 2 sorted arrays into a single 
sorted array. The function should be invoked from command line with the 2 sorted 
arrays as the arguments.
Here are sample inputs and outputs:

```
$ function_name [1, 2, 7, 9] [3, 6, 8]
> [1, 2, 3, 6, 7, 8, 9]

$ function_name [6, 8, 9] [1, 4, 6]
> [1, 4, 6, 6, 8, 9]

$ function_name [] [1, 2, 3]
> [1, 2, 3]
```

The next step is to containerize the function. The end result should look like this:

```
$ docker run <image>:<tag> [1, 2, 7, 9] [3, 6, 8]
> [1, 2, 3, 6, 7, 8, 9]
```

Create a public github repo for this exercise and include all files required to 
build and run the containerized function. Use a README for build and run steps 
if necessary. Please submit the github repo within a week of receiving the exercise.
