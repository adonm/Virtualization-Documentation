---
title: Virtual Machine (VM) Saved State Dump Provider API
description: The saved state format of a VM can be accessed via VmSavedStateDumpProvider DLL, which abstracts away the format to provide an API to extract dump-related content. The DLL exports a set of C-style Windows API functions.
ms.date: 04/19/2022
author: sethmanheim
ms.author: roharwoo

---

# Virtual Machine (VM) Saved State Dump Provider API


**Note: These APIs are not yet publicly available and will be available in the latest release of the Windows SDK.**

The saved state format of a VM can be accessed via VmSavedStateDumpProvider DLL, which abstracts away the format to provide an API to extract dump-related content. The DLL exports a set of C-style Windows API functions.
 
## API Methods

The VM Saved State Dump Provider DLL offers APIs that fall into two categories: 
1. I/O of the saved state files
2. Operations on the resulting handle generated by I/O on the saved state files.

|Methods   |Description|
| --- | --- |
|[ApplyPendingSavedStateFileReplayLog](./reference/ApplyPendingSavedStateFileReplayLog.md)|Opens the saved state file in read-write exclusive mode so that it applies any pending replay logs to the contents|
|[GetArchitecture](./reference/GetArchitecture.md)|Queries the saved state for the current achitecture the virtual processor was running|
|[GetGuestPhysicalMemoryChunks](./reference/GetGuestPhysicalMemoryChunks.md)|Returns the layout of the physical memory of the guest|
|[GetGuestRawSavedMemorySize](./reference/GetGuestRawSavedMemorySize.md)|Queries for the current paging mode in use by the virtual processor|
|[GetPagingMode](./reference/GetPagingMode.md)|Queries for the current paging mode in use by the virtual processor|
|[GetRegisterValue](./reference/GetRegisterValue.md)|Queries for a specific vergister value for a given virtual processor|
|[GetVpCount](./reference/GetVpCount.md)|Queries for the virtual processor count from the dump file|
|[GuestPhysicalAddressToRawSavedMemoryOffset](./reference/GuestPhysicalAddressToRawSavedMemoryOffset.md)|Translates the given guest physical address to a raw saved memory offset|
|[GuestVirtualAddressToPhysicalAddress](./reference/GuestVirtualAddressToPhysicalAddress.md)|Translates a virtual address to the associated physical address|
|[LoadSavedStateFile](./reference/LoadSavedStateFile.md)|Loads the saved state file and creates an instance of VmSavedStateDump|
|[LoadSavedStateFiles](./reference/LoadSavedStateFiles.md)|Loads the saved state files and creates an instance of VmSavedStateDump|
|[LocateSavedStateFiles](./reference/LocateSavedStateFiles.md)|Locate the saved state files for a given VM or snapshot|
|[ReadGuestPhysicalAddress](./reference/ReadGuestPhysicalAddress.md)|Reads from the saved state file the given guest physical address range|
|[ReadGuestRawSavedMemory](./reference/ReadGuestRawSavedMemory.md)|Read raw memory from the saved state file|
|[ReleaseSavedStateFiles](./reference/ReleaseSavedStateFiles.md)|Releases the given VmSavedStateDump provider that matches the supplied ID|
|   |   |
