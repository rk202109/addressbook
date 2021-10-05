pipeline {
    agent any
    environment {
        export JAVA_HOME="/Library/Java/JavaVirtualMachines/jdk1.8.0_301.jdk/Contents/Home"
        export MAVEN_HOME="/users/rkagathi/downloads/apache-maven-3.8.3"
        export PATH="$JAVA_HOME/bin:$MAVEN_HOME/bin:$PATH"
    }
    stages {
        stage('Compile') {
            steps { 
                sh 'mvn compile'
            }
        }
        stage('test') {
            steps { 
                sh 'mvn test'
            }
        }
        stage('package') {
            steps { 
                sh 'mvn package'
            }
        }
    }
}
