node() {
    def myImg
    stage ("Build image") {
        // download the dockerfile to build from
        git 'http://localhost:3000/Vetch/DockerBaseTest.git'

        // build our docker image
        myImg = docker.build("my-image:dockerpyrdf","--build-arg --network='host'")
    }
}