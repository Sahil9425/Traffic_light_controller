`timescale 1ns / 1ps
//////////////////////////////////////////////////////////////////////////////////
// Company: 
// Engineer: 
// 
// Create Date: 01.03.2023 21:34:19
// Design Name: 
// Module Name: traficlighttb
// Project Name: 
// Target Devices: 
// Tool Versions: 
// Description: 
// 
// Dependencies: 
// 
// Revision:
// Revision 0.01 - File Created
// Additional Comments:
// 
//////////////////////////////////////////////////////////////////////////////////


module traficlighttb();
reg clk,rst;
wire [2:0]L1;
wire [2:0]L2;
wire [2:0]LT;
wire [2:0]SL;
traficlight dut(.clk(clk) , .rst(rst) , .L1(L1) , .L2(L2)  ,.LT(LT),.SL(SL)   );

initial
begin
    clk=1'b0;
    forever #100 clk=~clk;
end

initial
begin
    rst=0;
    #100;
    rst=1;
    #100;
    rst=0;
    #(100*2);
    $finish;
    end

endmodule
