About: GridPulser70127420_0_MATLAB (formerly known as something like filament_PS_app_20_04_24...blahblah.mlapp) is a MATLAB app written as user-facing control software to interface with the DNDO gun pulser (701-274-20 R0). It handles communication over serial UART. It manages on/off states, set points, status readback, and has basic fault detection.

The UserVariant version is for compilation via MATLAB Compiler into a stand-alone executable, and removes/hides unimplemented features so as to not confuse the user.

Original author: M. Kemp

Changelog 
2023-01-20 - v1.1.0 - A. S. NGUYEN

	Added soft-start function & bypass control.
	- Top-right switch controls whether the 2 ohm resistor at the filament supply output is bypassed or not. Bypass is left off by default on program start-up. Must be left off during filament cold-start to limit inrush current to the filament.
		- Filament voltage control is disabled while bypass is off to limit power dissipation. When bypass is disabled from an on-state, filament set point will be reset to minimum.
	- On back-end, an extra serial character is being sent to grid pulser uC to communicate bypass setting.

2022-03-15 - V1.0 - A. S. Nguyen
	- Renamed program to GridPulser70127420_0_MATLABv1.mlapp for clarity.