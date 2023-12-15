# Houdini Engine installation and licencing guide

## Downloading SideFX Houdini

Houdini Engine inside Unreal Engine still runs actual Houdini in the background, using chained CLI commands, this means each user who wants to use Houdini Engine needs full Houdini install on his/her machine.

Open [SideFX website](https://www.sidefx.com/), log-in using credencials provided by your superviser. Next, proceed to the **Get** menu, **Download** option.

<img width="668" alt="Screenshot_1" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/8c9a05a7-f17f-4a29-bef3-f6dac5647b04">

Scroll past installer/launcher options, down to **Production builds** button.

<img width="412" alt="Screenshot_2" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/40266769-5a7d-4b32-8c7c-d9679d03c1f5">

In the builds archive, make sure to enable **Python 3** and **Windows** filters for easier time finding the correct build. We are interested, as of now, in version **19.5.569** -> _**houdini-19.5.569-win64-vc142.exe**_, click to download.

<img width="871" alt="Screenshot_4" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/0f113268-bf49-4683-bece-4f8223a3df48">

## Installing SideFX Houdini

Run the installer, we have a few toggles to mind during installation.

First of all, in the Choose Components step, make sure you have both **Licence Server** and **SideFX Labs** checkboxes are ticked.

<img width="374" alt="Screenshot_5" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/2676945d-5c94-43fa-978a-b990a366fcaa">

Next, on the Hoduini Engine step, make sure **Houdini Engine for Unreal** is ticked.
Note: Houdini Engine itself is provided with BP UE version you pull from version control, we install it just in case.

<img width="373" alt="Screenshot_6" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/d03138b8-aca2-4cd1-8be1-7c6b7d4a5d8a">

Proceed with remaining steps at default.

## Installing Houdini Engine licence to local machine.

Even though Houdini Engine is free, the licences themselves still exist and need to be installed for each user.
Open newly installed application called **Licence Administrator 19.5.569**.

<img width="478" alt="Screenshot_8" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/7a5f4461-ca8c-4e97-ac7a-f12081d02ba4">

Application will prompt login procedure, use the same credencials that have been used to download the Houdini package.

<img width="481" alt="Screenshot_9" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/5dcdfec4-50be-4b5e-a98c-66c730d305a1">

After succeseful login, a licence installation pop-up will come up. In the Houdini Engine product line, bump up the number of licences to be installed to **1** and click **Install**.

<img width="890" alt="Screenshot_10" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/b1b0f6ec-5cac-4a83-bd0e-630c05380d21">

If everything goes well, you will be presented with licences list and a Houdini Engine licence, that was installed.

<img width="693" alt="Screenshot_11" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/46045a74-081d-43f3-a62e-40437c3a93ef">

## Checking Houdini Engine inside UE.

Launch Unreal Engine project and look for **Houdini Engine** menu in the top bar.

<img width="542" alt="Screenshot_13" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/5e6a5afc-1723-46eb-a32a-1d0542914352">

If **Houdini Engine** menu is not there, check presence of the **Houdini Engine** folder in BP Engine. Path to check - _**ENGINE_FOLDER/Engine/Plugins/Runtime**_.

<img width="453" alt="Screenshot_12" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/f1c29982-6349-42af-9de5-42f4a14392a9">

Next, we will make sure that path to your Houdini install is correct and fixed. In the **Houdini Engine** menu, pick **PluginSettings**.

<img width="294" alt="Screenshot_14" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/c7394198-0687-416e-9d40-94097d5f0774">

Scroll down to **Houdini Location** section. Make sure to tick **Use custom Houdini location**, then locate the **bin** folder inside your Houdini installation path, force executable to be plain **Houdini**. To save these settings - relaunch UE.

<img width="535" alt="Screenshot_15" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/9344b726-7da1-4026-b5c7-c22a898a558d">

If everything went through correctly - we can try to create a Houdini Engine session, basically it's an instance of Houdini that will be brought up to calculate HDA changes. In **Houdini Engine** dropdown select **Create Session**.

<img width="293" alt="Screenshot_16" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/3be95604-a92a-41ef-80fe-b0b0354b108d">

Correct output is a pop-up in the lower right corner of your display, stating **Houdini Engine session connected**.

<img width="275" alt="Screenshot_17" src="https://github.com/vsamusenko/BP_HE_guide/assets/54007382/7f15ccf3-72a7-47cd-9fea-d68b30f7e9f9">

## Results

We have accomplished the following:
* Installed correct SideFX Houdini version.
* Installed Houdini Engine licence to the local machine.
* Confirmed correct installation.
