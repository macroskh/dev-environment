# Laravel development environment

1. Copy `.env.example` to `.env`
2. Replace `USER_ID` and `GROUP_ID` with your local IDs
3. Set `PROJECT_NAME`. Note: [a-z+] only!
4. Setup/download/clone the main project into `src` directory e.g. `src/projectname.loc`. Note: don't forget permissions
5. Enjoy

Now you can enter to the container `docker exec -it {projectname}_php bash` to use `git`, `composer` etc.
