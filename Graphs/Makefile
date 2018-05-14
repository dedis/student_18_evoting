SIZE=600
%.png: %.ppm
	mogrify -reverse -flatten $<
	mogrify -resize ${SIZE}x${SIZE} -format png $<
%.ppm: %.perf
	perl bargraph.pl -fig $< | fig2dev -L ppm -m 4 > $@
