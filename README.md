## Testing a local RAG based on llama3.2 LLM

1 - Install docker
2 - Execute the ollama and postgree containers
3 - Inside the ollama container, download the llama3.2 model
4 - Install the plugins extensions necessary to store the embeddings in the postgre, it should have the following extensions:
postgres=# \dx
                                                    List of installed extensions
        Name         | Version |   Schema   |                                      Description                                      
---------------------+---------+------------+---------------------------------------------------------------------------------------
 ai                  | 0.3.0   | public     | helper functions for ai workflows
 plpgsql             | 1.0     | pg_catalog | PL/pgSQL procedural language
 plpython3u          | 1.0     | pg_catalog | PL/Python3U untrusted procedural language
 timescaledb         | 2.16.1  | public     | Enables scalable inserts and complex queries for time-series data (Community Edition)
 timescaledb_toolkit | 1.18.0  | public     | Library of analytical hyperfunctions, time-series pipelining, and other SQL utilities
 vector              | 0.7.4   | public     | vector data type and ivfflat and hnsw access methods

5 - Pay attenccion on the ollama ip adress as host is is bridge network ( default) and run the commands of the notebook.