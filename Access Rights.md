	(r) -> read(4)
	(w) -> write(2)
	(x) -> execute(1)

**For example -> "==-rwxr-x---=="**:
- "-" -> default file ("d" = folder)
- "rwx" -> owner (7)
- "r-x" -> group (5)
- "---" -> other rights (nothing) (0)