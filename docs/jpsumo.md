# projects.jpsumo
-----
### All commands specific to the Jumping Sumo.

Below is a table of all the jpsumo Project command classes.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Class Name | ID | Hex ID | Description |
|------------|----|--------|-------------|
|[Piloting](#projectsjpsumopiloting)|0|0x0|All commands related to piloting the JumpingSumo|
|[PilotingState](#projectsjpsumopilotingstate)|1|0x1|Animations state from JS.|
|[Animations](#projectsjpsumoanimations)|2|0x2|Animation commands|
|[AnimationsState](#projectsjpsumoanimationsstate)|3|0x3|Animations state from JS.|
|[SettingsState](#projectsjpsumosettingsstate)|5|0x5|Settings state from product|
|[MediaRecord](#projectsjpsumomediarecord)|6|0x6|Media recording management|
|[MediaRecordState](#projectsjpsumomediarecordstate)|7|0x7|State of media recording|
|[NetworkSettings](#projectsjpsumonetworksettings)|8|0x8|Network settings commands|
|[NetworkSettingsState](#projectsjpsumonetworksettingsstate)|9|0x9|Network settings state from product|
|[Network](#projectsjpsumonetwork)|10|0xa|Network related commands|
|[NetworkState](#projectsjpsumonetworkstate)|11|0xb|Network state from Product|
|[AudioSettings](#projectsjpsumoaudiosettings)|12|0xc|Audio settings.|
|[AudioSettingsState](#projectsjpsumoaudiosettingsstate)|13|0xd|Audio settings state.|
|[RoadPlan](#projectsjpsumoroadplan)|14|0xe|RoadPlan commands.|
|[RoadPlanState](#projectsjpsumoroadplanstate)|15|0xf|RoadPlan command responses.|
|[SpeedSettings](#projectsjpsumospeedsettings)|16|0x10|Speed Settings commands|
|[SpeedSettingsState](#projectsjpsumospeedsettingsstate)|17|0x11|Speed Settings state from product|
|[MediaStreaming](#projectsjpsumomediastreaming)|18|0x12|Control media streaming behavior.|
|[MediaStreamingState](#projectsjpsumomediastreamingstate)|19|0x13|Media streaming status.|
|[MediaRecordEvent](#projectsjpsumomediarecordevent)|20|0x14|Events of media recording|
|[VideoSettings](#projectsjpsumovideosettings)|21|0x15|Video settings.|
|[VideoSettingsState](#projectsjpsumovideosettingsstate)|22|0x16|Video settings state.|
# projects.jpsumo.Piloting
-----
### All commands related to piloting the JumpingSumo

The Piloting Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[PCMD](#projectsjpsumopilotingpcmd)|0|0x0|Ask the JS speed and turn ratio.|
|[Posture](#projectsjpsumopilotingposture)|1|0x1|Request a posture|
|[addCapOffset](#projectsjpsumopilotingaddcapoffset)|2|0x2|Add the specified offset to the current cap.|
## projects.jpsumo.Piloting.PCMD 

Ask the JS speed and turn ratio.




Example sending the ` PCMD ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.Piloting;

//build a message requesting all settings
const PCMDMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.PCMD
);

drone.message.send(PCMDMessage);

```


## projects.jpsumo.Piloting.Posture 

Request a posture




Example sending the ` Posture ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.Piloting;

//build a message requesting all settings
const PostureMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.Posture
);

drone.message.send(PostureMessage);

```


## projects.jpsumo.Piloting.addCapOffset 

Add the specified offset to the current cap.




Example sending the ` addCapOffset ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.Piloting;

//build a message requesting all settings
const addCapOffsetMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.addCapOffset
);

drone.message.send(addCapOffsetMessage);

```


# projects.jpsumo.PilotingState
-----
### Animations state from JS.

The PilotingState Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[PostureChanged](#projectsjpsumopilotingstateposturechanged)|0|0x0|State of posture changed.|
|[AlertStateChanged](#projectsjpsumopilotingstatealertstatechanged)|1|0x1|JS alert state changed|
|[SpeedChanged](#projectsjpsumopilotingstatespeedchanged)|2|0x2|Notification sent when JS speed changes.|
## projects.jpsumo.PilotingState.PostureChanged 

State of posture changed.




Example sending the ` PostureChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.PilotingState;

//build a message requesting all settings
const PostureChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.PostureChanged
);

drone.message.send(PostureChangedMessage);

```


## projects.jpsumo.PilotingState.AlertStateChanged 

JS alert state changed




Example sending the ` AlertStateChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.PilotingState;

//build a message requesting all settings
const AlertStateChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.AlertStateChanged
);

drone.message.send(AlertStateChangedMessage);

```


## projects.jpsumo.PilotingState.SpeedChanged 

Notification sent when JS speed changes.




Example sending the ` SpeedChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.PilotingState;

//build a message requesting all settings
const SpeedChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.SpeedChanged
);

drone.message.send(SpeedChangedMessage);

```


# projects.jpsumo.Animations
-----
### Animation commands

The Animations Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[JumpStop](#projectsjpsumoanimationsjumpstop)|0|0x0|Stop jump, emergency jump stop, stop jump motor and stay there.|
|[JumpCancel](#projectsjpsumoanimationsjumpcancel)|1|0x1|Cancel jump and come back to previous state (if possible).|
|[JumpLoad](#projectsjpsumoanimationsjumpload)|2|0x2|Request jump loading|
|[Jump](#projectsjpsumoanimationsjump)|3|0x3|Request a jump|
|[SimpleAnimation](#projectsjpsumoanimationssimpleanimation)|4|0x4|Play a parameterless animation.|
## projects.jpsumo.Animations.JumpStop 

Stop jump, emergency jump stop, stop jump motor and stay there.




Example sending the ` JumpStop ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.Animations;

//build a message requesting all settings
const JumpStopMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.JumpStop
);

drone.message.send(JumpStopMessage);

```


## projects.jpsumo.Animations.JumpCancel 

Cancel jump and come back to previous state (if possible).




Example sending the ` JumpCancel ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.Animations;

//build a message requesting all settings
const JumpCancelMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.JumpCancel
);

drone.message.send(JumpCancelMessage);

```


## projects.jpsumo.Animations.JumpLoad 

Request jump loading




Example sending the ` JumpLoad ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.Animations;

//build a message requesting all settings
const JumpLoadMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.JumpLoad
);

drone.message.send(JumpLoadMessage);

```


## projects.jpsumo.Animations.Jump 

Request a jump




Example sending the ` Jump ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.Animations;

//build a message requesting all settings
const JumpMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.Jump
);

drone.message.send(JumpMessage);

```


## projects.jpsumo.Animations.SimpleAnimation 

Play a parameterless animation.




Example sending the ` SimpleAnimation ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.Animations;

//build a message requesting all settings
const SimpleAnimationMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.SimpleAnimation
);

drone.message.send(SimpleAnimationMessage);

```


# projects.jpsumo.AnimationsState
-----
### Animations state from JS.

The AnimationsState Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[JumpLoadChanged](#projectsjpsumoanimationsstatejumploadchanged)|0|0x0|State of jump load changed|
|[JumpTypeChanged](#projectsjpsumoanimationsstatejumptypechanged)|1|0x1|State of jump type changed.|
|[JumpMotorProblemChanged](#projectsjpsumoanimationsstatejumpmotorproblemchanged)|2|0x2|State about the jump motor problem|
## projects.jpsumo.AnimationsState.JumpLoadChanged 

State of jump load changed




Example sending the ` JumpLoadChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.AnimationsState;

//build a message requesting all settings
const JumpLoadChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.JumpLoadChanged
);

drone.message.send(JumpLoadChangedMessage);

```


## projects.jpsumo.AnimationsState.JumpTypeChanged 

State of jump type changed.




Example sending the ` JumpTypeChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.AnimationsState;

//build a message requesting all settings
const JumpTypeChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.JumpTypeChanged
);

drone.message.send(JumpTypeChangedMessage);

```


## projects.jpsumo.AnimationsState.JumpMotorProblemChanged 

State about the jump motor problem




Example sending the ` JumpMotorProblemChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.AnimationsState;

//build a message requesting all settings
const JumpMotorProblemChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.JumpMotorProblemChanged
);

drone.message.send(JumpMotorProblemChangedMessage);

```


# projects.jpsumo.SettingsState
-----
### Settings state from product

The SettingsState Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[ProductGPSVersionChanged](#projectsjpsumosettingsstateproductgpsversionchanged)|0|0x0|@deprecated Product GPS versions|
## projects.jpsumo.SettingsState.ProductGPSVersionChanged 

@deprecated Product GPS versions




Example sending the ` ProductGPSVersionChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.SettingsState;

//build a message requesting all settings
const ProductGPSVersionChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.ProductGPSVersionChanged
);

drone.message.send(ProductGPSVersionChangedMessage);

```


# projects.jpsumo.MediaRecord
-----
### Media recording management

The MediaRecord Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[Picture](#projectsjpsumomediarecordpicture)|0|0x0|@deprecated Take picture|
|[Video](#projectsjpsumomediarecordvideo)|1|0x1|@deprecated Video record|
|[PictureV2](#projectsjpsumomediarecordpicturev2)|2|0x2|Take picture|
|[VideoV2](#projectsjpsumomediarecordvideov2)|3|0x3|Video record|
## projects.jpsumo.MediaRecord.Picture 

@deprecated Take picture




Example sending the ` Picture ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.MediaRecord;

//build a message requesting all settings
const PictureMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.Picture
);

drone.message.send(PictureMessage);

```


## projects.jpsumo.MediaRecord.Video 

@deprecated Video record




Example sending the ` Video ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.MediaRecord;

//build a message requesting all settings
const VideoMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.Video
);

drone.message.send(VideoMessage);

```


## projects.jpsumo.MediaRecord.PictureV2 

Take picture




Example sending the ` PictureV2 ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.MediaRecord;

//build a message requesting all settings
const PictureV2Message=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.PictureV2
);

drone.message.send(PictureV2Message);

```


## projects.jpsumo.MediaRecord.VideoV2 

Video record




Example sending the ` VideoV2 ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.MediaRecord;

//build a message requesting all settings
const VideoV2Message=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.VideoV2
);

drone.message.send(VideoV2Message);

```


# projects.jpsumo.MediaRecordState
-----
### State of media recording

The MediaRecordState Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[PictureStateChanged](#projectsjpsumomediarecordstatepicturestatechanged)|0|0x0|@deprecated State of picture recording|
|[VideoStateChanged](#projectsjpsumomediarecordstatevideostatechanged)|1|0x1|@deprecated State of video recording|
|[PictureStateChangedV2](#projectsjpsumomediarecordstatepicturestatechangedv2)|2|0x2|State of device picture recording changed|
|[VideoStateChangedV2](#projectsjpsumomediarecordstatevideostatechangedv2)|3|0x3|State of device video recording changed|
## projects.jpsumo.MediaRecordState.PictureStateChanged 

@deprecated State of picture recording




Example sending the ` PictureStateChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.MediaRecordState;

//build a message requesting all settings
const PictureStateChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.PictureStateChanged
);

drone.message.send(PictureStateChangedMessage);

```


## projects.jpsumo.MediaRecordState.VideoStateChanged 

@deprecated State of video recording




Example sending the ` VideoStateChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.MediaRecordState;

//build a message requesting all settings
const VideoStateChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.VideoStateChanged
);

drone.message.send(VideoStateChangedMessage);

```


## projects.jpsumo.MediaRecordState.PictureStateChangedV2 

State of device picture recording changed




Example sending the ` PictureStateChangedV2 ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.MediaRecordState;

//build a message requesting all settings
const PictureStateChangedV2Message=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.PictureStateChangedV2
);

drone.message.send(PictureStateChangedV2Message);

```


## projects.jpsumo.MediaRecordState.VideoStateChangedV2 

State of device video recording changed




Example sending the ` VideoStateChangedV2 ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.MediaRecordState;

//build a message requesting all settings
const VideoStateChangedV2Message=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.VideoStateChangedV2
);

drone.message.send(VideoStateChangedV2Message);

```


# projects.jpsumo.NetworkSettings
-----
### Network settings commands

The NetworkSettings Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[WifiSelection](#projectsjpsumonetworksettingswifiselection)|0|0x0|Auto_select channel of choosen band|
## projects.jpsumo.NetworkSettings.WifiSelection 

Auto_select channel of choosen band




Example sending the ` WifiSelection ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.NetworkSettings;

//build a message requesting all settings
const WifiSelectionMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.WifiSelection
);

drone.message.send(WifiSelectionMessage);

```


# projects.jpsumo.NetworkSettingsState
-----
### Network settings state from product

The NetworkSettingsState Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[WifiSelectionChanged](#projectsjpsumonetworksettingsstatewifiselectionchanged)|0|0x0|Wifi selection from product|
## projects.jpsumo.NetworkSettingsState.WifiSelectionChanged 

Wifi selection from product




Example sending the ` WifiSelectionChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.NetworkSettingsState;

//build a message requesting all settings
const WifiSelectionChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.WifiSelectionChanged
);

drone.message.send(WifiSelectionChangedMessage);

```


# projects.jpsumo.Network
-----
### Network related commands

The Network Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[WifiScan](#projectsjpsumonetworkwifiscan)|0|0x0|Launches wifi network scan|
|[WifiAuthChannel](#projectsjpsumonetworkwifiauthchannel)|1|0x1|Controller inquire the list of authorized wifi channels.|
## projects.jpsumo.Network.WifiScan 

Launches wifi network scan




Example sending the ` WifiScan ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.Network;

//build a message requesting all settings
const WifiScanMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.WifiScan
);

drone.message.send(WifiScanMessage);

```


## projects.jpsumo.Network.WifiAuthChannel 

Controller inquire the list of authorized wifi channels.




Example sending the ` WifiAuthChannel ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.Network;

//build a message requesting all settings
const WifiAuthChannelMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.WifiAuthChannel
);

drone.message.send(WifiAuthChannelMessage);

```


# projects.jpsumo.NetworkState
-----
### Network state from Product

The NetworkState Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[WifiScanListChanged](#projectsjpsumonetworkstatewifiscanlistchanged)|0|0x0|One scanning result found|
|[AllWifiScanChanged](#projectsjpsumonetworkstateallwifiscanchanged)|1|0x1|State sent when all scanning result sent|
|[WifiAuthChannelListChanged](#projectsjpsumonetworkstatewifiauthchannellistchanged)|2|0x2|Notify of an Authorized Channel.|
|[AllWifiAuthChannelChanged](#projectsjpsumonetworkstateallwifiauthchannelchanged)|3|0x3|Notify the end of the list of Authorized wifi Channel.|
|[LinkQualityChanged](#projectsjpsumonetworkstatelinkqualitychanged)|4|0x4|Notification sent by the firmware to give an indication of the WiFi link quality.|
## projects.jpsumo.NetworkState.WifiScanListChanged 

One scanning result found




Example sending the ` WifiScanListChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.NetworkState;

//build a message requesting all settings
const WifiScanListChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.WifiScanListChanged
);

drone.message.send(WifiScanListChangedMessage);

```


## projects.jpsumo.NetworkState.AllWifiScanChanged 

State sent when all scanning result sent




Example sending the ` AllWifiScanChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.NetworkState;

//build a message requesting all settings
const AllWifiScanChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.AllWifiScanChanged
);

drone.message.send(AllWifiScanChangedMessage);

```


## projects.jpsumo.NetworkState.WifiAuthChannelListChanged 

Notify of an Authorized Channel.




Example sending the ` WifiAuthChannelListChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.NetworkState;

//build a message requesting all settings
const WifiAuthChannelListChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.WifiAuthChannelListChanged
);

drone.message.send(WifiAuthChannelListChangedMessage);

```


## projects.jpsumo.NetworkState.AllWifiAuthChannelChanged 

Notify the end of the list of Authorized wifi Channel.




Example sending the ` AllWifiAuthChannelChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.NetworkState;

//build a message requesting all settings
const AllWifiAuthChannelChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.AllWifiAuthChannelChanged
);

drone.message.send(AllWifiAuthChannelChangedMessage);

```


## projects.jpsumo.NetworkState.LinkQualityChanged 

Notification sent by the firmware to give an indication of the WiFi link quality.




Example sending the ` LinkQualityChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.NetworkState;

//build a message requesting all settings
const LinkQualityChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.LinkQualityChanged
);

drone.message.send(LinkQualityChangedMessage);

```


# projects.jpsumo.AudioSettings
-----
### Audio settings.

The AudioSettings Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[MasterVolume](#projectsjpsumoaudiosettingsmastervolume)|0|0x0|Master volume control.|
|[Theme](#projectsjpsumoaudiosettingstheme)|1|0x1|Audio Theme.|
## projects.jpsumo.AudioSettings.MasterVolume 

Master volume control.




Example sending the ` MasterVolume ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.AudioSettings;

//build a message requesting all settings
const MasterVolumeMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.MasterVolume
);

drone.message.send(MasterVolumeMessage);

```


## projects.jpsumo.AudioSettings.Theme 

Audio Theme.




Example sending the ` Theme ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.AudioSettings;

//build a message requesting all settings
const ThemeMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.Theme
);

drone.message.send(ThemeMessage);

```


# projects.jpsumo.AudioSettingsState
-----
### Audio settings state.

The AudioSettingsState Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[MasterVolumeChanged](#projectsjpsumoaudiosettingsstatemastervolumechanged)|0|0x0|Master volume control.|
|[ThemeChanged](#projectsjpsumoaudiosettingsstatethemechanged)|1|0x1|Command to notify controller of new Audio Theme.|
## projects.jpsumo.AudioSettingsState.MasterVolumeChanged 

Master volume control.




Example sending the ` MasterVolumeChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.AudioSettingsState;

//build a message requesting all settings
const MasterVolumeChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.MasterVolumeChanged
);

drone.message.send(MasterVolumeChangedMessage);

```


## projects.jpsumo.AudioSettingsState.ThemeChanged 

Command to notify controller of new Audio Theme.




Example sending the ` ThemeChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.AudioSettingsState;

//build a message requesting all settings
const ThemeChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.ThemeChanged
);

drone.message.send(ThemeChangedMessage);

```


# projects.jpsumo.RoadPlan
-----
### RoadPlan commands.

The RoadPlan Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[AllScriptsMetadata](#projectsjpsumoroadplanallscriptsmetadata)|0|0x0|Command to ask device all metadata scripts.|
|[ScriptUploaded](#projectsjpsumoroadplanscriptuploaded)|1|0x1|Notify device that a new file has been uploaded.|
|[ScriptDelete](#projectsjpsumoroadplanscriptdelete)|2|0x2|Ask the device to delete a script.|
|[PlayScript](#projectsjpsumoroadplanplayscript)|3|0x3|Ask the device to play a script.|
## projects.jpsumo.RoadPlan.AllScriptsMetadata 

Command to ask device all metadata scripts.




Example sending the ` AllScriptsMetadata ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.RoadPlan;

//build a message requesting all settings
const AllScriptsMetadataMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.AllScriptsMetadata
);

drone.message.send(AllScriptsMetadataMessage);

```


## projects.jpsumo.RoadPlan.ScriptUploaded 

Notify device that a new file has been uploaded.




Example sending the ` ScriptUploaded ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.RoadPlan;

//build a message requesting all settings
const ScriptUploadedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.ScriptUploaded
);

drone.message.send(ScriptUploadedMessage);

```


## projects.jpsumo.RoadPlan.ScriptDelete 

Ask the device to delete a script.




Example sending the ` ScriptDelete ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.RoadPlan;

//build a message requesting all settings
const ScriptDeleteMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.ScriptDelete
);

drone.message.send(ScriptDeleteMessage);

```


## projects.jpsumo.RoadPlan.PlayScript 

Ask the device to play a script.




Example sending the ` PlayScript ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.RoadPlan;

//build a message requesting all settings
const PlayScriptMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.PlayScript
);

drone.message.send(PlayScriptMessage);

```


# projects.jpsumo.RoadPlanState
-----
### RoadPlan command responses.

The RoadPlanState Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[ScriptMetadataListChanged](#projectsjpsumoroadplanstatescriptmetadatalistchanged)|0|0x0|Update the controller with metadata.|
|[AllScriptsMetadataChanged](#projectsjpsumoroadplanstateallscriptsmetadatachanged)|1|0x1|Notify controller that all script metadatas are updated.|
|[ScriptUploadChanged](#projectsjpsumoroadplanstatescriptuploadchanged)|2|0x2|Device response to ScriptUploaded command.|
|[ScriptDeleteChanged](#projectsjpsumoroadplanstatescriptdeletechanged)|3|0x3|Device response to ScriptDelete command.|
|[PlayScriptChanged](#projectsjpsumoroadplanstateplayscriptchanged)|4|0x4|Device response to PlayScript command.|
## projects.jpsumo.RoadPlanState.ScriptMetadataListChanged 

Update the controller with metadata.




Example sending the ` ScriptMetadataListChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.RoadPlanState;

//build a message requesting all settings
const ScriptMetadataListChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.ScriptMetadataListChanged
);

drone.message.send(ScriptMetadataListChangedMessage);

```


## projects.jpsumo.RoadPlanState.AllScriptsMetadataChanged 

Notify controller that all script metadatas are updated.




Example sending the ` AllScriptsMetadataChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.RoadPlanState;

//build a message requesting all settings
const AllScriptsMetadataChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.AllScriptsMetadataChanged
);

drone.message.send(AllScriptsMetadataChangedMessage);

```


## projects.jpsumo.RoadPlanState.ScriptUploadChanged 

Device response to ScriptUploaded command.




Example sending the ` ScriptUploadChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.RoadPlanState;

//build a message requesting all settings
const ScriptUploadChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.ScriptUploadChanged
);

drone.message.send(ScriptUploadChangedMessage);

```


## projects.jpsumo.RoadPlanState.ScriptDeleteChanged 

Device response to ScriptDelete command.




Example sending the ` ScriptDeleteChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.RoadPlanState;

//build a message requesting all settings
const ScriptDeleteChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.ScriptDeleteChanged
);

drone.message.send(ScriptDeleteChangedMessage);

```


## projects.jpsumo.RoadPlanState.PlayScriptChanged 

Device response to PlayScript command.




Example sending the ` PlayScriptChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.RoadPlanState;

//build a message requesting all settings
const PlayScriptChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.PlayScriptChanged
);

drone.message.send(PlayScriptChangedMessage);

```


# projects.jpsumo.SpeedSettings
-----
### Speed Settings commands

The SpeedSettings Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[Outdoor](#projectsjpsumospeedsettingsoutdoor)|0|0x0|@deprecated Outdoor property|
## projects.jpsumo.SpeedSettings.Outdoor 

@deprecated Outdoor property




Example sending the ` Outdoor ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.SpeedSettings;

//build a message requesting all settings
const OutdoorMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.Outdoor
);

drone.message.send(OutdoorMessage);

```


# projects.jpsumo.SpeedSettingsState
-----
### Speed Settings state from product

The SpeedSettingsState Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[OutdoorChanged](#projectsjpsumospeedsettingsstateoutdoorchanged)|0|0x0|@deprecated Outdoor property sent by product|
## projects.jpsumo.SpeedSettingsState.OutdoorChanged 

@deprecated Outdoor property sent by product




Example sending the ` OutdoorChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.SpeedSettingsState;

//build a message requesting all settings
const OutdoorChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.OutdoorChanged
);

drone.message.send(OutdoorChangedMessage);

```


# projects.jpsumo.MediaStreaming
-----
### Control media streaming behavior.

The MediaStreaming Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[VideoEnable](#projectsjpsumomediastreamingvideoenable)|0|0x0|Enable/disable video streaming.|
## projects.jpsumo.MediaStreaming.VideoEnable 

Enable/disable video streaming.




Example sending the ` VideoEnable ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.MediaStreaming;

//build a message requesting all settings
const VideoEnableMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.VideoEnable
);

drone.message.send(VideoEnableMessage);

```


# projects.jpsumo.MediaStreamingState
-----
### Media streaming status.

The MediaStreamingState Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[VideoEnableChanged](#projectsjpsumomediastreamingstatevideoenablechanged)|0|0x0|Return video streaming status.|
## projects.jpsumo.MediaStreamingState.VideoEnableChanged 

Return video streaming status.




Example sending the ` VideoEnableChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.MediaStreamingState;

//build a message requesting all settings
const VideoEnableChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.VideoEnableChanged
);

drone.message.send(VideoEnableChangedMessage);

```


# projects.jpsumo.MediaRecordEvent
-----
### Events of media recording

The MediaRecordEvent Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[PictureEventChanged](#projectsjpsumomediarecordeventpictureeventchanged)|0|0x0|Event of picture recording|
|[VideoEventChanged](#projectsjpsumomediarecordeventvideoeventchanged)|1|0x1|Event of video recording|
## projects.jpsumo.MediaRecordEvent.PictureEventChanged 

Event of picture recording




Example sending the ` PictureEventChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.MediaRecordEvent;

//build a message requesting all settings
const PictureEventChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.PictureEventChanged
);

drone.message.send(PictureEventChangedMessage);

```


## projects.jpsumo.MediaRecordEvent.VideoEventChanged 

Event of video recording




Example sending the ` VideoEventChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.MediaRecordEvent;

//build a message requesting all settings
const VideoEventChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.VideoEventChanged
);

drone.message.send(VideoEventChangedMessage);

```


# projects.jpsumo.VideoSettings
-----
### Video settings.

The VideoSettings Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[Autorecord](#projectsjpsumovideosettingsautorecord)|0|0x0|Set video automatic recording state.|
## projects.jpsumo.VideoSettings.Autorecord 

Set video automatic recording state.




Example sending the ` Autorecord ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.VideoSettings;

//build a message requesting all settings
const AutorecordMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.Autorecord
);

drone.message.send(AutorecordMessage);

```


# projects.jpsumo.VideoSettingsState
-----
### Video settings state.

The VideoSettingsState Class contains the following commands.
All hex IDs are included as well incase you need them for debugging or extending the module.

| Command Name | ID | Hex ID | Description |
|--------------|----|--------|-------------|
|[AutorecordChanged](#projectsjpsumovideosettingsstateautorecordchanged)|0|0x0|Get video automatic recording status.|
## projects.jpsumo.VideoSettingsState.AutorecordChanged 

Get video automatic recording status.




Example sending the ` AutorecordChanged ` command to your parrot drone :

```javascript

const project=drone.projects.jpsumo;
const commandClass=project.VideoSettingsState;

//build a message requesting all settings
const AutorecordChangedMessage=drone.message.build(
  project.id,
  commandClass.id,
  commandClass.AutorecordChanged
);

drone.message.send(AutorecordChangedMessage);

```
