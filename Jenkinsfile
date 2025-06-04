pipeline{
agent any

tools{
maven 'Maven'
}

stages{
stage('Checkout'){
steps{
git branch:'master',url:'https://github.com/sowjanya2004/MyMavenPipeline.git'
}
}

stage('Build'){
steps{
sh 'mvn clean package'
}
}

stage('Tests'){
steps{
sh 'mvn test'
}
}

stage('Run Application'){
steps{
sh 'java -jar target/MyMavenPipeline-1.0-SNAPSHOT.jar'
}
}
}

post{
success{
echo 'build succesfull'

}
failure{
echo 'build failure'
}
}
}


