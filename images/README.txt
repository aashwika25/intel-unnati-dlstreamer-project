This folder contains visual assets used in the Intel Unnati DL Streamer project documentation:

1. Pipeline Flowchart – Visual representation of the DL Streamer pipeline architecture showing stream decode, inference, and sink modules.  
2. Intel DL streamer pipeline framework - Enables high-performance real-time video analytics by building modular, GStreamer-based pipelines optimized for Intel CPUs and GPUs.
3. Output Snapshot – A sample output from a live camera feed showing bounding boxes for detected people..
4. Performance Comparison Chart – Line graph comparing CPU vs GPU average FPS across increasing stream counts (1 to 5).  
5. FPS vs Stream Count – Bar chart showing total cumulative FPS for CPU and GPU as stream count increases.  
6. Bottleneck Source Breakdown – Pie chart illustrating IO, inference, rendering, and other contributors to the GPU bottleneck at 5 streams. 
7. Resource Utilization Trends – Line chart showing CPU and GPU usage percentage rising with stream count.  
8. Latency Breakdown – Pie chart showing decode, inference, and post-processing time percentages per frame on GPU at 4 streams. 

Charts were generated using Python’s `matplotlib` library, based on experimental benchmarks run on Intel® Core™ i7 CPU with integrated Iris Xe graphics.
