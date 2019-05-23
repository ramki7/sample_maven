pipeline {
    agent any
    stages {
        stage ('checkout'){
            steps {
                git 'https://github.com/ramki7/sample_maven.git'
            } 
        }
        def MVNHOME =  tool name: 'mymaven', type: 'maven'
        stage ('compile'){
            steps {
                sh "${MVNHOME}/bin/mvn compile test"
            }
        }
        stage ('build'){
            steps {
                sh "${MVNHOME}/bin/mvn package"
            }
    }
    }
}
