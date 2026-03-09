UNF
===

Universal Numerical Fingerprint


The Universal Numerical Fingerprint (UNF) is a cryptographic signature of the approximated semantic content of a digital object.
It is computed on the normalized (or canonicalized) forms of the data values, and is thus independent of the storage 
medium and format of the data. 

CLI Usage
---------

This package now includes a CLI entrypoint that reads supported input files and emits JSON aligned with `unf6_schema.json`.

Build:

```bash
mvn -q -DskipUT=true package
```

Run (single line-based string file):

```bash
java -cp target/unf-6.0.2-SNAPSHOT.jar org.dataverse.unf.UnfCli \
	--input /path/to/values.txt \
	--type string
```

Run (CSV with explicit column types):

```bash
java -cp target/unf-6.0.2-SNAPSHOT.jar org.dataverse.unf.UnfCli \
	--input /path/to/data.csv \
	--column-types double,int
```

Run (dataset-level report from a directory of files):

```bash
java -cp target/unf-6.0.2-SNAPSHOT.jar org.dataverse.unf.UnfCli \
	--input /path/to/dataset-dir
```

For full options:

```bash
java -cp target/unf-6.0.2-SNAPSHOT.jar org.dataverse.unf.UnfCli --help
```

License
-------

See [LICENSE](LICENSE) 
