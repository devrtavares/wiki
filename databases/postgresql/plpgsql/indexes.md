
<sub>[:arrow_upper_left: PLPGSQL](../plpgsql.md)<sub>

```sql
CREATE [ UNIQUE ] INDEX [ CONCURRENTLY ] [ name ] ON table [ USING method ]
    ( { column | ( expression ) } [ COLLATE collation ] [ opclass ] [ ASC | DESC ] [ NULLS { FIRST | LAST } ] [, ...] )
    [ WITH ( storage_parameter = value [, ... ] ) ]
    [ TABLESPACE tablespace ]
    [ WHERE predicate ]

CREATE UNIQUE INDEX title_idx ON films (title);

CREATE INDEX ON films ((lower(title)));

CREATE INDEX title_idx_german ON films (title COLLATE "de_DE");

CREATE INDEX title_idx_nulls_low ON films (title NULLS FIRST);

CREATE UNIQUE INDEX title_idx ON films (title) WITH (fillfactor = 70);

CREATE INDEX gin_idx ON documents_table USING gin (locations) WITH (fastupdate = off);

CREATE INDEX code_idx ON films (code) TABLESPACE indexspace;

CREATE INDEX pointloc
    ON points USING gist (box(location,location));
SELECT * FROM points
    WHERE box(location,location) && '(0,0),(1,1)'::box;

CREATE INDEX CONCURRENTLY sales_quantity_index ON sales_table (quantity);
```