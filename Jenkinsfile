pipeline{

agent any

stages{

stage('git clone') {

steps{

git branch: "main", url: 'https://github.com/erwansistandi/react_django_demo_app.git'

}

}

stage ('testing'){

steps{

echo "Testing"

}

}

stage('build'){

steps{

script{

sh "docker build - no-cache -t react_django_demo_app ."

}

}

}

stage('docker run'){

steps{

script{

sh "docker run -p 8001:8001 -d react_django_demo_app"

}

}

}

}

}
