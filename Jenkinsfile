pipeline{

agent any

stages{

stage('Name of stage') {

steps{

git branch: "main", URL: 'https://github.com/erwansistandi/react_django_demo_app.git'

}

}

stage{

steps{

echo "Testing"

}

}

stage{

steps{

script{

sh "docker build - no-cache -t react_django_demo_app ."

}

}

}

stage{

steps{

script{

sh "docker run -p 8001:8001 -d react_django_demo_app"

}

}

}

}

}
