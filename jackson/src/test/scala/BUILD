junit_tests(name='scala',
  dependencies=[
    'finatra/jackson/src/main/scala',
    'finatra/jackson/src/main/java',
    'finatra/jackson/src/test/scala:test-deps',
    'finatra/logback',
    'util/util-core'
  ],
  sources=rglobs(
    'com/twitter/finatra/tests/*.scala',
  ),
  resources=[
    'finatra/jackson/src/test/resources'
  ]
)

scala_library(name="test-deps",
  provides = scala_artifact(
    org = 'com.twitter.finatra',
    name = 'jackson-test-jar',
    repo = artifactory,
  ),
  dependencies=[
    '3rdparty/jvm/junit',
    '3rdparty/jvm/org/scalatest',
    'finatra/inject/inject-core:test-deps',
    'finatra/jackson/src/main/scala',
  ],
  sources=globs(
    'com/twitter/finatra/json/*.scala',
    'com/twitter/finatra/validation/*.scala',
  ),
  java_sources=[
    'finatra/jackson/src/test/java'
  ],
)
