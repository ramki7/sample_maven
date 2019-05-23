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
                MVNHOME =  tool name: 'mymaven', type: 'maven'
                sh "${MVNHOME}/bin/mvn compile test"
            }
        }
        stage ('build'){
            steps {
                MVNHOME =  tool name: 'mymaven', type: 'maven'
                sh "${MVNHOME}/bin/mvn package"
            }
    }
    }
}
