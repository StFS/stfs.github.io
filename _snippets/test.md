---
layout: minimal
---

{% highlight text linenos hl_lines=7 %}

[INFO] Scanning for projects...
[INFO] Inspecting build with total of 1 modules...
[INFO] Installing Nexus Staging features:
[INFO]   ... total of 1 executions of maven-deploy-plugin replaced with nexus-staging-maven-plugin
[INFO] ------------------------------------------------------------------------
[INFO] Detecting the operating system and CPU architecture
[INFO] ------------------------------------------------------------------------
[INFO] os.detected.name: osx
[INFO] os.detected.arch: x86_64
[INFO] os.detected.bitness: 64
[INFO] os.detected.version: 14.4
[INFO] os.detected.version.major: 14
[INFO] os.detected.version.minor: 4
[INFO] os.detected.classifier: osx-x86_64
[INFO] 
[INFO] --------------------< org.eclipse.hono:hono-tests >---------------------
[INFO] Building Hono Integration Tests 2.6.0-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- maven-enforcer-plugin:3.3.0:enforce (enforce-no-snapshots) @ hono-tests ---
[INFO] Skipping Rule Enforcement.
[INFO] 
[INFO] --- maven-enforcer-plugin:3.3.0:enforce (enforce-java-17) @ hono-tests ---
[INFO] Rule 0: org.apache.maven.enforcer.rules.version.RequireJavaVersion passed
[INFO] 
[INFO] --- maven-checkstyle-plugin:3.3.0:check (checkstyle-check) @ hono-tests ---
[INFO] You have 0 Checkstyle violations.
[INFO] 
[INFO] --- properties-maven-plugin:1.2.0:read-project-properties (default) @ hono-tests ---
[INFO] Quiet processing - ignoring properties cannot be loaded from File: /Users/stefan.freyr/work/contrib/controlant-eclipse/eclipse-hono/tests/target/docker/qpid.port.properties
[INFO] Quiet processing - ignoring properties cannot be loaded from File: /Users/stefan.freyr/work/contrib/controlant-eclipse/eclipse-hono/tests/target/docker/adapter.http.port.properties
[INFO] Quiet processing - ignoring properties cannot be loaded from File: /Users/stefan.freyr/work/contrib/controlant-eclipse/eclipse-hono/tests/target/docker/adapter.lora.port.properties
[INFO] Quiet processing - ignoring properties cannot be loaded from File: /Users/stefan.freyr/work/contrib/controlant-eclipse/eclipse-hono/tests/target/docker/adapter.amqp.port.properties
[INFO] Quiet processing - ignoring properties cannot be loaded from File: /Users/stefan.freyr/work/contrib/controlant-eclipse/eclipse-hono/tests/target/docker/adapter.coap.port.properties
[INFO] 
[INFO] --- maven-resources-plugin:3.3.1:resources (default-resources) @ hono-tests ---
[INFO] Copying 67 resources from src/test/resources to target/resources
[INFO] The encoding used to copy filtered properties files have not been set. This means that the same encoding will be used to copy filtered properties files as when copying other filtered resources. This might not be what you want! Run your build with --debug to see which files might be affected. Read more at https://maven.apache.org/plugins/maven-resources-plugin/examples/filtering-properties-files.html
[INFO] 
[INFO] --- maven-compiler-plugin:3.11.0:compile (default-compile) @ hono-tests ---
[INFO] No sources to compile
[INFO] 
[INFO] --- maven-dependency-plugin:3.5.0:unpack-dependencies (copy_demo_certs) @ hono-tests ---
[INFO] org.eclipse.hono:hono-demo-certs:jar:2.6.0-SNAPSHOT already exists in destination.
[INFO] 
[INFO] --- maven-resources-plugin:3.3.1:testResources (default-testResources) @ hono-tests ---
[INFO] Copying 67 resources from src/test/resources to target/test-classes
[INFO] 
[INFO] --- maven-compiler-plugin:3.11.0:testCompile (default-testCompile) @ hono-tests ---
[INFO] Nothing to compile - all classes are up to date
[INFO] 
[INFO] --- maven-surefire-plugin:3.1.0:test (default-test) @ hono-tests ---
[INFO] Tests are skipped.
[INFO] 
[INFO] --- maven-dependency-plugin:3.5.0:unpack-dependencies (copy_legal_docs) @ hono-tests ---
[INFO] 
[INFO] --- maven-jar-plugin:3.3.0:jar (default-jar) @ hono-tests ---
[INFO] Skipping packaging of the jar
[INFO] 
[INFO] --- maven-failsafe-plugin:3.1.0:integration-test (default) @ hono-tests ---
[INFO] Using auto detected provider org.apache.maven.surefire.junitplatform.JUnitPlatformProvider
[INFO] 
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------
[INFO] Running org.eclipse.hono.tests.mqtt.CommandAndControlMqttIT
17:02:14.427 [main] INFO  o.e.h.tests.IntegrationTestSupport - vert.x uses legacy Base64 encoder
17:02:14.649 [main] WARN  i.n.r.d.DnsServerAddressStreamProviders - Can not find io.netty.resolver.dns.macos.MacOSDnsServerAddressStreamProvider in the classpath, fallback to system defaults. This may result in incorrect DNS resolutions on MacOS. Check whether you have a dependency on 'io.netty:netty-resolver-dns-native-macos'
17:02:14.675 [main] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - running testSendOneWayCommandSucceeds(MqttCommandEndpointConfiguration, VertxTestContext) [1]; parameters: subscribe as: DEVICE, southbound endpoint: command, northbound endpoint: command, topic filter: command///req/#
17:02:14.676 [main] INFO  o.e.h.tests.IntegrationTestSupport - Kafka Consumers are configured to connect to broker(s) at localhost:53312
17:02:14.744 [main] INFO  o.e.h.tests.IntegrationTestSupport - Kafka Producers are configured to connect to broker(s) at localhost:53312
17:02:15.337 [main] INFO  o.e.h.s.m.c.PasswordCredential - using regular expression for validating authentication identifiers: ^[a-zA-Z0-9-_=\.]+$
17:02:15.445 [main] INFO  o.e.h.s.a.SpringBasedHonoPasswordEncoder - using BCrypt [strength: 4] with PRNG [NativePRNGNonBlocking] for encoding clear text passwords
17:02:16.051 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - MQTTS connection to adapter [host: localhost, port: 53368] established
17:02:16.113 [vert.x-eventloop-thread-1] INFO  o.e.h.c.k.consumer.HonoKafkaConsumer - subscription topic doesn't exist as of now: hono.event.74a0f76b-0867-4d78-9934-337364db51b0 [client-id: event-4448ff58-fc5d-4093-974d-847f9e37bdb1]
17:02:16.120 [vert.x-kafka-consumer-thread-0] WARN  o.apache.kafka.clients.NetworkClient - [Consumer clientId=event-4448ff58-fc5d-4093-974d-847f9e37bdb1, groupId=its-48defeb7-0311-452b-9473-f5362ac78fab] Error while fetching metadata with correlation id 5 : {hono.event.74a0f76b-0867-4d78-9934-337364db51b0=UNKNOWN_TOPIC_OR_PARTITION}
17:02:16.283 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - received notification [TimeUntilDisconnectNotification [tenant-id: 74a0f76b-0867-4d78-9934-337364db51b0, device-id: dfd1e379-dd6d-4089-aa82-9ac135d7c48c, ttd: -1, readyUntil: +1000000000-12-31T23:59:59.999999999Z, creationTime: 2024-04-04T17:02:16.250Z]]
17:02:16.361 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands succeeded: 20
17:02:16.361 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands sent: 20
17:02:16.396 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands succeeded: 40
17:02:16.396 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands sent: 40
17:02:16.433 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands succeeded: 60
17:02:16.433 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands sent: 60
17:02:16.433 [main] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands sent: 60, commands succeeded: 60 after 148 milliseconds
17:02:17.341 [vert.x-eventloop-thread-1] INFO  o.e.h.c.k.consumer.HonoKafkaConsumer - Kafka consumer stopped successfully
17:02:17.341 [vert.x-eventloop-thread-1] INFO  o.e.h.tests.IntegrationTestSupport - connection to messaging infrastructure closed
17:02:17.351 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - connection to MQTT adapter closed
17:02:17.439 [main] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - running testSendOneWayCommandSucceeds(MqttCommandEndpointConfiguration, VertxTestContext) [2]; parameters: subscribe as: GATEWAY_FOR_ALL_DEVICES, southbound endpoint: command, northbound endpoint: command, topic filter: command//+/req/#
17:02:17.439 [main] INFO  o.e.h.tests.IntegrationTestSupport - Kafka Consumers are configured to connect to broker(s) at localhost:53312
17:02:17.440 [main] INFO  o.e.h.tests.IntegrationTestSupport - Kafka Producers are configured to connect to broker(s) at localhost:53312
17:02:17.468 [main] INFO  o.e.h.s.a.SpringBasedHonoPasswordEncoder - using BCrypt [strength: 4] with PRNG [NativePRNGNonBlocking] for encoding clear text passwords
17:02:17.537 [main] INFO  o.e.h.s.a.SpringBasedHonoPasswordEncoder - using BCrypt [strength: 4] with PRNG [NativePRNGNonBlocking] for encoding clear text passwords
17:02:17.653 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - MQTTS connection to adapter [host: localhost, port: 53368] established
17:02:17.663 [vert.x-eventloop-thread-1] INFO  o.e.h.c.k.consumer.HonoKafkaConsumer - subscription topic doesn't exist as of now: hono.event.e4811499-5812-4ac0-b625-2c03a85cfc11 [client-id: event-a2fda093-97b6-416c-b2f2-d5de208fbcad]
17:02:17.667 [vert.x-kafka-consumer-thread-1] WARN  o.apache.kafka.clients.NetworkClient - [Consumer clientId=event-a2fda093-97b6-416c-b2f2-d5de208fbcad, groupId=its-dcb83f47-4a24-47d2-a16b-ee4cfae0a367] Error while fetching metadata with correlation id 5 : {hono.event.e4811499-5812-4ac0-b625-2c03a85cfc11=UNKNOWN_TOPIC_OR_PARTITION}
17:02:18.276 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - received notification [TimeUntilDisconnectNotification [tenant-id: e4811499-5812-4ac0-b625-2c03a85cfc11, device-id: 13994a13-2b34-428b-a1e3-839d70146097, ttd: -1, readyUntil: +1000000000-12-31T23:59:59.999999999Z, creationTime: 2024-04-04T17:02:18.269Z]]
17:02:18.325 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands succeeded: 20
17:02:18.326 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands sent: 20
17:02:18.361 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands succeeded: 40
17:02:18.361 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands sent: 40
17:02:18.393 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands succeeded: 60
17:02:18.393 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands sent: 60
17:02:18.393 [main] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands sent: 60, commands succeeded: 60 after 117 milliseconds
17:02:19.361 [vert.x-eventloop-thread-1] INFO  o.e.h.c.k.consumer.HonoKafkaConsumer - Kafka consumer stopped successfully
17:02:19.361 [vert.x-eventloop-thread-1] INFO  o.e.h.tests.IntegrationTestSupport - connection to messaging infrastructure closed
17:02:19.362 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - connection to MQTT adapter closed
17:02:19.449 [main] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - running testSendOneWayCommandSucceeds(MqttCommandEndpointConfiguration, VertxTestContext) [3]; parameters: subscribe as: GATEWAY_FOR_SINGLE_DEVICE, southbound endpoint: command, northbound endpoint: command, topic filter: command//${deviceId}/req/#
17:02:19.449 [main] INFO  o.e.h.tests.IntegrationTestSupport - Kafka Consumers are configured to connect to broker(s) at localhost:53312
17:02:19.449 [main] INFO  o.e.h.tests.IntegrationTestSupport - Kafka Producers are configured to connect to broker(s) at localhost:53312
17:02:19.475 [main] INFO  o.e.h.s.a.SpringBasedHonoPasswordEncoder - using BCrypt [strength: 4] with PRNG [NativePRNGNonBlocking] for encoding clear text passwords
17:02:19.538 [main] INFO  o.e.h.s.a.SpringBasedHonoPasswordEncoder - using BCrypt [strength: 4] with PRNG [NativePRNGNonBlocking] for encoding clear text passwords
17:02:19.659 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - MQTTS connection to adapter [host: localhost, port: 53368] established
17:02:19.667 [vert.x-eventloop-thread-1] INFO  o.e.h.c.k.consumer.HonoKafkaConsumer - subscription topic doesn't exist as of now: hono.event.ef3ae237-729d-4761-aa7c-e762ec68bf09 [client-id: event-75865786-e530-43f0-aff8-100af7b01e59]
17:02:19.670 [vert.x-kafka-consumer-thread-2] WARN  o.apache.kafka.clients.NetworkClient - [Consumer clientId=event-75865786-e530-43f0-aff8-100af7b01e59, groupId=its-c18424ed-4c5d-4e06-9f07-7070e8bbd316] Error while fetching metadata with correlation id 5 : {hono.event.ef3ae237-729d-4761-aa7c-e762ec68bf09=UNKNOWN_TOPIC_OR_PARTITION}
17:02:20.296 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - received notification [TimeUntilDisconnectNotification [tenant-id: ef3ae237-729d-4761-aa7c-e762ec68bf09, device-id: a9385b01-26e6-4b57-b8ba-fbc09696e66c, ttd: -1, readyUntil: +1000000000-12-31T23:59:59.999999999Z, creationTime: 2024-04-04T17:02:20.290Z]]
17:02:20.348 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands succeeded: 20
17:02:20.348 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands sent: 20
17:02:20.382 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands succeeded: 40
17:02:20.382 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands sent: 40
17:02:20.417 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands succeeded: 60
17:02:20.417 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands sent: 60
17:02:20.418 [main] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - commands sent: 60, commands succeeded: 60 after 120 milliseconds
17:02:21.378 [vert.x-eventloop-thread-1] INFO  o.e.h.c.k.consumer.HonoKafkaConsumer - Kafka consumer stopped successfully
17:02:21.378 [vert.x-eventloop-thread-1] INFO  o.e.h.tests.IntegrationTestSupport - connection to messaging infrastructure closed
17:02:21.380 [vert.x-eventloop-thread-1] INFO  o.e.h.t.mqtt.CommandAndControlMqttIT - connection to MQTT adapter closed
[INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 7.108 s - in org.eclipse.hono.tests.mqtt.CommandAndControlMqttIT
[INFO] 
[INFO] Results:
[INFO] 
[INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0
[INFO] 
[INFO] 
[INFO] --- write-properties-file-maven-plugin:1.0.1:write-properties-file (default) @ hono-tests ---
[INFO] Saving properties to file /Users/stefan.freyr/work/contrib/controlant-eclipse/eclipse-hono/tests/target/docker/kafka.port.properties
[INFO] 
[INFO] --- maven-source-plugin:3.2.1:jar-no-fork (attach-sources) @ hono-tests ---
[INFO] Skipping source per configuration.
[INFO] 
[INFO] --- maven-failsafe-plugin:3.1.0:verify (default) @ hono-tests ---
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  38.212 s
[INFO] Finished at: 2024-04-04T17:02:23Z
[INFO] ------------------------------------------------------------------------


{% endhighlight %}
