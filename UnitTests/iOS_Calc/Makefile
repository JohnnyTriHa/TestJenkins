
default :
	xcodebuild -target "iOS_Calc_ApplicationTests (Device)" -configuration Release
	xcodebuild -target "iOS_Calc_ApplicationTests (Simulator)" -configuration Release
	BUILD_DIR="build" BUILD_STYLE="Release" sh ../Scripts/CombineLibs.sh
	sh ../Scripts/iPhoneFramework.sh

# If you need to clean a specific target/configuration: $(COMMAND) -target $(TARGET) -configuration DebugOrRelease -sdk $(SDK) clean
clean: 
	-rm -rf build/*
test:
	GHUNIT_CLI=1 xcodebuild -target Test -configuration Debug -sdk iphonesimulator5.0 build


