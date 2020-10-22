# maven
maven basics

cmd line sheet sheet
http://maven.apache.org/ref/3.6.3/maven-embedder/cli.html

only download the dependency 

    mvn dependency:resolve

Download artifacts directly by passing the remote repository

    mvn dependency:get -DgroupId=org.apache.maven -DartifactId=maven-core -Dversion=2.2.1 -Dpackaging=jar -Dclassifier=sources -DremoteRepositories=central::default::https://repo.maven.apache.org/maven2,myrepo::::http://myrepo.com/maven2
    mvn dependency:get -DgroupId=org.apache.maven -DartifactId=maven-core -Dversion=2.2.1 -Dpackaging=jar -Dclassifier=sources -DremoteRepositories=https://repo.maven.apache.org/maven2 
    mvn dependency:get -Dartifact=org.apache.maven:maven-core:2.2.1:jar:sources -DremoteRepositories=https://repo.maven.apache.org/maven2 -Ddest=/tmp/myfile.jar
