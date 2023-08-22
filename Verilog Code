`timescale 1ns / 1ps
//////////////////////////////////////////////////////////////////////////////////
// Company: 
// Engineer: 
// 
// Create Date: 27.02.2023 14:53:39
// Design Name: 
// Module Name: traficlight
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


module traficlight(
    input clk,
    input rst,
    output reg [2:0] L1,
    output reg [2:0]L2,
    output reg [2:0]LT,
    output reg[2:0]SL
    );
         parameter  S1=0, S2=1, S3 =2, S4=3, S5=4,S6=5;
       reg [3:0]count;
       reg[2:0] ps;
       parameter  sec7=7,sec5=5,sec2=2,sec3=3;
       always@(posedge clk or posedge rst)
           begin
           if(rst==1)
           begin
           ps<=S1;
           count<=0;
           end
           else
                 case(ps)
                   S1: if(count<sec7)
                           begin
                           ps<=S1;
                           count<=count+1;
                           end
                       else
                           begin
                           ps<=S2;
                           count<=0;
                           end
                   S2: if(count<sec2)
                           begin
                           ps<=S2;
                           count<=count+1;
                           end
                       else
                           begin
                           ps<=S3;
                           count<=0;
                           end
                   S3: if(count<sec5)
                           begin
                           ps<=S3;
                           count<=count+1;
                           end
                       else
                           begin
                           ps<=S4;
                           count<=0;
                           end
                   S4:if(count<sec2)
                           begin
                           ps<=S4;
                           count<=count+1;
                           end
                       else
                           begin
                           ps<=S5;
                           count<=0;
                           end
                   S5:if(count<sec3)
                           begin
                           ps<=S5;
                           count<=count+1;
                           end
                       else
                           begin
                           ps<=S6;
                           count<=0;
                           end   
                   S6:if(count<sec2)
                           begin
                           ps<=S6;
                           count<=count+1;
                           end  
                       else
                           begin
                           ps<=S1;
                           count<=0;
                           end
                   default: ps<=S1;
                   endcase
               end      
               always@(ps)    
               begin                 
                   case(ps)                        
                       S1:
                        begin
                       L1<=3'b001;
                          L2<=3'b001;
                          LT<=3'b100;
                          SL<=3'b100;
                       end
                       S2:
                       begin 
                          L1<=3'b001;
                          L2<=3'b010;
                          LT<=3'b100;
                          SL<=3'b100;
                       end
                       S3:
                       begin
                          L1<=3'b001;
                          L2<=3'b100;
                          LT<=3'b001;
                          SL<=3'b100;
                       end
                       S4:
                       begin
                         L1<=3'b010;
                         L2<=3'b100;
                          LT<=3'b010;
                          SL<=3'b100;
                       end
                       S5:
                       begin
                          L1<=3'b100;
                          L2<=3'b100;
                          LT<=3'b100;
                          SL<=3'b001;
                       end
                       S6:
                       begin 
                          L1<=3'b100;
                          L2<=3'b100;
                          LT<=3'b100;
                          SL<=3'b010;
                       end
                       default:
                       begin 
                          L1<=3'b000;
                          L2<=3'b000;
                          LT<=3'b000;
                          SL<=3'b000;
                       end
                       endcase
               end                
                 
endmodule
