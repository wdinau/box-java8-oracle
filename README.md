Wercker Oracle Java 8 box
=========================

A Total plagiarism thanks to mihkels/box-java8-oracle
I didn't need gradle as I'm using gradle wrapper

wercker.yml 
---------------------

```yml
box: wdinau/java8@0.0.1
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
            ./gradlew clean build
```


