set(HEADERS Condition.h
            CriticalSection.h
            ThreadImpl.h
            ThreadLocal.h)
if(NOT CORE_SYSTEM_NAME STREQUAL windowsstore)
  set(SOURCES Win32Exception.cpp)
  set(HEADERS ${HEADERS} Win32Exception.h)
endif()


core_add_library(threads_win)
