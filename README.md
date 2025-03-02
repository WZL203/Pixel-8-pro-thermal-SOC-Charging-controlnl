# Pixel-8-pro-SOC-
这是Pixel 8 pro SOC节流和充电优化的项目
{
    "Sensors": [
        {
            "Name": "north_therm",
            "Type": "UNKNOWN",
            "HotThreshold": ["NaN", 32.1, "NaN", "NaN", "NaN", "NaN", "NaN"],
            "HotHysteresis": [0.0, 0.9, 0.0, 0.0, 0.0, 0.0, 0.0],
            "Multiplier": 0.001,
            "PollingDelay": 60000,
            "PassiveDelay": 7000
        },
        {
            "Name": "cam_therm",
            "Type": "UNKNOWN",
            "HotThreshold": ["NaN", 33.7, "NaN", "NaN", "NaN", "NaN", "NaN"],
            "HotHysteresis": [0.0, 0.9, 0.0, 0.0, 0.0, 0.0, 0.0],
            "Multiplier": 0.001,
            "PollingDelay": 60000,
            "PassiveDelay": 7000
        },
        {
            "Name": "soc_therm",
            "Type": "UNKNOWN",
            "HotThreshold": ["NaN", 47.2, "NaN", "NaN", "NaN", "NaN", "NaN"],
            "HotHysteresis": [0.0, 0.9, 0.0, 0.0, 0.0, 0.0, 0.0],
            "Multiplier": 0.001,
            "PollingDelay": 60000,
            "PassiveDelay": 7000
        },
        {
            "Name": "charge_therm",
            "Type": "UNKNOWN",
            "HotThreshold": ["NaN", 48.4, "NaN", "NaN", "NaN", "NaN", "NaN"],
            "HotHysteresis": [0.0, 0.9, 0.0, 0.0, 0.0, 0.0, 0.0],
            "Multiplier": 0.001,
            "PollingDelay": 60000,
            "PassiveDelay": 7000
        },
        {
            "Name": "disp_therm",
            "Type": "UNKNOWN",
            "HotThreshold": ["NaN", 31.7, "NaN", "NaN", "NaN", "NaN", "NaN"],
            "HotHysteresis": [0.0, 0.9, 0.0, 0.0, 0.0, 0.0, 0.0],
            "Multiplier": 0.001,
            "PollingDelay": 60000,
            "PassiveDelay": 7000
        },
        {
            "Name": "battery",
            "Type": "BATTERY",
            "HotThreshold": ["NaN", "NaN", "NaN", "NaN", "NaN", "NaN", 65.0],
            "Multiplier": 0.001
        },
        {
            "Name": "neutral_therm",
            "Type": "UNKNOWN",
            "Multiplier": 0.001
        },
        {
            "Name": "quiet_therm",
            "Type": "UNKNOWN",
            "HotThreshold": ["NaN", 34.6, "NaN", "NaN", "NaN", "NaN", "NaN"],
            "HotHysteresis": [0.0, 0.9, 0.0, 0.0, 0.0, 0.0, 0.0],
            "Multiplier": 0.001,
            "PollingDelay": 60000,
            "PassiveDelay": 7000
        },
        {
            "Name": "usb_pwr_therm",
            "Type": "UNKNOWN",
            "HotThreshold": ["NaN", 35.0, "NaN", "NaN", "NaN", "NaN", "NaN"],
            "Multiplier": 0.001,
            "PollingDelay": 60000,
            "PassiveDelay": 7000
        },
        {
            "Name": "VIRTUAL-BTS-WINDOW-PARTIAL",
            "Type": "UNKNOWN",
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["cam_therm", "north_therm"],
            "Coefficient": [0.05, 0.14],
            "Offset": 560,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-SUB-0",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0, 0.27, 0.17, 0.11, 0, 0.2, 0.01, 0.06, 0.08],
            "Offset": 2110,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-SUB-1",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0.46, 0, 0.14, 0.28, 0, 0.06, 0.02, 0.14, 0],
            "Offset": -7280,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-SUB-2",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0.07, 0, 0, 0, 0, 0.28, 0.15, 0.02, 0.3],
            "Offset": 4010,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-SUB-3",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0.27, 0.06, 0.3, 0, 0, 0.2, 0.03, 0.02, 0.04],
            "Offset": 10,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-SUB-4",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0.9, 0, 0.05, 0, 0, 0, 0.01, 0, 0],
            "Offset": 730,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-SUB-5",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0.08, 0.02, 0.24, 0.23, 0, 0.29, 0.01, 0, 0],
            "Offset": 1870,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-SUB-6",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0, 0, 0, 0.04, 0.2, 0.07, 0.15, 0.3, 0.16],
            "Offset": -440,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-SUB-7",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0, 0.01, 0, 0, 0.07, 0.28, 0.25, 0.02, 0.08],
            "Offset": 9170,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-SUB-8",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0.1, 0.16, 0.11, 0.19, 0.26, 0, 0, 0.11, 0],
            "Offset": 1140,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-SUB-9",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0.02, 0.05, 0.21, 0.13, 0.02, 0.29, 0.09, 0, 0],
            "Offset": 5160,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-SUB-10",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0, 0, 0.16, 0, 0.49, 0.35, 0, 0, 0],
            "Offset": -1500,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN",
            "Type": "SKIN",
            "Version": "5.0",
            "VirtualSensor": true,
            "TriggerSensor": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "quiet_therm", "usb_pwr_therm"],
            "Formula": "MAXIMUM",
            "Combination": ["VIRTUAL-SKIN-SUB-0", "VIRTUAL-SKIN-SUB-1", "VIRTUAL-SKIN-SUB-2",
                            "VIRTUAL-SKIN-SUB-3", "VIRTUAL-SKIN-SUB-4", "VIRTUAL-SKIN-SUB-5",
                            "VIRTUAL-SKIN-SUB-6", "VIRTUAL-SKIN-SUB-7", "VIRTUAL-SKIN-SUB-8", "VIRTUAL-SKIN-SUB-9", "VIRTUAL-SKIN-SUB-10"],
            "Coefficient": [1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0],
            "HotThreshold": ["NaN", "NaN", "NaN", "NaN", "NaN", 52.0, 55.0],
            "HotHysteresis": [0.0, 0.0, 0.0, 0.0, 0.0, 1.9, 1.9],
            "Multiplier": 0.001,
            "SendCallback": true,
            "PollingDelay": 300000,
            "PassiveDelay": 7000,
            "BindedCdevInfo": [
                {
                    "CdevRequest": "gxp-cooling",
                    "LimitInfo": [0, 0, 0, 0, 0, 6, 6]
                }
            ]
        },
        {
            "Name": "VIRTUAL-SKIN-HINT",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "TriggerSensor": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "quiet_therm", "usb_pwr_therm"],
            "Formula": "MAXIMUM",
            "Combination": ["VIRTUAL-SKIN"],
            "Coefficient": [1.0],
            "HotThreshold": ["NaN", "NaN", "NaN", "NaN", "NaN", 52.0, 55.0],
            "HotHysteresis": [0.0, 0.0, 0.0, 0.0, 0.0, 1.9, 1.9],
            "Multiplier": 0.001,
            "SendPowerHint": true,
            "PollingDelay": 300000,
            "PassiveDelay": 7000
        },
        {
            "Name": "VIRTUAL-SKIN-CPU-LIGHT-ODPM",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "TriggerSensor": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "quiet_therm", "usb_pwr_therm"],
            "Formula": "MAXIMUM",
            "Combination": ["VIRTUAL-SKIN"],
            "Coefficient": [1.0],
            "HotThreshold": ["NaN", "NaN", "NaN", "NaN", "NaN", 45.0, 48.0],
            "HotHysteresis": [0.0, 0.0, 0.0, 0.0, 0.0, 1.9, 1.9],
            "Multiplier": 0.001,
            "PollingDelay": 300000,
            "PassiveDelay": 7000,
            "PIDInfo": {
                "K_Po": ["NaN", "NaN", 400, "NaN", "NaN", "NaN", "NaN"],
                "K_Pu": ["NaN", "NaN", 400, "NaN", "NaN", "NaN", "NaN"],
                "K_I": ["NaN", "NaN", 5, "NaN", "NaN", "NaN", "NaN"],
                "K_D": ["NaN", "NaN", 0, "NaN", "NaN", "NaN", "NaN"],
                "I_Max": ["NaN", "NaN", 2200, "NaN", "NaN", "NaN", "NaN"],
                "S_Power": ["NaN", "NaN", 800, "NaN", "NaN", "NaN", "NaN"],
                "MinAllocPower": ["NaN", "NaN", 800, "NaN", "NaN", "NaN", "NaN"],
                "MaxAllocPower": ["NaN", "NaN", 4600, "NaN", "NaN", "NaN", "NaN"],
                "I_Cutoff": ["NaN", "NaN", 4, "NaN", "NaN", "NaN", "NaN"]
            },
            "BindedCdevInfo": [
                {
                    "CdevRequest": "thermal-cpufreq-0",
                    "CdevWeightForPID": [1, 1, 1, 1, 1, 1, 1],
                    "MaxReleaseStep": 1,
                    "MaxThrottleStep": 1,
                    "BindedPowerRail": "S4M_VDD_CPUCL0",
                    "CdevCeiling": [0, 2, 2, 2, 2, 2, 2]
                },
                {
                    "CdevRequest": "thermal-cpufreq-1",
                    "CdevWeightForPID": [1, 1, 1, 1, 1, 1, 1],
                    "MaxReleaseStep": 1,
                    "MaxThrottleStep": 2,
                    "BindedPowerRail": "S3M_VDD_CPUCL1",
                    "CdevCeiling": [0, 6, 6, 6, 6, 6, 6]
                },
                {
                    "CdevRequest": "thermal-cpufreq-2",
                    "CdevWeightForPID": [1, 1, 1, 1, 1, 1, 1],
                    "MaxReleaseStep": 1,
                    "MaxThrottleStep": 2,
                    "BindedPowerRail": "S2M_VDD_CPUCL2",
                    "CdevCeiling": [0, 8, 8, 8, 8, 8, 8]
                }
            ]
        },
        {
            "Name": "VIRTUAL-SKIN-CPU-MID",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "TriggerSensor": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "quiet_therm", "usb_pwr_therm"],
            "Formula": "MAXIMUM",
            "Combination": ["VIRTUAL-SKIN"],
            "Coefficient": [1.0],
            "HotThreshold": ["NaN", "NaN", "NaN", "NaN", "NaN", 45.0, 48.0],
            "HotHysteresis": [0.0, 0.0, 0.0, 0.0, 0.0, 1.9, 1.9],
            "Multiplier": 0.001,
            "PollingDelay": 300000,
            "PassiveDelay": 7000,
            "PIDInfo": {
                "K_Po": ["NaN", "NaN", 400, "NaN", "NaN", "NaN", "NaN"],
                "K_Pu": ["NaN", "NaN", 400, "NaN", "NaN", "NaN", "NaN"],
                "K_I": ["NaN", "NaN", 5, "NaN", "NaN", "NaN", "NaN"],
                "K_D": ["NaN", "NaN", 0, "NaN", "NaN", "NaN", "NaN"],
                "I_Max": ["NaN", "NaN", 1500, "NaN", "NaN", "NaN", "NaN"],
                "S_Power": ["NaN", "NaN", 700, "NaN", "NaN", "NaN", "NaN"],
                "MinAllocPower": ["NaN", "NaN", 0, "NaN", "NaN", "NaN", "NaN"],
                "MaxAllocPower": ["NaN", "NaN", 2800, "NaN", "NaN", "NaN", "NaN"],
                "I_Cutoff": ["NaN", "NaN", 4, "NaN", "NaN", "NaN", "NaN"]
            },
            "BindedCdevInfo": [
                {
                    "CdevRequest": "thermal-cpufreq-0",
                    "CdevWeightForPID": [0.292, 0.292, 0.292, 0.292, 0.292, 0.292, 0.292],
                    "MaxReleaseStep": 1,
                    "MaxThrottleStep": 1,
                    "CdevCeiling": [0, 6, 6, 6, 6, 6, 6]
                },
                {
                    "CdevRequest": "thermal-cpufreq-1",
                    "CdevWeightForPID": [0.804, 0.804, 0.804, 0.804, 0.804, 0.804, 0.804],
                    "MaxReleaseStep": 1,
                    "MaxThrottleStep": 2,
                    "CdevCeiling": [0, 9, 9, 9, 9, 9, 9]
                },
                {
                    "CdevRequest": "thermal-cpufreq-2",
                    "CdevWeightForPID": [0.342, 0.342, 0.342, 0.342, 0.342, 0.342, 0.342],
                    "MaxReleaseStep": 1,
                    "MaxThrottleStep": 2,
                    "CdevCeiling": [0, 12, 12, 12, 12, 12, 12]
                }
            ],
            "Profile": [
                {
                    "Mode": "game",
                    "BindedCdevInfo": [
                        {
                           "CdevRequest": "thermal-cpufreq-0",
                           "MaxReleaseStep": 1,
                           "CdevCeiling": [0, 6, 6, 6, 6, 6, 6],
                           "Disabled": true
                        },
                        {
                           "CdevRequest": "thermal-cpufreq-1",
                           "MaxReleaseStep": 1,
                           "CdevCeiling": [0, 9, 9, 9, 9, 9, 9],
                           "Disabled": true
                        },
                        {
                           "CdevRequest": "thermal-cpufreq-2",
                           "MaxReleaseStep": 1,
                           "CdevCeiling": [0, 12, 12, 12, 12, 12, 12],
                           "Disabled": true
                        }
                    ]
                },
                {
                    "Mode": "camera",
                    "BindedCdevInfo": [
                        {
                           "CdevRequest": "thermal-cpufreq-0",
                           "MaxReleaseStep": 1,
                           "CdevCeiling": [0, 6, 6, 6, 6, 6, 6],
                           "Disabled": true
                        },
                        {
                           "CdevRequest": "thermal-cpufreq-1",
                           "MaxReleaseStep": 1,
                           "CdevCeiling": [0, 9, 9, 9, 9, 9, 9],
                           "Disabled": true
                        },
                        {
                           "CdevRequest": "thermal-cpufreq-2",
                           "MaxReleaseStep": 1,
                           "CdevCeiling": [0, 12, 12, 12, 12, 12, 12],
                           "Disabled": true
                        }
                    ]
                }
            ]
        },
        {
            "Name": "VIRTUAL-SKIN-CPU-HIGH",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "TriggerSensor": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "quiet_therm", "usb_pwr_therm"],
            "Formula": "MAXIMUM",
            "Combination": ["VIRTUAL-SKIN"],
            "Coefficient": [1.0],
            "HotThreshold": ["NaN", "NaN", 48.0, 52.0, "NaN", "NaN", "NaN"],
            "HotHysteresis": [0.0, 0.0, 1.9, 1.9, 0.0, 0.0, 0.0],
            "Multiplier": 0.001,
            "PollingDelay": 300000,
            "PassiveDelay": 7000,
            "PIDInfo": {
                "K_Po": ["NaN", "NaN", 400, "NaN", "NaN", "NaN", "NaN"],
                "K_Pu": ["NaN", "NaN", 400, "NaN", "NaN", "NaN", "NaN"],
                "K_I": ["NaN", "NaN", 5, "NaN", "NaN", "NaN", "NaN"],
                "K_D": ["NaN", "NaN", 0, "NaN", "NaN", "NaN", "NaN"],
                "I_Max": ["NaN", "NaN", 1000, "NaN", "NaN", "NaN", "NaN"],
                "S_Power": ["NaN", "NaN", 600, "NaN", "NaN", "NaN", "NaN"],
                "MinAllocPower": ["NaN", "NaN", 0, "NaN", "NaN", "NaN", "NaN"],
                "MaxAllocPower": ["NaN", "NaN", 1600, "NaN", "NaN", "NaN", "NaN"],
                "I_Cutoff": ["NaN", "NaN", 4, "NaN", "NaN", "NaN", "NaN"]
            },
            "BindedCdevInfo": [
                {
                    "CdevRequest": "thermal-cpufreq-0",
                    "CdevWeightForPID": [0.156, 0.156, 0.156, 0.156, 0.156, 0.156, 0.156],
                    "MaxReleaseStep": 1,
                    "MaxThrottleStep": 1,
                    "CdevCeiling": [0, 8, 8, 8, 8, 8, 8]
                },
                {
                    "CdevRequest": "thermal-cpufreq-1",
                    "CdevWeightForPID": [0.428, 0.428, 0.428, 0.428, 0.428, 0.428, 0.428],
                    "MaxReleaseStep": 1,
                    "MaxThrottleStep": 2,
                    "CdevCeiling": [0, 11, 11, 11, 11, 11, 11]
                },
                {
                    "CdevRequest": "thermal-cpufreq-2",
                    "CdevWeightForPID": [0.225, 0.225, 0.225, 0.225, 0.225, 0.225, 0.225],
                    "MaxReleaseStep": 1,
                    "MaxThrottleStep": 2,
                    "CdevCeiling": [0, 13, 13, 13, 13, 13, 13]
                }
            ],
            "Profile": [
                {
                    "Mode": "game",
                    "BindedCdevInfo": [
                        {
                           "CdevRequest": "thermal-cpufreq-0",
                           "MaxReleaseStep": 1,
                           "CdevCeiling": [0, 8, 8, 8, 8, 8, 8],
                           "Disabled": true
                        },
                        {
                           "CdevRequest": "thermal-cpufreq-1",
                           "MaxReleaseStep": 1,
                           "CdevCeiling": [0, 11, 11, 11, 11, 11, 11],
                           "Disabled": true
                        },
                        {
                           "CdevRequest": "thermal-cpufreq-2",
                           "MaxReleaseStep": 1,
                           "CdevCeiling": [0, 13, 13, 13, 13, 13, 13],
                           "Disabled": true
                        }
                    ]
                },
                {
                    "Mode": "camera",
                    "BindedCdevInfo": [
                        {
                           "CdevRequest": "thermal-cpufreq-0",
                           "CdevWeightForPID": [0.156, 0.156, 0.156, 0.156, 0.156, 0.156, 0.156],
                           "MaxReleaseStep": 1,
                           "MaxThrottleStep": 1,
                           "CdevCeiling": [0, 2, 6, 6, 6, 6, 6]
                        },
                        {
                           "CdevRequest": "thermal-cpufreq-1",
                           "CdevWeightForPID": [0.428, 0.428, 0.428, 0.428, 0.428, 0.428, 0.428],
                           "MaxReleaseStep": 1,
                           "MaxThrottleStep": 2,
                           "CdevCeiling": [0, 6, 9, 9, 9, 9, 9]
                        },
                        {
                           "CdevRequest": "thermal-cpufreq-2",
                           "CdevWeightForPID": [0.225, 0.225, 0.225, 0.225, 0.225, 0.225, 0.225],
                           "MaxReleaseStep": 1,
                           "MaxThrottleStep": 2,
                           "CdevCeiling": [0, 8, 12, 12, 12, 12, 12]
                        }
                    ]
                }
            ]
        },
        {
            "Name": "VIRTUAL-SKIN-SOC",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "TriggerSensor": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "quiet_therm", "usb_pwr_therm"],
            "Formula": "MAXIMUM",
            "Combination": ["VIRTUAL-SKIN"],
            "Coefficient": [1.0],
            "HotThreshold": ["NaN", "NaN", "NaN", "NaN", "NaN", 52.0, 55.0],
            "HotHysteresis": [0.0, 0.0, 0.0, 0.0, 0.0, 1.9, 1.9],
            "Multiplier": 0.001,
            "PollingDelay": 300000,
            "PassiveDelay": 7000,
            "PIDInfo": {
                "K_Po": ["NaN", "NaN", "NaN", 300, "NaN", "NaN", "NaN"],
                "K_Pu": ["NaN", "NaN", "NaN", 300, "NaN", "NaN", "NaN"],
                "K_I": ["NaN", "NaN", "NaN", 5, "NaN", "NaN", "NaN"],
                "K_D": ["NaN", "NaN", "NaN", 0, "NaN", "NaN", "NaN"],
                "I_Max": ["NaN", "NaN", "NaN", 2600, "NaN", "NaN", "NaN"],
                "S_Power": ["NaN", "NaN", "NaN", 800, "NaN", "NaN", "NaN"],
                "MinAllocPower": ["NaN", "NaN", "NaN", 800, "NaN", "NaN", "NaN"],
                "MaxAllocPower": ["NaN", "NaN", "NaN", 3900, "NaN", "NaN", "NaN"],
                "I_Cutoff": ["NaN", "NaN", "NaN", 8, "NaN", "NaN", "NaN"]
            },
            "BindedCdevInfo": [
                {
                    "CdevRequest": "thermal-cpufreq-0",
                    "CdevWeightForPID": [1, 1, 1, 1, 1, 1, 1],
                    "MaxReleaseStep": 1,
                    "MaxThrottleStep": 1,
                    "BindedPowerRail": "S4M_VDD_CPUCL0",
                    "CdevCeiling": [0, 8, 8, 8, 8, 9, 9],
                    "LimitInfo": [0, 0, 0, 0, 0, 9, 9]
                },
                {
                    "CdevRequest": "thermal-cpufreq-1",
                    "CdevWeightForPID": [1, 1, 1, 1, 1, 1, 1],
                    "MaxReleaseStep": 1,
                    "MaxThrottleStep": 2,
                    "BindedPowerRail": "S3M_VDD_CPUCL1",
                    "CdevCeiling": [0, 11, 11, 11, 11, 14, 14],
                    "LimitInfo": [0, 0, 0, 0, 0, 14, 14]
                },
                {
                    "CdevRequest": "thermal-cpufreq-2",
                    "CdevWeightForPID": [1, 1, 1, 1, 1, 1, 1],
                    "MaxReleaseStep": 1,
                    "MaxThrottleStep": 2,
                    "BindedPowerRail": "S2M_VDD_CPUCL2",
                    "CdevCeiling": [0, 13, 13, 13, 13, 14, 14],
                    "LimitInfo": [0, 0, 0, 0, 0, 14, 14]
                },
                {
                    "CdevRequest": "thermal-gpufreq-0",
                    "CdevWeightForPID": [1, 1, 1, 1, 1, 1, 1],
                    "MaxReleaseStep": 1,
                    "MaxThrottleStep": 1,
                    "BindedPowerRail": "S2S_VDD_G3D",
                    "CdevCeiling": [0, 8, 8, 8, 9, 11, 11],
                    "LimitInfo": [0, 0, 0, 0, 0, 11, 11]
                },
                {
                    "CdevRequest": "tpu_cooling",
                    "CdevWeightForPID": [1, 1, 1, 1, 1, 1, 1],
                    "MaxReleaseStep": 1,
                    "MaxThrottleStep": 1,
                    "BindedPowerRail": "S7M_VDD_TPU",
                    "CdevCeiling": [0, 7, 7, 7, 7, 7, 7],
                    "LimitInfo": [0, 0, 0, 0, 0, 7, 7]
                }
            ]
        },
        {
            "Name": "VIRTUAL-SKIN-GPU",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "TriggerSensor": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "quiet_therm", "usb_pwr_therm"],
            "Formula": "MAXIMUM",
            "Combination": ["VIRTUAL-SKIN"],
            "Coefficient": [1.0],
            "HotThreshold": ["NaN", "NaN", "NaN", 46.5, 52.0, "NaN", "NaN"],
            "HotHysteresis": [0.0, 0.0, 0.0, 1.4, 1.9, 0.0, 0.0],
            "Multiplier": 0.001,
            "PollingDelay": 300000,
            "PassiveDelay": 7000,
            "PIDInfo": {
                "K_Po": ["NaN", "NaN", 700, "NaN", "NaN", "NaN", "NaN"],
                "K_Pu": ["NaN", "NaN", 700, "NaN", "NaN", "NaN", "NaN"],
                "K_I": ["NaN", "NaN", 5, "NaN", "NaN", "NaN", "NaN"],
                "K_D": ["NaN", "NaN", 0, "NaN", "NaN", "NaN", "NaN"],
                "I_Max": ["NaN", "NaN", 1723, "NaN", "NaN", "NaN", "NaN"],
                "S_Power": ["NaN", "NaN", 473, "NaN", "NaN", "NaN", "NaN"],
                "MinAllocPower": ["NaN", "NaN", 0, "NaN", "NaN", "NaN", "NaN"],
                "MaxAllocPower": ["NaN", "NaN", 2500, "NaN", "NaN", "NaN", "NaN"],
                "I_Cutoff": ["NaN", "NaN", 4, "NaN", "NaN", "NaN", "NaN"]
            },
            "BindedCdevInfo": [
                {
                    "CdevRequest": "thermal-gpufreq-0",
                    "CdevWeightForPID": [1, 1, 1, 1, 1, 1, 1],
                    "CdevCeiling": [0, 8, 8, 9, 11, 11, 11]
                }
            ]
        },
        {
            "Name": "cellular-emergency",
            "Type": "POWER_AMPLIFIER",
            "VirtualSensor": true,
            "TriggerSensor": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "quiet_therm", "usb_pwr_therm"],
            "Formula": "MAXIMUM",
            "Combination": ["VIRTUAL-SKIN"],
            "Coefficient": [1.0],
            "HotThreshold": ["NaN", "NaN", "NaN", "NaN", "NaN", 54.0, "NaN"],
            "HotHysteresis": [0.0, 0.0, 0.0, 0.0, 0.0, 1.9, 0.0],
            "Multiplier": 0.001,
            "SendCallback": true,
            "PollingDelay": 300000,
            "PassiveDelay": 7000
        },
        {
            "Name": "VIRTUAL-SKIN-SPEAKER-SUB-0",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0, 0.14, 0, 0.15, 0, 0, 0, 0.88, 0],
            "Offset": -11750,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-SPEAKER-SUB-1",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0.01, 0.18, 0, 0, 0, 0.24, 0, 0.01, 0.35],
            "Offset": 3600,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-SPEAKER-SUB-2",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0, 0.01, 0, 0, 0.13, 0.31, 0.11, 0.18, 0.09],
            "Offset": 2140,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-SPEAKER",
            "Type": "UNKNOWN",
            "Version": "2.0",
            "VirtualSensor": true,
            "TriggerSensor": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "quiet_therm", "usb_pwr_therm"],
            "Formula": "MAXIMUM",
            "Combination": ["VIRTUAL-SKIN-SPEAKER-SUB-0", "VIRTUAL-SKIN-SPEAKER-SUB-1", "VIRTUAL-SKIN-SPEAKER-SUB-2"],
            "Coefficient": [1, 1, 1],
            "HotThreshold": ["NaN", 37.0, "NaN", "NaN", "NaN", "NaN", "NaN"],
            "HotHysteresis": [0.0, 1.9, 0.0, 0.0, 0.0, 0.0, 0.0],
            "Multiplier": 0.001,
            "SendCallback": true,
            "PollingDelay": 60000,
            "PassiveDelay": 7000
        },
        {
            "Name": "VIRTUAL-SKIN-CHARGE-SUB-0",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0.04, 0.16, 0.19, 0.16, 0.17, 0, 0.01, 0.24, 0],
            "Offset": -820,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-CHARGE-SUB-1",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0.02, 0.01, 0.04, 0.04, 0.4, 0.14, 0.1, 0.02, 0.12],
            "Offset": 1840,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-CHARGE-SUB-2",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0.18, 0.1, 0.15, 0.13, 0.22, 0.16, 0.02, 0.04, 0.01],
            "Offset": -2810,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-CHARGE-SUB-3",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0.1, 0.16, 0.11, 0.19, 0.26, 0, 0, 0.11, 0],
            "Offset": 1140,
            "Multiplier": 0.001
        },
        {
            "Name": "thb_hda",
            "Type": "UNKNOWN",
            "Multiplier": 1
        },
        {
            "Name": "WLC_CHECK",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "COUNT_THRESHOLD",
            "Combination": ["thb_hda", "thb_hda"],
            "Coefficient": [1, -51],
            "Multiplier": 1
        },
        {
            "Name": "NO_WLC",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "COUNT_THRESHOLD",
            "Combination": ["WLC_CHECK"],
            "Coefficient": [-2],
            "Multiplier": 1
        },
        {
            "Name": "VIRTUAL-SKIN-CHARGE",
            "Type": "UNKNOWN",
            "Version": "4.0",
            "VirtualSensor": true,
            "Formula": "MAXIMUM",
            "Combination": ["VIRTUAL-SKIN-CHARGE-SUB-0", "VIRTUAL-SKIN-CHARGE-SUB-1", "VIRTUAL-SKIN-CHARGE-SUB-2", "VIRTUAL-SKIN-CHARGE-SUB-3"],
            "Coefficient": [1.0, 1.0, 1.0, 1.0],
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-CHARGE-WIRED",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "TriggerSensor": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "quiet_therm", "usb_pwr_therm"],
            "Formula": "WEIGHTED_AVG",
            "Combination": ["VIRTUAL-SKIN-CHARGE"],
            "Coefficient": ["NO_WLC"],
            "CoefficientType": ["SENSOR"],
            "HotThreshold": ["NaN", "NaN", "NaN", "NaN", 45.0, 47.0, 55.0],
            "HotHysteresis": [0.0, 0.0, 0.0, 0.0, 3.9, 1.9, 1.9],
            "Multiplier": 0.001,
            "PollingDelay": 60000,
            "PassiveDelay": 7000,
            "PIDInfo": {
                "K_Po": ["NaN", "NaN", 119, "NaN", "NaN", "NaN", "NaN"],
                "K_Pu": ["NaN", "NaN", 119, "NaN", "NaN", "NaN", "NaN"],
                "K_I": ["NaN", "NaN", 25, "NaN", "NaN", "NaN", "NaN"],
                "K_D": ["NaN", "NaN", 0, "NaN", "NaN", "NaN", "NaN"],
                "I_Max": ["NaN", "NaN", 1302, "NaN", "NaN", "NaN", "NaN"],
                "S_Power": ["NaN", "NaN", 2527, "NaN", "NaN", "NaN", "NaN"],
                "MinAllocPower": ["NaN", "NaN", 0, "NaN", "NaN", "NaN", "NaN"],
                "MaxAllocPower": ["NaN", "NaN", 6219, "NaN", "NaN", "NaN", "NaN"],
                "I_Cutoff": ["NaN", "NaN", 6, "NaN", "NaN", "NaN", "NaN"],
                "I_Default": 1302
            },
            "ExcludedPowerInfo": [
                {
                    "PowerRail": "PARTIAL_SYSTEM_POWER",
                    "PowerWeight": [0.12, 0.12, 0.06, 0.06, 0.24, 0.24, 0.24]
                }
            ],
            "BindedCdevInfo": [
                {
                    "CdevRequest": "chg_mdis",
                    "CdevWeightForPID": [1, 1, 1, 1, 1, 1, 1],
                    "MaxReleaseStep": 1,
                    "MaxThrottleStep": 1,
                    "CdevCeiling": [0, 25, 25, 25, 26, 26, 26],
                    "LimitInfo": [0, 0, 1, 1, 1, 26, 26]
                }
            ]
        },
        {
            "Name": "VIRTUAL-SKIN-CHARGE-PERSIST",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "TriggerSensor": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "quiet_therm", "usb_pwr_therm"],
            "Formula": "MAXIMUM",
            "Combination": ["VIRTUAL-SKIN-CHARGE"],
            "Coefficient": [1.0],
            "HotThreshold": ["NaN", "NaN", "NaN", 45.0, 47.0, 51.0, 55.0],
            "HotHysteresis": [0.0, 0.0, 0.0, 3.9, 1.9, 1.9, 1.9],
            "Multiplier": 0.001,
            "PollingDelay": 60000,
            "PassiveDelay": 7000,
            "PIDInfo": {
                "K_Po": ["NaN", "NaN", 213, "NaN", "NaN", "NaN", "NaN"],
                "K_Pu": ["NaN", "NaN", 213, "NaN", "NaN", "NaN", "NaN"],
                "K_I": ["NaN", "NaN", 27, "NaN", "NaN", "NaN", "NaN"],
                "K_D": ["NaN", "NaN", 0, "NaN", "NaN", "NaN", "NaN"],
                "I_Max": ["NaN", "NaN", 1383, "NaN", "NaN", "NaN", "NaN"],
                "S_Power": ["NaN", "NaN", 2383, "NaN", "NaN", "NaN", "NaN"],
                "MinAllocPower": ["NaN", "NaN", 0, "NaN", "NaN", "NaN", "NaN"],
                "MaxAllocPower": ["NaN", "NaN", 8022, "NaN", "NaN", "NaN", "NaN"],
                "I_Cutoff": ["NaN", "NaN", 8, "NaN", "NaN", "NaN", "NaN"],
                "I_Default": 1383
            },
            "ExcludedPowerInfo": [
                {
                    "PowerRail": "PARTIAL_SYSTEM_POWER",
                    "PowerWeight": [0.21, 0.21, 0.21, 0.21, 0.42, 0.42, 0.42]
                }
            ],
            "BindedCdevInfo": [
                {
                    "CdevRequest": "chg_mdis",
                    "CdevWeightForPID": [1, 1, 1, 1, 1, 1, 1],
                    "MaxReleaseStep": 1,
                    "MaxThrottleStep": 1,
                    "CdevCeiling": [0, 25, 25, 26, 26, 26, 26],
                    "LimitInfo": [0, 0, 1, 1, 26, 26, 26]
                }
            ]
        },
        {
            "Name": "VIRTUAL-SKIN-FRONT-SUB-0",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0.04, 0.03, 0.1, 0.05, 0.35, 0.3, 0, 0, 0.04],
            "Offset": 1850,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-FRONT-SUB-1",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0, 0, 0.35, 0.22, 0.22, 0.07, 0.03, 0, 0],
            "Offset": -560,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-FRONT-SUB-2",
            "Type": "UNKNOWN",
            "Hidden": true,
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "battery", "neutral_therm", "quiet_therm", "usb_pwr_therm"],
            "Coefficient": [0.05, 0.13, 0.12, 0.07, 0.37, 0.06, 0.01, 0.01, 0],
            "Offset": 5070,
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-SKIN-FRONT",
            "Type": "UNKNOWN",
            "Version": "1.0",
            "VirtualSensor": true,
            "TriggerSensor": ["north_therm", "cam_therm", "soc_therm", "charge_therm", "disp_therm", "quiet_therm", "usb_pwr_therm"],
            "Formula": "MAXIMUM",
            "Combination": ["VIRTUAL-SKIN-FRONT-SUB-0", "VIRTUAL-SKIN-FRONT-SUB-1", "VIRTUAL-SKIN-FRONT-SUB-2"],
            "Coefficient": [1, 1, 1],
            "Multiplier": 0.001
        },
        {
            "Name": "USB-MINUS-NEUTRAL",
            "Type": "UNKNOWN",
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["usb_pwr_therm", "neutral_therm"],
            "Coefficient": [1.0, -1.0],
            "Multiplier": 0.001
        },
        {
            "Name": "USB-MINUS-QUIET",
            "Type": "UNKNOWN",
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["usb_pwr_therm", "quiet_therm"],
            "Coefficient": [1.0, -1.0],
            "Multiplier": 0.001
        },
        {
            "Name": "USB_QUIET_RFFE",
            "Type": "UNKNOWN",
            "VirtualSensor": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["USB-MINUS-QUIET", "VSYS_PWR_RFFE"],
            "CombinationType": ["SENSOR", "ODPM"],
            "Coefficient": [1, -6],
            "Multiplier": 0.001
        },
        {
            "Name": "VIRTUAL-USB-THROTTLING-SUB0",
            "Type": "UNKNOWN",
            "VirtualSensor": true,
            "Formula": "COUNT_THRESHOLD",
            "Combination": ["USB-MINUS-NEUTRAL", "USB_QUIET_RFFE"],
            "Coefficient": [10000, 4000],
            "Multiplier": 1
        },
        {
            "Name": "VIRTUAL-USB-THROTTLING",
            "Type": "USB_PORT",
            "VirtualSensor": true,
            "Formula": "COUNT_THRESHOLD",
            "TriggerSensor": "usb_pwr_therm",
            "Combination": ["usb_pwr_therm", "USB-MINUS-NEUTRAL", "USB-MINUS-QUIET", "VIRTUAL-USB-THROTTLING-SUB0"],
            "Coefficient": [46000, 0, 0, 1],
            "HotThreshold": ["NaN", "NaN", "NaN", "NaN", "5.0", "NaN", "NaN"],
            "BindedCdevInfo": [
                {
                    "CdevRequest": "usbc-port",
                    "LimitInfo": [0, 0, 0, 0, 1, 1, 1]
                }
            ],
            "Multiplier": 1,
            "PollingDelay": 300000,
            "PassiveDelay": 7000
        },
        {
            "Name": "VIRTUAL-USB-UI-SUB0",
            "Type": "UNKNOWN",
            "VirtualSensor": true,
            "Formula": "COUNT_THRESHOLD",
            "Combination": ["USB-MINUS-NEUTRAL", "USB_QUIET_RFFE"],
            "Coefficient": [11000, 5000],
            "Multiplier": 1
        },
        {
            "Name": "VIRTUAL-USB-UI",
            "Type": "USB_PORT",
            "VirtualSensor": true,
            "Formula": "COUNT_THRESHOLD",
            "TriggerSensor": "usb_pwr_therm",
            "Combination": ["usb_pwr_therm", "USB-MINUS-NEUTRAL", "USB-MINUS-QUIET", "VIRTUAL-USB-UI-SUB0"],
            "Coefficient": [48000, 0, 0, 1],
            "HotThreshold": ["NaN", "NaN", "NaN", "NaN", "NaN", "4.0", "NaN"],
            "Multiplier": 1,
            "PollingDelay": 300000,
            "PassiveDelay": 7000,
            "SendCallback": true
        },
        {
            "Name": "LITTLE",
            "Type": "CPU",
            "HotThreshold": ["NaN", "NaN", "NaN", "NaN", "NaN", "NaN", "NaN"],
            "Multiplier": 0.001
        },
        {
            "Name": "MID",
            "Type": "CPU",
            "HotThreshold": ["NaN", "NaN", "NaN", "NaN", "NaN", "NaN", "NaN"],
            "Multiplier": 0.001
        },
        {
            "Name": "BIG",
            "Type": "CPU",
            "HotThreshold": ["NaN", "NaN", "NaN", "NaN", "NaN", "NaN", "NaN"],
            "Multiplier": 0.001
        },
        {
            "Name": "G3D",
            "Type": "GPU",
            "HotThreshold": ["NaN", "NaN", "NaN", "NaN", "NaN", "NaN", "NaN"],
            "Multiplier": 0.001
        },
        {
            "Name": "TPU",
            "Type": "NPU",
            "HotThreshold": ["NaN", "NaN", "NaN", "NaN", "NaN", "NaN", "NaN"],
            "Multiplier": 0.001
        }
    ],
    "CoolingDevices": [
        {
            "Name": "thermal-cpufreq-0",
            "Type": "CPU",
            "WritePath": "/dev/thermal/cdev-by-name/thermal-cpufreq-0/user_vote"
        },
        {
            "Name": "thermal-cpufreq-1",
            "Type": "CPU",
            "WritePath": "/dev/thermal/cdev-by-name/thermal-cpufreq-1/user_vote"
        },
        {
            "Name": "thermal-cpufreq-2",
            "Type": "CPU",
            "WritePath": "/dev/thermal/cdev-by-name/thermal-cpufreq-2/user_vote"
        },
        {
            "Name": "thermal-gpufreq-0",
            "Type": "GPU",
            "WritePath": "/dev/thermal/cdev-by-name/thermal-gpufreq-0/user_vote"
        },
        {
            "Name": "chg_mdis",
            "Type": "BATTERY"
        },
        {
            "Name": "usbc-port",
            "Type": "BATTERY"
        },
        {
            "Name": "tpu_cooling",
            "Type": "NPU",
            "WritePath": "/dev/thermal/cdev-by-name/tpu_cooling/user_vote"
        },
        {
            "Name": "gxp-cooling",
            "Type": "NPU",
            "WritePath": "/dev/thermal/cdev-by-name/gxp-cooling/user_vote"
        }
    ],
    "PowerRails": [
        {
            "Name": "VSYS_PWR_RFFE",
            "PowerSampleDelay": 7000,
            "PowerSampleCount": 2
        },
        {
            "Name": "S2M_VDD_CPUCL2",
            "PowerSampleDelay": 7000,
            "PowerSampleCount": 1
        },
        {
            "Name": "S3M_VDD_CPUCL1",
            "PowerSampleDelay": 7000,
            "PowerSampleCount": 1
        },
        {
            "Name": "S4M_VDD_CPUCL0",
            "PowerSampleDelay": 7000,
            "PowerSampleCount": 1
        },
        {
            "Name": "S2S_VDD_G3D",
            "PowerSampleDelay": 7000,
            "PowerSampleCount": 1
        },
        {
            "Name": "S7M_VDD_TPU",
            "PowerSampleDelay": 7000,
            "PowerSampleCount": 1
        },
        {
            "Name": "PARTIAL_SYSTEM_POWER",
            "VirtualRails": true,
            "Formula": "WEIGHTED_AVG",
            "Combination": ["S1S_VDD_CAM", "S2S_VDD_G3D", "S4S_VDD2H_MEM", "S5S_VDDQ_MEM", "S8S_VDD_G3D_L2", "S9S_VDD_AOC", "L2S_PLL_MIPI_UFS", "L21S_VDD2L_MEM", "VSYS_PWR_DISPLAY", "VSYS_PWR_WLAN_BT", "S1M_VDD_MIF", "S2M_VDD_CPUCL2", "S3M_VDD_CPUCL1", "S4M_VDD_CPUCL0", "S5M_VDD_INT", "S6M_LLDO1", "S7M_VDD_TPU", "S8M_LLDO2", "VSYS_PWR_MODEM", "VSYS_PWR_RFFE"],
            "Coefficient": [1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0],
            "PowerSampleDelay": 7000,
            "PowerSampleCount": 5
        }
    ],
    "Stats": {
        "Sensors": {
            "RecordWithDefaultThreshold": ["VIRTUAL-SKIN", "VIRTUAL-SKIN-CHARGE"],
            "RecordWithThreshold": [
                {
                    "Name": "VIRTUAL-BTS-WINDOW-PARTIAL",
                    "Thresholds": [31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51]
                },
                {
                    "Name": "VIRTUAL-SKIN-SPEAKER",
                    "Thresholds": [31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51]
                },
                {
                    "Name": "VIRTUAL-SKIN",
                    "Thresholds": [31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51]
                },
                {
                    "Name": "VIRTUAL-SKIN-SUB-0",
                    "Thresholds": [31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51]
                },
                {
                    "Name": "VIRTUAL-SKIN-SUB-1",
                    "Thresholds": [31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51]
                },
                {
                    "Name": "VIRTUAL-SKIN-SUB-2",
                    "Thresholds": [31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51]
                },
                {
                    "Name": "VIRTUAL-SKIN-SUB-3",
                    "Thresholds": [31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51]
                },
                {
                    "Name": "VIRTUAL-SKIN-SUB-4",
                    "Thresholds": [31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51]
                },
                {
                    "Name": "VIRTUAL-SKIN-SUB-5",
                    "Thresholds": [31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51]
                },
                {
                    "Name": "VIRTUAL-SKIN-SUB-6",
                    "Thresholds": [31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51]
                },
                {
                    "Name": "VIRTUAL-SKIN-SUB-7",
                    "Thresholds": [31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51]
                },
                {
                    "Name": "VIRTUAL-SKIN-SUB-8",
                    "Thresholds": [31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51]
                },
                {
                    "Name": "VIRTUAL-SKIN-SUB-9",
                    "Thresholds": [31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51]
                },
                {
                    "Name": "VIRTUAL-SKIN-SUB-10",
                    "Thresholds": [31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51]
                },
                {
                    "Name": "VIRTUAL-SKIN-CHARGE",
                    "Thresholds": [31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51]
                },
                {
                    "Name": "VIRTUAL-USB-THROTTLING",
                    "Thresholds": [3.0]
                }
            ],
            "Abnormality": {
                "Outlier": {
                    "Configs": [
                        {
                            "Monitor": [
                                "VIRTUAL-SKIN",
                                "VIRTUAL-SKIN-SUB-0",
                                "VIRTUAL-SKIN-SUB-1",
                                "VIRTUAL-SKIN-SUB-2",
                                "VIRTUAL-SKIN-SUB-3",
                                "VIRTUAL-SKIN-SUB-4",
                                "VIRTUAL-SKIN-SUB-5",
                                "VIRTUAL-SKIN-SUB-6",
                                "VIRTUAL-SKIN-SUB-7",
                                "VIRTUAL-SKIN-SUB-8",
                                "VIRTUAL-SKIN-SUB-9",
                                "VIRTUAL-SKIN-SUB-10"
                            ],
                            "TempRange": [0.0, 55.0]
                        }
                    ]
                },
                "Stuck": {
                    "Configs": [
                        {
                            "Monitor": [
                                "VIRTUAL-SKIN",
                                "VIRTUAL-SKIN-SUB-0",
                                "VIRTUAL-SKIN-SUB-1",
                                "VIRTUAL-SKIN-SUB-2",
                                "VIRTUAL-SKIN-SUB-3",
                                "VIRTUAL-SKIN-SUB-4",
                                "VIRTUAL-SKIN-SUB-5",
                                "VIRTUAL-SKIN-SUB-6",
                                "VIRTUAL-SKIN-SUB-7",
                                "VIRTUAL-SKIN-SUB-8",
                                "VIRTUAL-SKIN-SUB-9",
                                "VIRTUAL-SKIN-SUB-10",
                                "VIRTUAL-SKIN-SPEAKER",
                                "VIRTUAL-SKIN-SPEAKER-SUB-0",
                                "VIRTUAL-SKIN-SPEAKER-SUB-1",
                                "VIRTUAL-SKIN-SPEAKER-SUB-2",
                                "VIRTUAL-SKIN-FRONT",
                                "VIRTUAL-SKIN-FRONT-SUB-0",
                                "VIRTUAL-SKIN-FRONT-SUB-1",
                                "VIRTUAL-SKIN-FRONT-SUB-2"
                            ],
                            "TempStuck": {
                                "MinPollingCount": 8,
                                "MinStuckDuration": 120000
                            }
                        }
                    ]
                }
            }
        },
        "CoolingDevices": {
            "RecordVotePerSensor": {
                "DefaultThresholdEnableAll": true
            }
        }
    }
}
