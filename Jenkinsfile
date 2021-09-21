pipeline
{
agent any
stages{
stage('Build Application'){
steps{
bat 'mvn clean install'
}
}

 

stage('SonarQube Testing'){
steps{
bat 'mvn sonar:sonar -Dsonar.sources=src/ -Dsonar.host.url=http://localhost:9000 -Dsonar.login=902a8bc8c25e483a73913b1b39ab59607643cdcf'
}
}

 

stage('Deploy Application to Mulesoft Cloudhub'){
steps{
bat 'mvn package deploy -DmuleDeploy'
}
}

 

}
}
