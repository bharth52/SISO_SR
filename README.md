# AIM
To stimulate and synthesis SISO SR using Vivado.

# Software Required:
vivado 2023.2 software.

# Procedure:
STEP:1 Start the vivado software, Select and Name the New project.

STEP:2 Select the device family, device, package and speed.

STEP:3 Select new source in the New Project and select Verilog Module as the Source type.

STEP:4 Type the File Name and module name and Click Next and then finish button. Type the code and save it.

STEP:5 Select the run simulation and then run Behavioral Simulation in the Source Window and click the check syntax.

STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table.

STEP:7 compare the output with truth table.# SISO_SR
# The shift register, which allows serial input (one bit after the other through a single data line) and produces a serial output is known as a Serial-In Serial-Out shift register. Since there is only one output, the data leaves the shift register one bit at a time in a serial pattern, thus the name Serial-In Serial-Out Shift Register. The logic circuit given below shows a serial-in serial-out shift register. The circuit consists of four D flip-flops which are connected in a serial manner. All these flip-flops are synchronous with each other since the same clock signal is applied to each flip-flop. 
![image](https://github.com/RESMIRNAIR/SISO_SR/assets/154305926/778bf654-f276-4c56-ab9b-33de0e21eac9)
# PROGRAM
library IEEE;

use IEEE.STD_LOGIC_1164.ALL;

use IEEE.STD_LOGIC_ARITH.ALL;

use IEEE.STD_LOGIC_UNSIGNED.ALL;

entity sipo is

Port (clk,rst,s_in:in std_logic;

p_out: out std_logic_vector(3 downto 0));

end sipo;

architecture Behavioral of sipo is

signal temp_reg: std_logic_vector(3 downto 0):=(others=>'0');

begin

process(clk,rst)

begin

if rst='1' then

temp_reg<=(others=>'0');

elsif rising_edge(clk) then

temp_reg <= temp_reg(2 downto 0) & s_in;

end if

end process

end Behavioral
# OUTPUT
![329478098-6808f6ca-b18d-449b-8126-6b8c20b336b3](https://github.com/bharth52/SISO_SR/assets/165644574/c65a5012-1005-4e69-ba6a-c81c03a2f0c9)
# RESULT
The SISO_SR output has verified successfully

