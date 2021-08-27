# Exo Sense Pi Node-RED

Node-RED for Exo Sense Pi - Multi-sensor module with Raspberry Pi 4 core.

Install and run Node-RED on Exo Sense Pi and access all its functionalities with this module.

## Setup

Before using this node make sure the [Exo Sense Pi kernel module](https://github.com/sfera-labs/exo-sense-pi-kernel-module) is installed on Exo Sense Pi.

## Usage

This node lets you control and monitor the functionalities of Exo Sense Pi
by reading/writing the sysfs files provided by its
<a href="https://github.com/sfera-labs/exo-sense-pi-kernel-module" target="_blank">Kernel module</a>.


### Inputs
<dl class="message-properties">
    <dt>payload - <span class="property-type">string | number</span></dt>
    <dd>the value to write or empty to only trigger a read.</dd>
</dl>

### Outputs
<dl class="message-properties">
  (Readable features only)
  <dt>payload - <span class="property-type">string</span></dt>
  <dd>the value read.</dd>
</dl>

In the configuration, select the functionality (sysfs file) to link this node to.
Functionalities can be readable (R) and/or writable (W).<br>
Use <code>msg.payload</code> as the value to write to or read from the file.

For details on the values' formats refer to the
<a href="https://github.com/sfera-labs/exo-sense-pi-kernel-module#readme" target="_blank">Kernel module documentation</a>.
