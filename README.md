# comet-cooling
This repository contains codes for cooling methods 
got to the repo link "https://github.com/marg-tools/CoMeT.git" and clone the CoMeT-main folder in to your local system
Extract the contents of CoMeT-main.zip and make a copy of hotspot_tool folder and name it hotspot_tool3.

first of all run the command "make" inside the hotspot_tool and hotspot_tool3 folders.

Delete the file temperature.c from the folder hotspot_tool3 and replace it with the file "temperature.c from this repository.

Go to the CoMeT-main/config/hotspot/2_5D and copy all the content into the hotspot_tool an dhotspot_tool3 folder.

run the notebook oldarch file generator to generate sample trace files within  designated folders. After creating the traces, got to the folder containing the traces named "mycsv2_5.trace" and run the following command.


"../../../hotspot -c ../../../stack_hotspot.config -p mycsv2_5.trace -o temperature_mem.trace -model_secondary 1 -model_type grid -steady_file steady_temperature_mem.log -all_transient_file all_transient_mem.init -grid_steady_file grid_steady_mem.log -steady_state_print_disable 1 -l 1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1, -type 2.5D -sampling_intvl 0.001 -grid_layer_file ../../../stack.lcf -detailed_3D on -init_file ../../../stack.init"


## for simulating the real trace files

Extract the contents of zip file TraceBasedDTM-main.zip. Go to TraceBasedDTM-main/Traces_1.8_2.4_3.0_3.6/WorkArea_3.6 and find the various benchmark folders containing the traces. Modify them according to the architecture and copy them into oldarch folder in hotspot_tool and hotspot_tool3. 


The files cooling_2.5D_realtime_HMC and cooling_realtime_2.5D_realtime_HBM are the cpdes that implement our cooling strategy.

