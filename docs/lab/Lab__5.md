---
title: Lab 5
author:Angelica Cesareo , Vinh Phan
---
# Task number 1-1
For the first part of the lab we were asked to design a SR latch and develop a test bench for it. we tried researching examples of test benches but we had a hard time understanding them. The closest we got to was this one.

module SR_latch_dataflow (input R, input S, output Q, output Qbar); 
assign #2 Q_i = Q;
assign #2 Qbar_i = Qbar; 
assign #2 Q = ~ (R | Qbar);
assign #2 Qbar = ~ (S | Q);
endmodule


SR_latch_dataflow DUT1 (.S(S), .R(R), .Q(Q), .Qbar(Qbar));

module testbench_SR_latch;
reg S, R;
wire Q;
wire Qbar;

integer i;

initial
 begin
  $recordfile("file1.trn");
  $recordvars();
 end


endmodule
