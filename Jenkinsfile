pipeline {
    agent any

tools {
maven "maven-master"
}
        stages{
            stage ("get scm"){
                steps{
                    git credentialsId: 'bd7bcfbd-6a0d-44f8-a724-1c9115e62687', url: 'https://github.com/manojsekharan/spring3-mvc-maven-xml-hello-world.git'
                }
             }
            
            stage ("gbuild"){
            steps {
                sh "mvn package"
            }
            }
            stage("archive artifact"){
            steps{
            archiveArtifacts 'target/*.war'
            }
            }
}
