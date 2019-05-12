pipeline{
agent any
stages{
stage('scm checkout'){
steps{
git 'https://github.com/KirtiVyas/jenkins-example.git'
}
}
stage('packaging with sonar'){
steps{
withSonarQubeEnv('sonar'){
sh 'mvn sonar:sonar clean package'
}
}
}
}
}
