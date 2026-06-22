# Secondary Storage

## Size/Speed/Cost

| Type              | Size         | Speed           | Cost   |
|-------------------|--------------|-----------------|--------|
| Flash memory      | Up to 1TB    | Up to 10Gbps    | $$$$$$ |
| HHD - PC          | 1 to 8TB     | 6Gbps           | $$$    |
| HDD - Laptop      | 0.5 to 4TB   | 3 to 6Gbps      | $$$$   |
| SSD               | 120 to 960GB | 500 to 1000MBps | $$$$$  |
| External HDD 3.5" | 4 to 8TB     | 6Gbps           | $      |
| External HDD 2.5" | 1 to 5TB     | 3 to 6Gbps      | $$     |

## Cloud Storage

A form of secondary storage which is itself connected to
remote storage using the internet

**Size**
> Popular services like Google Drive or Drop box provide
> a limit of up to 15GB and 2GB, but the real maximum size
> is extremely large, within terabytes

**Speed**
> Because data is transferred between your computer and a service
> provider's server over the internet, this is determined by
> the speed of your internet.

**Cost**
> Costs vary between service providers with some offering
> extra benefits like security.

## M.2 Format

M.2 is a form factor - it describes the shape and size of a
hardware device. The M.2 connector can access the PCIe 3.0,
SATA 3.0 and USB 3.0 bus, depending on the type of M.2 device.

The motherboard decides what that specific M.2 slot
supports. Either PCIe bus, SATA bus (older systems)
and rarer, USB bus.

An M.2 SATA SSD can connect via the M.2 connector but will
use the slower SATA bus, whereas an NVMe SSD will use the
PCIe bus, allowing NVMe drives to run at much faster speeds.

| Category | SATA \|\|\| SSD | NVMe SSD  |
|----------|-----------------|-----------|
| Read     | 530 MB/s        | 3500 MB/s |
| Write    | 500 MB/s        | 3000 MB/s |