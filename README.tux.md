# Build Tuxedo image with kernel
```
sudo podman build --build-arg KERNEL_VERSION=6.6.9-200.fc39.x86_64 -t ub-custom-tuxedo -f Containerfile.tuxedo .
```

# Load kernel module from container
```
sudo podman run --rm --privileged localhost/ub-custom-tuxedo modprobe tuxedo_nb05_ec
```

# Available tuxedo modules
```
STEP 10/10: RUN tree | grep tux
|   |-- tuxedo-drivers.conffiles
|   `-- tuxedo-drivers.dkms
|   |-- tuxedo_compatibility_check
|   |   |-- tuxedo_compatibility_check.c
|   |   |-- tuxedo_compatibility_check.h
|   |   |-- tuxedo_compatibility_check.ko
|   |   |-- tuxedo_compatibility_check.mod
|   |   |-- tuxedo_compatibility_check.mod.c
|   |   |-- tuxedo_compatibility_check.mod.o
|   |   `-- tuxedo_compatibility_check.o
|   |-- tuxedo_io
|   |   |-- tuxedo_io.c
|   |   |-- tuxedo_io.ko
|   |   |-- tuxedo_io.mod
|   |   |-- tuxedo_io.mod.c
|   |   |-- tuxedo_io.mod.o
|   |   |-- tuxedo_io.o
|   |   `-- tuxedo_io_ioctl.h
|   |-- tuxedo_keyboard.c
|   |-- tuxedo_keyboard.ko
|   |-- tuxedo_keyboard.mod
|   |-- tuxedo_keyboard.mod.c
|   |-- tuxedo_keyboard.mod.o
|   |-- tuxedo_keyboard.o
|   |-- tuxedo_keyboard_common.h
|   |-- tuxedo_nb05
|   |   |-- tuxedo_nb05_ec.c
|   |   |-- tuxedo_nb05_ec.h
|   |   |-- tuxedo_nb05_ec.ko
|   |   |-- tuxedo_nb05_ec.mod
|   |   |-- tuxedo_nb05_ec.mod.c
|   |   |-- tuxedo_nb05_ec.mod.o
|   |   |-- tuxedo_nb05_ec.o
|   |   |-- tuxedo_nb05_keyboard.c
|   |   |-- tuxedo_nb05_keyboard.ko
|   |   |-- tuxedo_nb05_keyboard.mod
|   |   |-- tuxedo_nb05_keyboard.mod.c
|   |   |-- tuxedo_nb05_keyboard.mod.o
|   |   |-- tuxedo_nb05_keyboard.o
|   |   |-- tuxedo_nb05_power_profiles.c
|   |   |-- tuxedo_nb05_power_profiles.h
|   |   |-- tuxedo_nb05_power_profiles.ko
|   |   |-- tuxedo_nb05_power_profiles.mod
|   |   |-- tuxedo_nb05_power_profiles.mod.c
|   |   |-- tuxedo_nb05_power_profiles.mod.o
|   |   |-- tuxedo_nb05_power_profiles.o
|   |   |-- tuxedo_nb05_sensors.c
|   |   |-- tuxedo_nb05_sensors.ko
|   |   |-- tuxedo_nb05_sensors.mod
|   |   |-- tuxedo_nb05_sensors.mod.c
|   |   |-- tuxedo_nb05_sensors.mod.o
|   |   `-- tuxedo_nb05_sensors.o
|-- tuxedo-drivers.spec.in
`-- tuxedo_keyboard.conf
```