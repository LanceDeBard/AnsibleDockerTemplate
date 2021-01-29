 This is a role to streamline the configuration and implementation of docker containers
 
    Configuration
    Files:
    vars/ contains a file with the docker container's information
    files/ contains a .xml file for firewalld configuration
    Two files need to be configured beforehands in vars/ and files/
    
    Variables: 
     defaults/main.yml
       containernames variable should contain a list of names for your container
        This list should correlate to the names of the Vars and Xml files
        {{ item }}Vars.yml <- This should be the name of the container's config in the vars/ directory
        {{ item }}.xml <- This should be the name of the firewalld xml file in the files/ directory
