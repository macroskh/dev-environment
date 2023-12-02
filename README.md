# Laravel development environment

1. Copy `.env.example` to `.env`
2. Replace `USER_ID` and `GROUP_ID` with your local IDs
3. Set `PROJECT_NAME`. Note: [a-z+] only!
4. Setup/download/clone the main project into `src` directory e.g. `src/projectname.loc`.
5. Change base directory permissions `docker exec -it --user root {projectname}_php chown -R {userId}:{groupId} .`.

Enjoy

Now you can enter to the container `docker exec -it {projectname}_php bash` to use `git`, `composer` etc.
