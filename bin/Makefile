CXX=g++
RM=rm -f

#ibm_model.a : ibm_model.o
#	   ar rcs $@ $<

ibm_model : main.o ibm_model.o utils.o
	g++ -o $@ $^

main.o : main.cc ibm_model.h
	g++ -c $<

utils.o : utils.cc utils.h
	g++ -c $<

ibm_model.o : ibm_model.cc ibm_model.h utils.h
	g++ -c $<


clean:
	$(RM) main.o ibm_model.o utils.o ibm_model
