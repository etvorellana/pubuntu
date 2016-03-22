# Parallella Image scripts

## TODO

- TEST
- ??? Add bitstream scripts to flow

## Flow

- Build bitstreams and place in fpga_bitfiles/  

### Optional

```sh
export PARALLELLA_LINUX=/path/to/parallella-linux
```

### Now do

```sh
./bootfs-and-kernel.sh
./rootfs.sh
./image.sh out/parallella_e16_headless_gpiose_7010_bootfs.tar.gz parallella_e16_headless_gpiose_7010.img
./image.sh out/parallella_e16_headless_gpiose_7020_bootfs.tar.gz parallella_e16_headless_gpiose_7020.img
```

---

## Building coprthr

```
git clone https://github.com/parallella/coprthr --branch esdk-2016.3
cd coprthr
./configure --enable-epiphany
make
sudo make install
```

### Copy these files/directories to overlay

- /etc/ocl.conf
- /etc/OpenCL/
- /var/clproc (permission 1777)
- /usr/local/browndeer


