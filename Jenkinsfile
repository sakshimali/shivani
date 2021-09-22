pipeline
{
agent any
stages{
stage('Build Application'){
steps{
bat 'mvn -B -U -e -V clean -DskipTests package'
}
}

 

stage('SonarQube Testing'){
steps{
bat 'mvn sonar:sonar -Dsonar.sources=src/ -Dsonar.host.url=http://localhost:9000 -Dsonar.login=d92e59d37456cd16e45cecbee172b5aedbbea210'
}
}

 

stage('Deploy Application to Mulesoft Cloudhub'){
steps{
bat 'mvn  deploy -DmuleDeploy'
}
}
}
}
