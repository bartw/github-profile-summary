# github-profile-summary

## live at [https://github-profile-summary.com/](https://github-profile-summary.com/)

## screenshot
![github-profile-summary](https://user-images.githubusercontent.com/1521451/33906301-da659f12-df81-11e7-9fc4-1c47d62e2a95.PNG)

## run locally
* `git clone https://github.com/tipsy/github-profile-summary.git`
* `cd github-profile-summary`
* `mvn install`
* `java -jar target/github-profile-summary-1.0-jar-with-dependencies.jar`

If no api-token is set, you only get ~50 requests/hour  

To run the app with an api-token, first generate a token at 
[https://github.com/settings/tokens](https://github.com/settings/tokens), 
then launch the jar with the token:

* `java -Doauth-token=your-token -jar target/github-profile-summary-1.0-jar-with-dependencies.jar`

## run locally with docker

* `git clone https://github.com/tipsy/github-profile-summary.git`
* `cd github-profile-summary`
* `docker build -t github-profile-summary .`
* `docker run -it --rm --name github-profile-summary -p 7070:7070 github-profile-summary`
* OR with a token `docker run -it --rm --name github-profile-summary -p 7070:7070 -e "TOKEN=mytoken" github-profile-summary`
* browse to http://localhost:7070
