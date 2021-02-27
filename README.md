# Origin

Copy from https://github.com/eclipse/leshan/tree/leshan-1.0.0/leshan-server-demo
to have a standalone maven project/module.

Also for the license, look in that repository.

This repository is only useful to see which steps are needed to set up a standalone leshan server.
For example if your curious how the pom of a standalone server looks like, if you have little maven experience.
See also https://github.com/eclipse/leshan/issues/844 for more context,
and also https://github.com/eclipse/leshan/issues/845 to remark that this repo has no added value (anymore) in comparison with the demo server maintained by eclipse.


# Usage

install maven
`mvn clean install`

compile server
`mvn package`
run server
`java -jar target/solid-leshan-1.0-SNAPSHOT.jar`

run client (zie ook leshan-client-demo)


bash command used to replace all package ...; in java files
`find . -name '*.java' -exec sed -i -e 's+package org.eclipse.leshan.server.demo\(.*\)+//package org.eclipse.leshan.server.demo\1\
package net.inrupt.iotsolidugent.leshan.server.solid\1+' {} \;`

bash command used to replace all import ....; in java files
`find . -name '*.java' -exec sed -i -e 's+\(import org.eclipse.leshan.server.demo\)\(.*\)+//\1\2\
import net.inrupt.iotsolidugent.leshan.server.solid\2+' {} \;`

