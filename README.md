
### Pipelines that iterate through subsets

Download/create a set of files associated with each subset

> Example: https://github.com/jsta/gssurgo_data/blob/master/Makefile

Create a file holding a list of subset ids

> Example: https://github.com/jsta/nesR/blob/master/477/Makefile

Brute force write out a list of files for each subset

> Example: https://github.com/jsta/realsat-r/blob/master/Makefile

----

### Self-documenting Makefiles

```makefile
help:
	@grep -E '^[a-zA-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | sort | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[36m%-30s\033[0m %s\n", $$1, $$2}'
```

> See: https://marmelab.com/blog/2016/02/29/auto-documented-makefile.html

----

### Cheatsheet

https://jsta.github.io/ProgrammingNotes/make.html
