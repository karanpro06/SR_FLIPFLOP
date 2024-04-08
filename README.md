# SR_FLIPFLOP
# Aim
To design and simulate SR Flipflop using vivado.
Apparatus Required
Personal Computer with vivado software.
![image](https://github.com/RESMIRNAIR/SR_FLIPFLOP/assets/154305926/c17acfa3-84d9-4ef6-99ab-d36655169f63)
# Circuit Diagram
![image](https://github.com/RESMIRNAIR/SR_FLIPFLOP/assets/154305926/51cb1738-6112-466e-a1b0-f9dd9f2e9d25)
# Truth Table
![image](https://github.com/RESMIRNAIR/SR_FLIPFLOP/assets/154305926/0946849a-bd0a-445b-b27e-0833dee20e51)
# Program
~~~
module sr(clk,s,r,rst,q );
input s,r,clk,rst;
output reg q;
always@(posedge clk)
begin
if(rst==1)
q=1'b0;
else
begin
case({s,r})
2'b00: q=q;
2'b01:q=1'b0;
2'b10:q=1'b1;
2'b11:q=1'bx;
endcase
end
end
endmodule
~~~
# Output
![image](https://github.com/karanpro06/SR_FLIPFLOP/assets/119782103/789cce66-5a8e-4142-b9d8-2e76ff202248)
# Result
Hence the SR Flipflop is verified successfully.
