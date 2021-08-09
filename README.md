# exceltricks


### Return nothing if there's no result in VLOOKUP

`=IFERROR(VLOOKUP('TabName'!C2,'TabName'!A:B,2,FALSE),"")`



### Lookup a Value in Two Columns

=Index(array, Match(value_to_lookup, lookup_array, match_type))

`=INDEX('TabName'!$A$1:$B$1000, MATCH('TabName'!A2,'TabName'!$A$1:$B$1000,0))`



### Pull the Dignity or Anon gift ID from the JG file (help)

`=IF(ISNUMBER(SEARCH("Dignity",Modify!CM2)),CONCATENATE(Modify!CM2,Modify!BE2),IF(A2="21-1868",Modify!BE2,""))`
