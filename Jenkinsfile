pipeline{
agent any
stages{
stage('Get it from GutHUB'){
	steps{
	echo "Get it from GutHUB"
	git credentialsId: '7ed02961-1449-499e-a32c-6d1ff69e3746', url: 'https://github.com/tilchev/JenkinsDemo.git'
	echo "Done"
	
	}
}
stage('Build'){
	steps{
	echo "Build it!"
	sh label: '', script: './Build.sh'
	echo "Done"
	}
}
stage('Deploy'){
	steps{
	echo "Deploy it!"
	sh label: '', script: './Deploy.sh'
	echo "Done"
	}
}
stage('Test'){
	steps{
	echo "Test it"
	sh label: '', script: './Test.sh'
	echo "Done"
	}
}
}
}
