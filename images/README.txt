This folder contains visual assets used in the Intel Unnati DL Streamer project documentation:

1. Pipeline Flowchart – Visual representation of the DL Streamer pipeline architecture showing stream decode, inference, and sink modules.  
   

2. Output Snapshot – A sample output from a live camera feed showing bounding boxes for detected people, vehicles, and bikes.  
   [Attach: output_snapshot.png]  ← (From "Output Snapshot" section)

3. Performance Comparison Chart – Line graph comparing CPU vs GPU average FPS across increasing stream counts (1 to 5).  
   [Attach: performance_chart.png]  ← (From "Performance Comparison Chart" section)

4. FPS vs Stream Count – Bar chart showing total cumulative FPS for CPU and GPU as stream count increases.  
   [Attach: throughput_bar_chart.png]  ← (From "FPS vs Stream Count" section)

5. Bottleneck Source Breakdown – Pie chart illustrating IO, inference, rendering, and other contributors to the GPU bottleneck at 5 streams.  
   [Attach: bottleneck_pie.png]  ← (From "Bottleneck Source Breakdown" section)

6. Resource Utilization Trends – Line chart showing CPU and GPU usage percentage rising with stream count.  
   [Attach: resource_utilization_chart.png]  ← (From "Resource Utilization Trends" addition)

7. Latency Breakdown – Pie chart showing decode, inference, and post-processing time percentages per frame on GPU at 4 streams.  
   [Attach: latency_breakdown_pie.png]  ← (From "Latency Breakdown" optional section)

All charts were generated using Python’s `matplotlib` library, based on experimental benchmarks run on Intel® Core™ i7 CPU with integrated Iris Xe graphics.
