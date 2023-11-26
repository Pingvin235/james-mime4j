Instruction for building a BGERP version of the library 'x.y.z'
---------------------------------------------------------------

## In .git/config change origin repo
[remote "origin"]
#	url = https://github.com/apache/james-mime4j.git
	url = https://github.com/Pingvin235/james-mime4j.git

## Execute
git checkout master && git pull --rebase

## Switch the origin repo back
[remote "origin"]
	url = https://github.com/apache/james-mime4j.git
#	url = https://github.com/Pingvin235/james-mime4j.git

## Execute
git push && git checkout bgerp

## Replace in all pom.xml files version to
x.y.z.bgerp

## Execute
mvn clean
mvn package install -DskipTests

## Check the new libraries with locally running BGERP

## Publish the built libraries
repo.bgerp.org

