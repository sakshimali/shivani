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
bat 'mvn sonar:sonar -Dsonar.sources=src/ -Dsonar.host.url=http://localhost:9000 -Dsonar.login=94fca4c5ff9e6bda8cfa3b9ac8f7cea37d8fa82f'
}
}

 

stage('Deploy Application to Mulesoft Cloudhub'){
steps{
bat 'mvn package deploy -DmuleDeploy'
}
}

 

}
}
