
Error from Isaac sim while loading Google 3D tiles:

2024-11-18 04:38:02 [66,276ms] [Warning] [gpu.foundation.plugin] Waiting on revision (10584) of Commandlist (Render graph command list (Render queue 0, device 0, frame submission index 1)) at cpu-revision (10584) that has not been submitted yet and is at gpu-revision (10583) can lead to deadlocks
2024-11-18 04:38:02 [66,276ms] [Warning] [omni.fabric.plugin] Warning: attribute normals not found for bucket id 11

2024-11-18 04:38:02 [66,277ms] [Warning] [omni.fabric.plugin] Warning: attribute normals not found for bucket id 11

2024-11-18 04:38:08 [72,146ms] [Warning] [gpu.foundation.plugin] Waiting on revision (10584) of Commandlist (Render graph command list (Render queue 0, device 0, frame submission index 1)) at cpu-revision (10584) that has not been submitted yet and is at gpu-revision (10583) can lead to deadlocks
2024-11-18 04:38:08 [72,149ms] [Warning] [gpu.foundation.plugin] Waiting on revision (10584) of Commandlist (Render graph command list (Render queue 0, device 0, frame submission index 1)) at cpu-revision (10584) that has not been submitted yet and is at gpu-revision (10583) can lead to deadlocks

Error from cmake while building:

[ 98%] Linking CXX shared module ../../lib/CesiumOmniverseCppTestsPythonBindings.cpython-310-x86_64-linux-gnu.so
lto-wrapper: warning: using serial compilation of 2 LTRANS jobs
lto-wrapper: note: see the ‘-flto’ option documentation for more information
/usr/bin/ld: ../../lib/libCesiumOmniverseCore.a(UsdTokens.cpp.o): in function `carb::detail::CachedInterface<omni::fabric::IToken, (char const*)0>::getInternal()':
UsdTokens.cpp:(.text._ZN4carb6detail15CachedInterfaceIN4omni6fabric6ITokenELPKc0EE11getInternalEv[_ZN4carb6detail15CachedInterfaceIN4omni6fabric6ITokenELPKc0EE11getInternalEv]+0x21b): undefined reference to `carb::thread::detail::ParkingLot::WaitBucket::bucket(void const*)::waitBuckets'
/usr/bin/ld: ../../lib/libCesiumOmniverseCore.a(UsdTokens.cpp.o): relocation R_X86_64_PC32 against undefined hidden symbol `_ZZN4carb6thread6detail10ParkingLot10WaitBucket6bucketEPKvE11waitBuckets' can not be used when making a shared object
/usr/bin/ld: final link failed: bad value
collect2: error: ld returned 1 exit status
gmake[2]: *** [tests/bindings/CMakeFiles/CesiumOmniverseCppTestsPythonBindings.dir/build.make:254: lib/CesiumOmniverseCppTestsPythonBindings.cpython-310-x86_64-linux-gnu.so] Error 1
gmake[1]: *** [CMakeFiles/Makefile2:678: tests/bindings/CMakeFiles/CesiumOmniverseCppTestsPythonBindings.dir/all] Error 2
gmake: *** [Makefile:166: all] Error 2
