# exceltricks

  
### Lookup a Value in Two Columns

=Index(array, Match(value_to_lookup, lookup_array, match_type))

	=INDEX('TabName'!$A$1:$B$1000, MATCH('TabName'!A2,'TabName'!$A$1:$B$1000,0))

---

### Pull the Dignity or Anon gift ID from the JG file

Relies on the anon record ID - currently 21-1868. Replace as needed.

	=IF(ISNUMBER(SEARCH("Dignity",Modify!CM2)),CONCATENATE(Modify!CM2,Modify!BE2),IF(A2="21-1868",Modify!BE2,""))

---

### Strip non-printing characters from Kiltwalk address lines, and replace with semicolons

	=SUBSTITUTE(SUBSTITUTE(G2,CHAR(10),""),CHAR(13),";")

---

### Trim and strip whitespace, includes nonbreaking space characters

	=TRIM(SUBSTITUTE(A1, CHAR(160), " "))

---

### UK Postcode formatting (use the above trim formula first!)

	=CONCATENATE(LEFT(A1,LEN(A1)-3)," ",RIGHT(A1,3))

---

### Extract text between two characters in a cell

	=REGEXEXTRACT(A1,"vip\.ce\.(.*)\.http")

---

### Strip non-numeric characters (input with CTRL+SHIFT+ENTER)

	=MID(A1,MIN(IF(ISNUMBER((--MID(A1,ROW(INDIRECT("1:"&LEN(A1))),1))),(ROW(INDIRECT("1:"&LEN(A1)))),"")),MAX(IF(ISNUMBER((--MID(A1,ROW(INDIRECT("1:"&LEN(A1))),1))),(ROW(INDIRECT("1:"&LEN(A1)))),""))-MIN(IF(ISNUMBER((--MID(A1,ROW(INDIRECT("1:"&LEN(A1))),1))),(ROW(INDIRECT("1:"&LEN(A1)))),""))+1)


