NVIDIA Vulkan Beta drivers for Gentoo
=====================================

Please read https://developer.nvidia.com/vulkan-driver first.

To use this overlay, run

```bash
emerge -n app-eselect/eselect-repository dev-vcs/git
eselect repository add nvidia-vulkan git https://github.com/kakra/nvidia-vulkan.git
emaint sync -r nvidia-vulkan
```

Please ensure that the repository stays in sync. You may use these commands:

```
emaint sync -r nvidia-vulkan # just this repository
# OR
emaint sync -A               # all repositories
# OR
emaint sync -a               # all auto-sync repositories
```

To sync automatically with your usual portage sync, ensure auto-sync is enabled for
this repository. Auto-sync defaults to true, if in doubt, check `man portage`.

After the repository is synced, unmask/mask as appropriate.

These drivers are checked with the Vulkan GPUinfo diagnostic software. You can see my
submitted entries here:

https://vulkan.gpuinfo.org/listreports.php?submitter=hurikhan77
