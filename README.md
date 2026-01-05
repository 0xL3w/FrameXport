# FrameXPort - 1.73

### 

**FrameXPort** is a modified fork of the [UxPlay](https://github.com/FDH2/UxPlay) project, designed to export frames via RTP/UDP. This fork aims to provide a custom method for frames to be streamed over the network for custom use cases.

The core functionality of UxPlay has been retained, with key adjustments made to disable Gstreamer and send frames exclusively via the RTP network protocol.

**Key Features**
- **RTP Frame export** - Allows frames to be exported via rtp/udp for custom streaming or processing.
- **Disable Gstreamer** - Allows the user to disable Gstreamer.
- **Disable Audio** - Currently, when using the "-nogst" flag, audio will be disabled. **This may change in future versions**

**Setup**
- Please follow the build instructions in the original UxPlay README. This can be found here. [UxPlay](https://github.com/FDH2/UxPlay)

**Usage**
**Flags:**
- -nogst - Disables gstreamer
- -rtp - HOST:PORT - RTP destination (IP and port)

Both flags need to be used together in order for FrameXport to work. This does not affect UxPlay functionality (This may change in future versions)

**Modifications**
- **RTP Export functionality** - This modification introduces a feature which sends frame data over the UDP protocol, instead of sending this to Gstreamer for decoding.
- **Multiple NAL Unit Parsing** - Properly handles H.264 SPS/PPS/IDR frames.
- **FU-A Fragmentation** - Handles large frames correctly (**This may be optional in the future via flags**)

**Note**
If receiving and displaying the RTP stream via Gstreamer, you may encounter format compatibility issues with different video sinks. Please ensure you are using the correct one for your use case. Display sinks are specific to Gstreamer. FFmpeg,VLC and other tools use their own display systems. 

**License**
- This project is licensed under the same terms as the [UxPlay repository](https://github.com/FDH2/UxPlay). [See the full license here](https://github.com/FDH2/UxPlay?tab=GPL-3.0-1-ov-file)
