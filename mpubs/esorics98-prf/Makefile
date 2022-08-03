#
# Author Simon Foley s.foley@cs.ucc.ie
# Time-stamp: <98/05/15 15:18:34 snf22>
#
# Makefile for paper "A Kernelized Architecture for Multilevel Secure
# Application Policies", European Symposium on Research in Computer
# Security, Louvain-la-Neuve, Belgium, September 1998, Springer LNCS.
#
# See 00Readme for more details. 
#
# 

ZEVES=/home/snf22/sw/eves/system/zeves

pct: REFINE.pct
sct: REFINE.sct 

REFINE.pct: REFINE.sct REFINE.prf SKPI.pct SKPIO.pct
	echo "read script \"REFINE.prf\"; \
              quit;" | $(ZEVES)

SKPIO.pct: SKPIO.sct SKPIO.prf SCUP.pct OBJECT.pct
	echo "read script \"SKPIO.prf\"; \
              quit;" | $(ZEVES)

SKPI.pct: SKPI.sct SKPI.prf SCUP.pct OBJECT.pct
	echo "read script \"SKPI.prf\"; \
              quit;" | $(ZEVES)

SCUP.pct: SCUP.sct SCUP.prf
	echo "read script \"SCUP.prf\"; \
              quit;" | $(ZEVES)

OBJECT.pct: OBJECT.sct OBJECT.prf
	echo "read script \"OBJECT.prf\"; \
              quit;" | $(ZEVES)

REFINE.sct: REFINE.tex SKPI.sct SKPIO.sct
	echo "check \"REFINE.tex\"; quit;" | $(ZEVES)

SKPI.sct: SKPI.tex SCUP.sct OBJECT.sct
	echo "check \"SKPI.tex\"; quit;" | $(ZEVES)

SKPIO.sct: SKPIO.tex SCUP.sct OBJECT.sct
	echo "check \"SKPIO.tex\"; quit;" | $(ZEVES)

OBJECT.sct: OBJECT.tex
	echo "check \"OBJECT.tex\"; quit;" | $(ZEVES)

SCUP.sct: SCUP.tex 
	echo "check \"SCUP.tex\"; quit;" | $(ZEVES)
