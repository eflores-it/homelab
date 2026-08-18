# homelab
Hands-on IT homelab documenting virtualization, Linux, networking, and cloud infrastructure practice
# Ubuntu VM Lab

## Goal

Set up an Ubuntu Desktop virtual machine using VirtualBox to gain hands-on experience with virtualization, Linux, and basic IT troubleshooting.

## Environment

- Virtualization Software: VirtualBox
- Operating System: Ubuntu Desktop
- VM Name: ubuntu lab
- Memory: 2048 MB
- CPU: 1
- Virtual Disk: 25 GB
- ISO: Ubuntu Desktop AMD64

---

## Troubleshooting Log

### Issue 1 — Ubuntu VM Boot/Display Error

When I initially started the Ubuntu VM, I encountered a boot/display error that prevented Ubuntu from starting correctly.
<img width="949" height="704" alt="Screenshot 2026-08-17 191554" src="https://github.com/user-attachments/assets/b48bbd84-780b-4a83-b471-c1538a446aa9" />


#### Initial Configuration

The VirtualBox Graphics Controller was set to the default option:

- Graphics Controller: **VMSVGA**
- <img width="1073" height="626" alt="image" src="https://github.com/user-attachments/assets/a84dc0f5-d81d-4be1-816b-e3d8f6cb6120" />


With this configuration, the VM produced an error during startup and Ubuntu would not boot correctly.

#### Troubleshooting

I opened the VirtualBox settings for the Ubuntu VM and navigated to:

**Settings → Display → Graphics Controller**

I changed the Graphics Controller from:

**VMSVGA → VBoxSVGA**
<img width="949" height="564" alt="Screenshot 2026-08-18 115855" src="https://github.com/user-attachments/assets/f5fcd617-4877-4292-a770-72c2fb1e8d03" />


I then restarted the virtual machine and attempted to boot Ubuntu again.

#### Result
<img width="851" height="785" alt="Screenshot 2026-08-17 192703" src="https://github.com/user-attachments/assets/ed34577b-fe74-4efd-87c3-c55f484d88f4" />


**Resolved.**

After changing the Graphics Controller to **VBoxSVGA**, the Ubuntu VM successfully booted and I was able to proceed with the Ubuntu installation.
<img width="942" height="858" alt="Screenshot 2026-08-17 193011" src="https://github.com/user-attachments/assets/5a9dbb52-aaf6-407d-96e4-ddb6f910ad9e" />


#### What I Learned

- VirtualBox graphics controller settings can affect whether a guest operating system boots correctly.
- The default configuration does not always work correctly for every VM.
- Changing one configuration setting at a time makes it easier to identify what resolves a problem.
- I learned how to access and modify VirtualBox display and graphics configuration settings.
- I practiced verifying a configuration change by restarting the VM and testing the result.

---

### Issue 2 — Ubuntu Installer "Next" Button Unresponsive

After successfully resolving the VM boot issue, I proceeded with the Ubuntu installation.

During the installation process, the **Next** button became unresponsive and clicking it did not advance to the next installation step.

#### Troubleshooting Attempted

- Restarted the virtual machine.
- Tested the mouse inside the VM.
- Tested keyboard navigation.
- Checked VirtualBox display/input settings.
- Attempted to use the installer after restarting the VM.

#### Current Status

**Unresolved — troubleshooting paused.**

The VM successfully boots into the Ubuntu installer, but the installation cannot currently proceed because the **Next** button is not responding.

I will continue troubleshooting this issue in a future session.

---

## Skills Practiced

- Virtual machine creation
- VirtualBox configuration
- Ubuntu installation
- ISO image usage
- VM hardware configuration
- Display/graphics troubleshooting
- Input troubleshooting
- Problem isolation
- Testing configuration changes
- Technical documentation
- Troubleshooting documentation

## Key Takeaway

This lab demonstrated that troubleshooting is an iterative process. I encountered a VM boot/display error, investigated the VirtualBox graphics configuration, changed the Graphics Controller from **VMSVGA to VBoxSVGA**, and verified that the change resolved the problem.

The Ubuntu installation then presented a separate issue with the installer interface, which is being documented for continued troubleshooting.
