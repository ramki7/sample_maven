pipeline {
    agent any
    stages {
        stage ('checkout'){
            step {
            git 'https://github.com/ramki7/sample_maven.git'
            } 
        }
        def MVNHOME =  tool name: 'mymaven', type: 'maven'
        stage ('compile'){
            step {
            sh "${MVNHOME}/bin/mvn compile test"
            }
        }
        stage ('build'){
            step {
            sh "${MVNHOME}/bin/mvn package"
            }
    }
    }
}
