pipeline {
       agent any
       
    tools {
         maven "jenkin-maven"
    }
    
    
    stages {
          stage('SCM') {
              steps {
                   git 'https://github.com/ashwin1-dev/14-nov-war.git'
                   }
                       }
                       
            stage('BUILD') {
                steps {
                       sh "mvn  clean test package "
                      }
                           }
                           
            stage('DEPLOY') {
               
                steps {
                   sh " scp /var/lib/jenkins/workspace/pipe5/target/vle2.war  192.168.0.32:/opt/apache-tomcat-9.0.54/webapps "
                      }
                           }
    }
}
