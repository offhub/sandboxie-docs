# Sandbox Options - Resource Access

The _Resource Access_ window in [Sandboxie Plus](SbPlus.md) displays and changes the configuration and options associated with a single sandbox.

* * *

In this window, the individual settings are organized into settings pages, and some pages are organized into groups, as shown below.

![asdasdasd](../Media/SbPlusBox07ResAcc01Files.png)

The left part of the window contains the pages and the right upper part groups. When a settings page is selected (clicked) in the left part of the window, the right part of the window shows the related settings.

When a change has been made in a particular page, the change must be applied to Sandboxie before leaving settings page. This can be done manually using the Apply button.

**Note:** Most configuration changes do not apply to programs that are already running sandboxed at the time the configuration is changed. To keep things simple, you are advised to make configuration changes when no programs are running in the sandbox.

* * *

The sections below describe each settings group page.

# ![](../Media/Resources/AmpelHt1.png) Resource Access

## ![](../Media/Resources/FolderHt2.png) Files

> Configure which processes can access Files, Folders and Pipes.  
'Open' access only applies to program binaries located outside the sandbox, you can use 'Open for All' instead to make it apply to all programs, or change this behavior in the Policies tab.

* Add File/Folder

	* Browse for File
	
	* Browse for Folder	
	
* Show Templates

* Remove

## ![](../Media/Resources/RegEditHt2.png) Registry

> Configure which processes can access the Registry.  
'Open' access only applies to program binaries located outside the sandbox, you can use 'Open for All' instead to make it apply to all programs, or change this behavior in the Policies tab.

* Add Reg Key

* Show Templates

* Remove

## ![](../Media/Resources/PortHt2.png) IPC

> Configure which processes can access NT IPC objects like ALPC ports and other processes memory and context.  
To specify a process use '$:program.exe' as path.

* Add IPC Path

* Show Templates

* Remove

## ![](../Media/Resources/WindowHt2.png) Wnd

> Configure which processes can access Desktop objects like Windows and alike.

* Add Wnd Class

* Show Templates

* Don't alter the window title

* Remove

## ![](../Media/Resources/ObjectsHt2.png) COM

> Configure which processes can access COM objects.

* Add COM Object

* Show Templates

* Don't use virtualized COM, Open access to hosts COM infrastructure (not recommended)

* Remove

## ![](../Media/Resources/PolicyHt2.png) Access Policies

#### ![](../Media/Resources/AnonHt4.png) Access Mode

* Privacy Mode, block file and registry access to all locations except the generic system ones

	> When the Privacy Mode is enabled, sandboxed processes will be only able to read C:\Windows\\*, C:\Program Files\\*, and parts of the HKLM registry, all other locations will need explicit access to be readable and/or writable. In this mode, Rule Specificity is always enabled.

#### ![](../Media/Resources/PolicyHt4.png) Rule Policies

* Prioritize rules based on their Specificity and Process Match Level

	> The rule specificity is a measure to how well a given rule matches a particular path, simply put the specificity is the length of characters from the begin of the path up to and including the last matching non-wildcard substring. A rule which matches only file types like "\*.tmp" would have the highest specificity as it would always match the entire file path.  
	The process match level has a higher priority than the specificity and describes how a rule applies to a given process. Rules applying by process name or group have the strongest match level, followed by the match by negation (i.e. rules applying to all processes but the given one), while the lowest match levels have global matches, i.e. rules that apply to any process.
	
	> See [Use Rule Specificity](UseRuleSpecificity.md)

* Apply Close...=!\<program>,... rules also to all binaries located in the sandbox.

* Apply File and Key Open directives only to binaries located outside the sandbox.

* * *

For information about the settings, see these pages:

*	[General Options](SbPlusBox01GeneralOptions.md)

*	[Security Options](SbPlusBox02SecurityOptions.md)

*	[Program Groups](SbPlusBox03ProgramGroups.md)

*	[Program Control](SbPlusBox04ProgramControl.md)

*	[Stop Behaviour](SbPlusBox05StopBehaviour.md)

*	[Start Restrictions](SbPlusBox06StartRestrictions.md)

*	[Resource Access](SbPlusBox07ResourceAccess.md)

*	[Network Options](SbPlusBox08NetworkOptions.md)

*	[File Recovery](SbPlusBox90FileRecovery.md)

*	[Advanced Options](SbPlusBox10AdvancedOptions.md)

*	[App Templates](SbPlusBox11AppTemplates.md)

*	[Edit ini Section](SbPlusBox12EditIniSection.md)

