# sky local manifests

Redmi 12 5G (codename `sky`, board `ravelin`, SoC SM4450) for LineageOS 24.0.

## Sync

```sh
repo init -u https://github.com/LineageOS/android.git -b lineage-24.0
mkdir -p .repo/local_manifests
curl -L -o .repo/local_manifests/sky.xml \
  https://raw.githubusercontent.com/sm4450-river-tibet-project/local_manifests/main/sky.xml
repo sync -c -j8 --force-sync --no-clone-bundle --no-tags
```

## Build

```sh
source build/envsetup.sh
breakfast sky
brunch sky
```

## Repos

| repo | path | branch |
|---|---|---|
| device_xiaomi_sky | device/xiaomi/sky | lineage-24.0 |
| device_xiaomi_sm4450-common | device/xiaomi/sm4450-common | lineage-24.0 |
| kernel_xiaomi_sky-6.12 | kernel/xiaomi/sky | 6.12 |
| kernel_xiaomi_sky-devicetrees-6.12 | kernel/xiaomi/sky-devicetrees | 6.12 |
| kernel_xiaomi_sky-modules | kernel/xiaomi/sky-modules | 6.12 |
