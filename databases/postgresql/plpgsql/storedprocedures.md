# postgresql

<sub>[:arrow_upper_left: PLPGSQL](../plpgsql.md)<sub>

## procedures

```sql
CREATE [ OR REPLACE ] FUNCTION
      name ( [ [ argmode ] [ argname ] argtype [ { DEFAULT | = } default_expr ] [, ...] ] )
      [ RETURNS rettype
        | RETURNS TABLE ( column_name column_type [, ...] ) ]
    { LANGUAGE lang_name
      | WINDOW
      | IMMUTABLE | STABLE | VOLATILE | [ NOT ] LEAKPROOF
      | CALLED ON NULL INPUT | RETURNS NULL ON NULL INPUT | STRICT
      | [ EXTERNAL ] SECURITY INVOKER | [ EXTERNAL ] SECURITY DEFINER
      | COST execution_cost
      | ROWS result_rows
      | SET configuration_parameter { TO value | = value | FROM CURRENT }
      | AS 'definition'
      | AS 'obj_file', 'link_symbol'
    } ...
      [ WITH ( attribute [, ...] ) ]
```

```sql
CREATE FUNCTION extended_sales(p_itemno int)
RETURNS TABLE(quantity int, total numeric) AS $
BEGIN
    RETURN QUERY SELECT s.quantity, s.quantity * s.price FROM sales AS s
                 WHERE s.itemno = p_itemno;
END;

$ LANGUAGE plpgsql;
```


- [postgresql](https://www.postgresql.org/docs/)
- [devmedia](https://www.devmedia.com.br/trabalhando-com-stored-procedures-no-postgresql/33354)