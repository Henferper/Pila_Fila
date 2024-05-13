mermaid
classDiagram
    class Zeppelin {
        Porta: 8080
    }
    class HiveServer {
        Porta: 10000
        Porta: 10002
    }
    class Metastore {   
        Porta: 9083
    }
    class LivySpark {
        Porta: 8998
        Porta: 18080
        
    }
    class PostgreSQL {
        Porta: 5432
    }
    class MinIO {
        Porta: 9000
        Porta: 9001
    }

    Zeppelin <--> LivySpark
    LivySpark <--> Metastore: 
    LivySpark <--> MinIO: 
    MinIO <--> HiveServer: 
    Metastore <--> PostgreSQL: 
    Metastore <--> HiveServer: 
