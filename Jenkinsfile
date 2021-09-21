pipeline
{​​​
agent any
stages{​​​
stage('Build Application'){​​​
steps{​​​
bat 'mvn clean install'
}​​​
}​​​

stage('SonarQube Testing'){​​​
steps{​​​
bat 'mvn sonar:sonar -Dsonar.sources=src/ -Dsonar.host.url=http://localhost:9000 -Dsonar.login=d6211fdca52322431d056a37812c3dded43a6b30'
}​​​
}​​​

stage('Deploy Application to Mulesoft Cloudhub'){​​​
steps{​​​
bat 'mvn package deploy -DmuleDeploy'
}​​​
}​​​

}​​​
}​​​
