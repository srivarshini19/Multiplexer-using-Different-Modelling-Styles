# SIMULATION AND IMPLEMENTATION OF 4:1 MULTIPLEXER

AIM
To design and simulate a 4:1 Multiplexer (MUX) using Verilog HDL in four different modeling styles—Gate-Level, Data Flow, Behavioral, and Structural—and to verify its functionality through a testbench using the Vivado 2023.1 simulation environment. The experiment aims to understand how different abstraction levels in Verilog can be used to describe the same digital logic circuit and analyze their performance.

APPARATUS REQUIRED
Vivado 2023.1
Procedure
Open Vivado 2023.1.
Create a New RTL Project and give a name (e.g., Mux4_to_1).
Add/create your Verilog files and testbench.
Select an FPGA part (e.g., xc7a35ticsg324-1L).
Run Synthesis to check for errors.
Run Simulation → Run Behavioral Simulation.
Observe the waveforms of inputs and outputs.
Adjust simulation time if needed (e.g., 1000ns).
Save the project and take screenshots of results.
Close simulation.
Logic Diagram
<img width="1014" height="807" alt="image" src="https://github.com/user-attachments/assets/b74506cc-aa74-4256-862d-bbad11abdc73" />


Truth Table
<img width="873" height="464" alt="image" src="https://github.com/user-attachments/assets/0af78cc7-3f91-4be9-8c60-69db8acf8570" />


Verilog Code
4:1 MUX Gate-Level Implementation
// Gate Level Modelling - Skeleton
module mux4_gate (
    input  wire I0, I1, I2, I3,
    input  wire S0, S1,
    output wire Y
);
    // Declare internal wires

    // Write NOT gates

    // Write AND gates

    // Write OR gate

endmodule
4:1 MUX Gate-Level Implementation- Testbench
// Testbench Skeleton
`timescale 1ns/1ps
module tb_mux4_gate;

    // Declare testbench signals
    reg I0, I1, I2, I3;
    reg S0, S1;
    wire Y;

    // Instantiate DUT
    mux4_gate uut (
        .I0(I0), .I1(I1), .I2(I2), .I3(I3),
        .S0(S0), .S1(S1),
        .Y(Y)
    );

    initial begin
        // Initialize inputs

        // Apply test cases

        // Stop simulation
        #10 $stop;
    end

endmodule
Simulated Output Gate Level Modelling
_______ Here Paste the Simulated output ___________

4:1 MUX Data flow Modelling
// Dataflow Modelling - Skeleton
module mux4_dataflow (
    input  wire I0, I1, I2, I3,
    input  wire S0, S1,
    output wire Y
);
    // Write assign statement using operators

endmodule
4:1 MUX Data flow Modelling- Testbench
// Testbench Skeleton
`timescale 1ns/1ps
module tb_mux4_dataflow;

    // Declare testbench signals
    reg I0, I1, I2, I3;
    reg S0, S1;
    wire Y;

    // Instantiate DUT
    mux4_dataflow uut (
        .I0(I0), .I1(I1), .I2(I2), .I3(I3),
        .S0(S0), .S1(S1),
        .Y(Y)
    );

    initial begin
        // Initialize inputs

        // Apply test cases

        // Stop simulation
        #10 $stop;
    end

endmodule
Simulated Output Dataflow Modelling
_______ Here Paste the Simulated output ___________

4:1 MUX Behavioral Implementation
module mux4_to_1_behavioral (
    input wire A,
    input wire B,
    input wire C,
    input wire D,
    input wire S0,
    input wire S1,
    output reg Y
);
    always @(*) begin
        
    end
endmodule
4:1 MUX Behavioral Modelling- Testbench
// Testbench Skeleton
`timescale 1ns/1ps
module tb_mux4_behavioral;

    // Declare testbench signals
    reg I0, I1, I2, I3;
    reg S0, S1;
    wire Y;

    // Instantiate DUT
    mux4_behavioral uut (
        .I0(I0), .I1(I1), .I2(I2), .I3(I3),
        .S0(S0), .S1(S1),
        .Y(Y)
    );

    initial begin
        // Initialize inputs

        // Apply test cases

        // Stop simulation
        #10 $stop;
    end

endmodule
Simulated Output Behavioral Modelling
_______ Here Paste the Simulated output ___________

4:1 MUX Structural Implementation
<img width="1471" height="821" alt="image" src="https://github.com/user-attachments/assets/19c1fd5a-d70f-409b-9090-edacc40b8425" />


module mux2_to_1 (
    input wire A,
    input wire B,
    input wire S,
    output wire Y
);
    assign Y = S ? B : A;
endmodule

module mux4_to_1_structural (
    input wire A,
    input wire B,
    input wire C,
    input wire D,
    input wire S0,
    input wire S1,
    output wire Y
);




endmodule
Testbench Implementation
`timescale 1ns / 1ps

module mux4_to_1_tb;
    reg A, B, C, D, S0, S1;
    wire Y_gate, Y_dataflow, Y_behavioral, Y_structural;

    

    initial begin
        A = 0; B = 0; C = 0; D = 0; S0 = 0; S1 = 0;

      
        #10 $stop;
    end

   
    end
endmodule
Simulated Output Structural Modelling
_______ Here Paste the Simulated output ___________

CONCLUSION
In this experiment, a 4:1 Multiplexer was successfully designed and simulated using Verilog HDL across four different modeling styles: Gate-Level, Data Flow, Behavioral, and Structural.The simulation results verified the correct functionality of the MUX, with all implementations producing identical outputs for the given input conditions.
