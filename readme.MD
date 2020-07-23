# OBS-NativeCam
obs-NativeCam is a fork of obs-VirtualCam which attempts to ensure maximum quality and native-resolution output of OBS sources.

1) The output plugin/main menu tool has been removed, preventing users from making the mistake of scaling their source into whatever their OBS canvas resolution is and outputting that.

2) The directshow source outputs RGB32 in an attempt to prevent any unnecessary color loss due to chroma subsampling.

3) The directshow source does not support any scaled resolutions at all. If there is no OBS stream active, the directshow filter will fail to open. The OBS stream must be started first, then the directshow filter will output exactly the resolution of the OBS source.

Refer to https://github.com/catxFish/obs-virtual-cam for further info
