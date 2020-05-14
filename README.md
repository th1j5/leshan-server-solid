# Origin

Copy from https://github.com/eclipse/leshan/tree/leshan-1.0.0/leshan-server-demo
to have a standalone maven project/module.


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

