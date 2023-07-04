# Houdini Engine installation and licencing guide

## Downloading SideFX Houdini

Houdini Engine inside Unreal Engine still runs actual Houdini in the background, using chained CLI commands, this means each user who wants to use Houdini Engine needs full Houdini install on his/her machine.

Open [SideFX website](https://www.sidefx.com/), log-in using credencials provided by your superviser. Next, proceed to the **Get** menu, **Download** option.

<img width="668" alt="Screenshot_1" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/3bd4a5bb-0d9b-481a-8575-104b2ebf0957">

Scroll past installer/launcher options, down to **Production builds** button.

<img width="412" alt="Screenshot_2" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/18b7dcab-f41c-4c69-9ac8-435047151a5d">

In the builds archive, make sure to enable **Python 3** and **Windows** filters for easier time finding the correct build. We are interested, as of now, in version **19.5.569** -> _**houdini-19.5.569-win64-vc142.exe**_, click to download.

<img width="871" alt="Screenshot_4" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/ba17589f-e955-47db-a0f1-6bdb69097c28">


## Installing SideFX Houdini

Run the installer, we have a few toggles to mind during installation.

First of all, in the Choose Components step, make sure you have both **Licence Server** and **SideFX Labs** checkboxes are ticked.

<img width="374" alt="Screenshot_5" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/fecbeef5-e823-486a-851d-83c79f19aec9">

Next, on the Hoduini Engine step, make sure **Houdini Engine for Unreal** is ticked.
Note: Houdini Engine itself is provided with BP UE version you pull from version control, we install it just in case.

<img width="373" alt="Screenshot_6" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/e1de6b73-9710-4cd0-babf-a79f0eeb14f0">

Proceed with remaining steps at default.

## Installing Houdini Engine licence to local machine.

Even though Houdini Engine is free, the licences themselves still exist and need to be installed for each user.
Open newly installed application called **Licence Administrator 19.5.569**.

<img width="478" alt="Screenshot_8" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/0c17492f-f2d2-4528-9e8a-2ad5f35464e4">

Application will prompt login procedure, use the same credencials that have been used to download the Houdini package.

<img width="481" alt="Screenshot_9" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/da9085f9-cf21-4dba-af90-bbe14f82e570">

After succeseful login, a licence installation pop-up will come up. In the Houdini Engine product line, bump up the number of licences to be installed to **1** and click **Install**.

<img width="890" alt="Screenshot_10" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/53ad5739-9419-4e0b-ae93-f84d11d3bdfb">

If everything goes well, you will be presented with licences list and a Houdini Engine licence, that was installed.

<img width="693" alt="Screenshot_11" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/6dc20c8e-6a89-436f-8002-e1a5ba252454">

## Checking Houdini Engine inside UE.

Launch Unreal Engine project and look for **Houdini Engine** menu in the top bar.

<img width="542" alt="Screenshot_13" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/3f24d167-207e-4188-8b52-b14cc16865e9">

If **Houdini Engine** menu is not there, check presence of the **Houdini Engine** folder in BP Engine. Path to check - _**ENGINE_FOLDER/Engine/Plugins/Runtime**_.

<img width="453" alt="Screenshot_12" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/7480dab3-3e26-4c38-8ffe-d539942cadf4">

Next, we will make sure that path to your Houdini install is correct and fixed. In the **Houdini Engine** menu, pick **PluginSettings**.

<img width="294" alt="Screenshot_14" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/10bd63b7-5834-4614-be73-495fbaf2ec1e">

Scroll down to **Houdini Location** section. Make sure to tick **Use custom Houdini location**, then locate the **bin** folder inside your Houdini installation path, force executable to be plain **Houdini**. To save these settings - relaunch UE.

<img width="535" alt="Screenshot_15" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/33e8684f-b4c0-42f3-ae85-44f743102e7c">

If everything went through correctly - we can try to create a Houdini Engine session, basically it's an instance of Houdini that will be brought up to calculate HDA changes. In **Houdini Engine** dropdown select **Create Session**.

<img width="293" alt="Screenshot_16" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/f75a1bf4-d73f-467c-a1b7-2451cdbeed83">

Correct output is a pop-up in the lower left corner of the UE window, stating **Houdini Engine session connected**.

<img width="275" alt="Screenshot_17" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/3203dfe4-6fb3-43f2-88e3-585937adc1ee">

## Results

We have accomplished the following:
* Installed correct SideFX Houdini version.
* Installed Houdini Engine licence to the local machine.
* Confirmed correct installation.
