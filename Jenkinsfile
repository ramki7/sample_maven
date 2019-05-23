pipeline {
    stage ('checkout') {
     git 'https://github.com/ramki7/sample_maven.git'
       
    }
    def MVNHOME =  tool name: 'mymaven', type: 'maven'
    stage ('compile') {
      
        sh "${MVNHOME}/bin/mvn compile test"
     }
    stage ('build')
    {
        sh "${MVNHOME}/bin/mvn package"
    }
    stage ('deploy')
    {
        
    }
    
}
