library ieee;
use ieee.std_logic_1164.all;
use ieee.std_logic_unsigned.all;

entity rom_en is
  port (a, b, c         : in  std_logic;
         f1, f2, f3, f4 : out std_logic);
end;
architecture arch_rom of rom_en is

  type     memory is array (7 downto 0) of std_logic_vector (3 downto 0);
  constant ROM : memory := ("0100", "0110", "1000", "1101", "0010", "0001", "1101", "1011");
  signal   sel : std_logic_vector(2 downto 0);
  signal   y   : std_logic_vector(3 downto 0);
signal temp: integer:=0;
begin
  sel <= a & b & c;
--  with sel select
-- y <=  rom(0)      when "111",
-- rom(1)      when "110",
-- rom(2)      when "101",
--   rom(3)      when "100",
--          rom(4)      when "011",
--                 rom(5)      when "010",
--       rom(6)      when "001",
--rom(7) when others;
temp <= conv_integer(sel);
y<= rom(7-temp);

  f1 <= y(3);
  f2 <= y(2);
  f3 <= y(1);
  f4 <= y(0);

end arch_rom;
