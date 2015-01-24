# ananas
A Key-Value Framework For Object Drive

###1.1 Overview

This section describes basic Key Value Framework (KVF) concept and the overview, and the interface definition. Through KVF it defines unified data model, function, and parameters.

This Framework allows different Key Value Storage (KVS, also known as Key Value Store) regisgter and unregister, like Virtual File System (VFS) manages ext3, jfs, brtfs, etc.

And this framework provides unified API for upper application to call, to avoid write multiple adapters for different KVS, like call adapter for different vendors KVSs.

###1.2 Key Value Storage Introduction

Traditional storage is based on SCSI architecture, clients uses Logical Block Address (LBA) to read and write data. Upon block provides more services, such as file system, data base, etc.

As an alternative, Key Value Storage (also known as Object storage system) proveide Key-Vaule pair operation. Applicatin store value by specify key name, and key name maybe a variable string, also value is a variable data buffer. Then application is easy to store data, need no complicated layout design based on linear block space, only focuses on key name policy design and how to store key (like use Distributed Hashb Table to store it) . Upon KVS, it’s easy to build file, swift, hds, no-sql, even block service, shown as Figure_1.

Actually, 512 or 4096 byte based block device is a simple kind KVS, its key name is LBA and its value is 512 or 4096 data. Since its simplicity, application needs complicated layout design; and variable key value store is smarter, so application will be easy to store data on it. This is a kind of trade-off.
