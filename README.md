Wercker Oracle Java 8 box
=========================

Wercker box with Oracle Java 8 and maven and gradle installed

Basic working example 
---------------------

To build simple Spring Boot application You just have to create ```wercker.yml``` file with following content and place in the root of your Java project.

```yml
box: mihkels/java8-oracle@0.0.1
build:
  steps:
    - script:
        name: Show base information
          code: |
            gradle -v
            echo $JAVA_HOME
            java -version
            javac -version
      - script:
          name: Run gradle
          code: |
            gradle --full-stacktrace -q --project-cache-dir=$WERCKER_CACHE_DIR assamble
```


