# Liquibase Scylla

## Create keyspace
```
CREATE KEYSPACE IF NOT EXISTS test WITH replication = {
  'class': 'SimpleStrategy',
  'replication_factor': '3'
};
```

## Run
```
java -cp liquibase.jar:lib/picocli-4.6.1.jar liquibase.integration.commandline.LiquibaseCommandLine --changeLogFile=changelog.sql update
```

## Versions
### Java
```
java -version

openjdk version "11.0.2" 2019-01-15
OpenJDK Runtime Environment 18.9 (build 11.0.2+9)
OpenJDK 64-Bit Server VM 18.9 (build 11.0.2+9, mixed mode)
```

### Scylla
```
show version

[cqlsh 5.0.1 | Cassandra 3.0.8 | CQL spec 3.3.1 | Native protocol v4]
```