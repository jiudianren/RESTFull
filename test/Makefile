# 声明一个变量 Source
#使用该变量时 用 $()  ${}来引用一个变量  如 ${SOURce}
#  $(wildcard *.cpp) 调用一个函数
#  wildcard 是函数名   *.cpp是参数  

SOURCE = $(wildcard *.cpp)
OBJS = $(patsubst %.cpp,%.o,$(SOURCE))

# 编译选项	
# CC Compiler Flags  
#export的变量，可以向下传递

RESTBED_HOME=/home/phub/gitPro/RESTFull/restbed
# export RESTBED_HOME=/home/phub/gitPro/RESTFull/restbed
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:${RESTBED_HOME}/library
INCLUDE = -I   ${RESTBED_HOME}/include
export CXXFLAGS=  -g -Wall -std=c++11    ${INCLUDE}
export SHARE   := -fPIC -shared -o


# 默认关闭
export GLINUX=ON
ifeq ($(GLINUX),  ON)
else
endif

TARGET  := Testjson

currentFile:$(OBJS)

# 编译规则		
all: 
	echo $(SOURCE)
	echo $(OBJS)
	currentFile


PHONY : clean install EHO
clean :
	-rm    *.o 


install:EHO
	$(CXX) ${CXXFLAGS}  ${INCLUDE}  ${LGTEST}  -lpthread   -lrestbed -o ${TARGET}  $(OBJS)   

EHO:
	@echo $(INCLUDES)
	@echo $(SOURCE)
	@echo $(OBJS)
	echo ${CXX}
	echo ${CXXFLAGS}
	echo ${ROOT_DIR}
	echo ${MAKE} 
	echo ${BUID_DIR}


