# ece8893-lab2--tiling-based-convolution-in-hls-solved
**TO GET THIS SOLUTION VISIT:** [ECE8893 Lab2- Tiling-based Convolution in HLS Solved](https://www.ankitcodinghub.com/product/ece8893-parallel-programming-for-fpgas-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;113724&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;ECE8893 Lab2- Tiling-based Convolution in HLS Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Problem Statement:

Implement the following convolutional layer (sample taken from the ResNet50 Model, refer [1]): Kernel Size – 3×3 Filter Size – 64 Input Feature Map – (64, 184, 320) Stride – 1 Padding – 1 Output Feature Map – (64, 184, 320) For reference on

Convolutional Layer in deep learning, refer [2]

Part A – C model implementation (30% Weightage):

Implement the convolution at the software-level (no hardware level features). This is to ensure functional correctness and to act as a debugging reference for implementing tiling-based convolution.

Your code must pass the testbench.

Note: Here, handling the border pixels correctly for padding is very important ( Refer to [2] ) as you would extend this concept for the hardware implementation in the next part.

Part B – Unoptimized but synthesizable tiled-convolution in HLS (30% Weightage):

Implement the convolution layer as a synthesizable tiled convolution (Refer [1]). a) Implement the convolution for a single tile in conv_3x3.cpp

b) Implement the complete tiled convolution in tiled_conv.cpp There are functions available in utils.cpp to assist with this.

Part C – Optimized and (synthesizable) tiled-convolution (40% Weightage):

Apply suitable HLS optimizations to optimize the latency while keeping resource utilization under 100%. The target is to achieve an overall latency of &lt; 740ms (speedup of at least 30x)

You need to estimate how much of a speedup your optimized convolution code should hit to meet this overall speedup. Amdahlâ€™s law in action!

Note: This is the most important part of this lab.

Bonus!

Up for the challenge?

– If the overall latency achieved is less than 600ms, 1 extra point.

– If the overall latency achieved is less than 450ms, total 2 extra points.

– To add a little spice to this, if your latency is among the Top 5 in the class, you get 1 additional point.

– If you’re in the Top 10 but not in the Top 5, you get 0.5 additional point. (i.e. you can score a maximum of 13 points in this lab!!)

Sugested sequence of code development:

The software-level C model

Tiled implementation: tiled_conv + conv_3x3 together

Optimize conv_3x3

Optimize tiled_conv

Before running synthesis, always simulate the whole layer first, make sure it passes, then synthesize

References:

[1] Lab 2 Reference Article:

https://sharc-knowledgebase.netlify.app/articles/cnn/tiling-based_convolution_for_hls/ [2] Conv Layer Reference:

https://stanford.edu/~shervine/teaching/cs-230/cheatsheet-convolutional-neural-networks

Some constraints to follow:

For Part B &amp; Part C, buffer dimensions should not be changed except for minor increments in input buffer height and width for handling the border pixels.

Tile slice or Tile cube dimensions should not be changed.

Input or output feature map dimensions should not be changed.

Clock period should be fixed at 10ns.

* The data precision should not be changed for latency calculation (can be explored).

Targets:

Part A: Functional correctness. Test bench must pass.

Part B: Latency of ~22.2 seconds for the entire layer (This is just a reference for the kind of latency expected and not a target as such).

Part C: Latency &lt; 740 ms for the entire layer(i.e. 30x speedup). Resource utilization to be under 100% in both Part B and Part C.

What to submit:

Part A – src/model_conv.cpp.

Part B. a) src/utils.cpp.

Part B. b) src/conv_3x3.cpp.

Part B. c) src/tiled_conv.cpp.

Part C. a) src/utils.cpp.

Part C. b) optimized src/conv_3x3.cpp. HLS report.

Part C. c) optimized src/tiled_conv.cpp. HLS report. Part C. d) src/conv.h.

* Lab Report

For Part A, upload your model_conv.cpp For Part B, upload Part_B.tar.gz which contains PartB. a), b) and c) without optimizations. For Part C, upload Part_C.tar.gz which contains PartC. a), b), c) and d) with optimizations &amp; pragmas Reference Data:

* Input to the convolution:

bin/conv_layer_input_feature_map.bin

* Golden output of the convolution (for comparing results with): bin/conv_layer_output_feature_map.bin

* Weights for the convolution layer: bin/conv_layer_weights.bin

* Biases for the convolution layer: bin/conv_layer_bias.bin

Grading (Refer ‘What to submit’):

Part A – C model implementation -&gt; 3pts

Part B – Unoptimized by synthesizable tiled-convolution -&gt; 3pts

Part C – Optimized and (synthesizable) tiled-convolution -&gt; 4pts

If Lab Report not submitted -&gt; -6pts

If Lab Report submitted but not up to the mark or missing required items -&gt; accordingly pts can be subtracted (Refer ‘What to include in the Lab Report’ below).

Bonus points can be obtained as described in the ‘Bonus’ section.

What to include in the Lab Report:

Part A (-1pts):

1) How did you handle the border condition related to padding?

2) What is the MSE obtained (floating-point simulation)?

Part B (-1pts):

1) What is the MSE obtained (floating-point simulation)?

2) What is the latency and utilization (of each resource) you obtained after synthesis (for both single tile case and for the entire layer)? Note:

For these above questions, a brief and precise answer in one or two sentences is enough. For utilization mention resource count. Part C (-4pts):

1) A table indicating each optimization tried and corresponding latency, speedup, and utilization (of each resource) obtained.

Files:

tiled_conv.cpp -&gt; implement complete tiled convolution conv_3x3.cpp -&gt; implement convolution computation model_conv.cpp -&gt; implement convolution layer at software level (no hardware level features involved) sim.cpp -&gt; testbench

conv.h -&gt; contains defines and function declarations

utils.cpp -&gt; contains useful functions for implementing tiled convolution

* csim.out -&gt; binary obtained after compilation that can be run to simulate the design

Scripts:

0_cmodel_sim_float.sh followed by ./csim.out-&gt; Compile and simulate the software-level implementation with floating point data type (faster)

1_cmodel_sim_fixp.sh followed by ./csim.out-&gt; Compile and simulate the software-level implementation with fixed point data type

(slower)

2_hls_sim_float.sh followed by ./csim.out-&gt; Compile and simulate hardware level implementation with floating point data type

3_hls_sim_fixp.sh followed by ./csim.out -&gt; Compile and simulate hardware level implementation with fixed point a type conv_synth.tcl -&gt; Run Vitis HLS synthesis on conv_3x3 layer_synth.tcl -&gt; Run Vitis HLS synthesis on tiled_conv
