node() {
    def myImg
    stage ("Get image") {
        git 'http://localhost:3000/Vetch/DockerBaseTest.git'
    }
    stage("Build image"){
        myImg = docker.build("dockerpyrdf .","--network='host'")
    }
    stage("Run image"){
        docker.run("dockerpyrdf")
    }
}