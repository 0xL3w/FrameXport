# FrameXPort - 

### **Overview**

**FrameXPort** is a modified fork of the UxPlay project([UxPlay](https://github.com/FDH2/UxPlay)), designed to export frames via UDP. This fork aims to provide a custom method for frames to be streamed over the network for custom use cases.

The core functionality of UxPlay has been retained, excluding Gstreamer, with key adjustments made to disable Gstreamer and send frames exclusively via the UDP network protocol.

**Key Features**
- **UDP Frame export** - Allows frames to be exported via UDP for custom streaming or processing.
- **Based on UxPlay** - Retains the base functionality of UxPlay, while adding the ability to send frame data over the network.

**Setup**
- PLease follow the installation instructions in the original UxPlay README. THis can be found here. [UxPlay](https://github.com/FDH2/UxPlay)

**Modifications**
- **UDP Export functionality** - This modification introduces a feature which sends frame data over the UDP protocol, instead of sending this to Gstreamer for decoding. Gstreamer is disabled.

**License**
- This project is licensed under the same terms as the [UxPlay repository(https://github.com/FDH2/UxPlay). [See the full license here](https://github.com/FDH2/UxPlay?tab=GPL-3.0-1-ov-file)
