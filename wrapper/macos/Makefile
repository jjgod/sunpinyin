all: debug

release: release-i386 release-ppc
	xcodebuild -project SunPinyin.xcodeproj -configuration Release build
	rm -f build/SunPinyin.app
	cd build ; ln -s Release/SunPinyin.app SunPinyin.app  
	
debug:
	xcodebuild -project SunPinyin.xcodeproj -configuration Debug build
	rm -f build/SunPinyin.app
	cd build ; ln -s Debug/SunPinyin.app SunPinyin.app

clean:
	rm -rf build

install:
	rm -rf "/Library/Input Methods/SunPinyin.app"
	cp -R build/Debug/SunPinyin.app "/Library/Input Methods"

