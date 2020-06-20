**Soft Real-time System with Simulink and Arduino**

The aim here is to build a (low-cost) soft real-time system by using Arduino as an IO server (data acquisition device). The software that we use is MATLAB Simulink 2018b. The developed real-time system will be used for controlling low dynamic systems, such as thermal and fluidic systems, while performing data acquisition process. The real-time system is expected to run at a 10 Hz of sampling rate, with the capability to log data to its hard drive at each iteration, thus, the resulting data is equally timed.

**Steps to do:**


Here, we assume you have successfully installed the Simulink Support Packages for Arduino. After running the MATLAB, go to system monitor (in Linux system) or task manager (in Windows system), and set the MATLAB priority to be the highest. Sort the process lists based on the priority and make sure that MATLAB has the highest priority. You must set priority of other processes to normal if they consume rather high processor power.

![alt text](https://github.com/auralius/soft-rt-simulink-arduino/blob/master/figures/fig1.png?raw=true)

*Figure 1: In Linux, process priority value is called __"nice value"__: the lower the nice value is, the higher the priority is. -20 is the highest prority in a Linux system. In a Windows system, the highest priority is labelled as __“realtime”__.*

Next, run the provided MATLAB Simulink file. A Simulink file named: __Template10HzUno.slx__ is provided. Use this file as a template to build your project (see Figure 2). You can adapt the configuration to suit your hardware selections. However, before continuing with your project, you should perform jitter test.  Run the Simulink file for at least 60 seconds and then use the m-file named: __jitter_tes_result.m__ to plot the result. Your system should have jitter less than 1% (see Figure 3).

![alt text](https://github.com/auralius/soft-rt-simulink-arduino/blob/master/figures/fig2.png?raw=true)
 
*Figure 2: Run this model for about 60 seconds. A file named loggedtime.mat is generated.*

![alt text](https://github.com/auralius/soft-rt-simulink-arduino/blob/master/figures/fig3.png?raw=true)

*Figure 3: Jitter result from jitter_test_result.m showing jitter of less than one percent.*


manurunga@yandex.com
