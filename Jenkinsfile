//pipeline {
  //agent any
  //stages {
   // stage('Print Hostname') {
     // steps {
       //     sh 'hostname'
     // }
   // }
 // }
//}
pipeline {
  agent any
    env.JAVA_HOME= tool name: 'myjava', type: 'jdk'
    def mavehHome= tool name: 'myMaven', type: 'maven'
        def mvnCMD= "${mavehHome}/bin/mvn"
  stages 
 {
    stage('FetchGitCode') 
    {
       git 'https://github.com/atmarampradhan/sparkjava-war-example.git'
    }
    
     stage('Compile')
    {
       sh "${mvnCMD} compile"
       echo "Maven packaging -DskipTests"
    } 
 }
}
