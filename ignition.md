See https://www.msextra.com/forums/viewtopic.php?t=76799

For those who might need this in the future...

The Bosch 0.227.100.124 is commonly called the "Bosch 124", but Bosch refers to it as the "BIM 027". If you do internet searches for BIM 027, you'll find more information than by looking for Bosch 124.

From the following page, we know that the trigger should be set to "Going high": http://www.megamanual.com/ms2/Bosch_124.htm

But, we need to know the correct maximum current. From the below documents, it looks like it supports 10 amps, but 8.5 amps would be best.

This ignition module monitors the coil amps and will regulate the output to maintain the modules rated amps. This is good for the coil, but could overheat the ignition module if your dwell is set too long. A proper heat sink with heat sink compound between the module and sink are necessary if you plan to let the ignition module manage the current. This works just fine in Porsches where their OEM ECU's have longer dwell times and let the module manage the current. They have large heat sinks to keep the ignition modules cool.

When you look in the supporting documents, you'll see that there is a "Type of Trigger" column. And the BIM 027 is a Hall Effect trigger. Which is ideal for the Megasquirt ECU's ignition output. Combined with the modules current monitoring, it makes it very easy to get maximum current without overheating the coils. You can set a relatively high dwell time and a reasonable spark duration (~1ms) and let the module handle the rest. However, it would work better to use a dwell table and use lower dwell times for light load and higher dwell times for higher load.

By combining the specifications for the ignition module's maximum current with a coil's calculated dwell time (plus loom resistance), you can come up with a very good first guess at dwell times.