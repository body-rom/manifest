# BodyOS Build Instructions

---

## Initialize the Local Repository

```bash
repo init -u https://github.com/body-rom/manifest.git -b 16-qpr2 --git-lfs
```

---

## Sync the Source

```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

---

## Set Up the Environment

```bash
source build/envsetup.sh
```

---

## Choose a Target Device

```bash
lunch aosp_<device>-bp4a-userdebug
```
> Replace `<device>` with your actual device codename.

---

## Build the Code

```bash
mka bacon -j$(nproc --all) | tee log.txt
```

The build output will be saved to `log.txt` for review.

---
## Credit
userariii
