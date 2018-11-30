# Magic Mirror² Module: MMM-Dynamic-Modules

MMM-Dynamic-Modules moves modules without need to restart Magic Mirror. Module also allows to hide or show modules. Module have method to change configured positions back.

## Installation


```bash
cd ~/MagicMirror/modules
git clone https://github.com/Toreke/MMM-Dynamic-Modules.git
```

Config:

```
{
	module: "MMM-Dynamic-Modules",
},
```

## How to use


Module can be used by following way:

```
this.sendNotification('CHANGE_POSITIONS', 
	modules = {
		'clock':{
			visible: 'true',
			position: 'top_right',
		},

		'MMM-WeeklySchedule':{
			visible: 'true',
			position: 'top_left',
		},

		'MMM-AirQuality':{
			visible: 'true',
			position: 'bottom_bar',
		}
	}
);
```

And positions according to your config:

```
this.sendNotification(CHANGE_POSITIONS_DEFAULTS);
```

Order of the modules matters. If there is multiple modules in the same position, first module will be top, second module under it, and so on.