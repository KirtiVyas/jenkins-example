pipeline{
agent any
stages{
stage('scm checkout'){
steps{
git 'https://github.com/mg2412/maven-project.git'
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
