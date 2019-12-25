Header-only C++ 17 log


	#include "nanolog.hpp"

	nanolog::initialize(nanolog::GuaranteedLogger(), "/tmp/", "nanolog", 1);
	LOG_INFO << "Sample NanoLog: " << 1 << 2.5 << 'c';



