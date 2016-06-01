GET_FILENAME_COMPONENT(OBJNAME ${CMAKE_CURRENT_LIST_DIR} NAME)
INCLUDE_DIRECTORIES(include)
AUX_SOURCE_DIRECTORY(src OBJECT_SRC)
ADD_LIBRARY(${OBJNAME} OBJECT ${OBJECT_SRC})

SOURCE_GROUP(FileIO .*File.*cc)
SOURCE_GROUP(TCPIP .*Transport.*cc)
SOURCE_GROUP(TCPIP FILES src/Serializable.cc src/Producer.cc src/CommandReceiver.cc src/DataCollector.cc src/DataSender.cc  src/LogCollector.cc)
SOURCE_GROUP(Event .*Event.*cc)
SOURCE_GROUP(Utilities FILES src/Utils.cc src/Time.cc src/Mutex.cc src/EudaqThread.cc)