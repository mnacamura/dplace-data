
NM='nexus_treemanip.py'

all: summary.trees posterior.trees

summary.trees: original/a400-m1pcv-time.mcct.trees.gz
	gunzip -c $< > tmp
	$(NM) -c -t tmp $@
	rm tmp

posterior.trees: original/a400-m1pcv-time.trees.gz
	# remove 1000 (10%), sample 1000
	$(NM) -c -d 1-1000 $< tmp
	$(NM) -n 1000 tmp $@
	rm tmp
