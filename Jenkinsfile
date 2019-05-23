pipeline {
    agent any
    stages {
        stage ('checkout'){
            steps {
                git 'https://github.com/ramki7/sample_maven.git'
            } 
        }
        
        stage ('compile'){
            steps {
                tool name: 'mymaven', type: 'maven'
                sh "mymaven/bin/mvn compile test"
            }
        }
        stage ('build'){
            steps {
                tool name: 'mymaven', type: 'maven'
                sh "mymaven/bin/mvn package"
            }
    }
    }
}
