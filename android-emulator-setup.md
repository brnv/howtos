### Setting up Android emulator

1. Install System Image for your api version:

	* simple way to do this is to install packages from `android` gui

2. Check available android targets:

	```
	$ android list targets
	```

3. Create new avd:

	```
	$ android create avd -n <avd_name> -t <target_id> -p <avd_path>
	```

4. Check avd configuration file, which is located in:

	```
	<avd_path>/config.ini
	```

5. Finally, run the emulator:

	```
	$ emulator -avd <avd_name>
	```

### Some tips for emulator speeding up

1. Extra options for `android create avd` command:

	```
	--abi default/x86
	```

2. Extra options for `emulator` command:

	```
	-gpu on
	-scale 0.5 (from 0.1 to 3)
	-qemu -m 512 -enable-kvm
	```
