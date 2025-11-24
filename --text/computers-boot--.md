
# specific - Throttlestop guide

Use at your own risk

Throttlestop is generally used to undervolt the cpu on locked desktops or laptops. It is a very powerful tool capable of increasing cpu performance when used correctly. If your cpu temperatures typically exceed 60c while playing, I would recommend only undervolting.

My current recommendation is to use Throttlestop v9.0.

## Main Screen

Set Clock Mod to 100% and Set Multiplier to max value. The Multiplier is what multiplies the base clock of the cpu, typically 100. Untick Power Saver, BD Prochot, Speedstep, and C1E.

Click Stop Data on the Main Screen! You'll need to do this every time you open Throttlestop. There's no need for it to track temperatures unless you're using it for monitoring purposes.

## FIVR

Lock Non-Turbo Ratio to the highest possible value. Simply typing 99 in the box will set it to max. Set Turbo Limits to max. Hold the right arrow on the BOTTOM cpu core and the rest should automatically follow. Check Disable and Lock Turbo Power Limits. Set the Cache Min/Max to the highest available value. Skip undervolting for now.

## TPL

Set Short/Long Power to max value (just type 9999). Drag Turbo Time Limit slider to max value. Tick Speed Shift and set Min/Max to 255. Tick start SpeedShift when Throttlestop starts. This will lock the CPU to max speed. Untick PP0 Power Limit (this setting will cause temperature increases. Highly recommended to avoid if you have high temps already). Tick Intel Power Balance and set CPU to 31 and GPU to 0 (unless you use the iGPU). This gives priority to the CPU over the GPU when the TDP limit is met.

## C1

Click the arrow on the right to bring up the C-States control pane. Set Request to C1 and untick all the boxes below. Click Apply and then Ok.

## Options

You can force Timer Resolution via Throttlestop. Set AC Timer Res to 0 and the Timer Res value will go to 0.5

## Undervolting

THERE IS NO "BEST"! Every CPU is different, and depending on your chip, you may get a better or worse undervolt than someone with the same CPU as you. This requires TESTING! Go back to the FIVR window, and adjust CPU Core and Cache. To unlock the screen, tick Unlock Adjustable Voltage. My advice is to start with an Adjustable voltage and adjust the Offset, going as low as possible before you experience freezing or loss of performance. After reaching your limit, monitor your Voltage under load. Use a stress test for this. You'll need to press Start Data on the main screen if you previously stopped it. Find the max value your CPU hits, and then change the voltage type to Static for both core and cache. Set the Voltage slider equivalent to the max voltage your cpu hits, and set to Offset to 0. In my experience, this provides a slight performance increase over Adaptive voltage when properly used, and can even shave off a few degrees under load.
