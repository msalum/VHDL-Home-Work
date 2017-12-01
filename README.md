# VHDL-Home-Work

Assignment: Debugging ALU design (5p)

Bob had to ship the ALU design to the hardware manufacturer by yesterday. The project manager is angry about missed deadline. 
Bob still hasn't figured out why the ALU is not working properly. Help Bob by figuring out what's the problem.

If you're on Ubuntu 14.04 install GHDL and GtkWave:
sudo add-apt-repository ppa:pgavin/ghdl
sudo apt-get update
sudo apt-get install ghdl gtkwave git

If you're on Ubuntu 16.04:
wget https://launchpad.net/~pgavin/+archive/ubuntu/ghdl/+build/6057094/+files/ghdl_0.31-1pgavin2~trusty2_amd64.deb
wget http://cz.archive.ubuntu.com/ubuntu/pool/universe/g/gnat-4.8/libgnat-4.8_4.8.2-8ubuntu3_amd64.deb
wget http://cz.archive.ubuntu.com/ubuntu/pool/universe/g/gnat-4.8/gnat-4.8-base_4.8.2-8ubuntu3_amd64.deb
sudo dpkg -i libgnat-4.8_4.8.2-8ubuntu3_amd64.deb  gnat-4.8-base_4.8.2-8ubuntu3_amd64.deb  ghdl_0.31-1pgavin2~trusty2_amd64.deb 
sudo apt -f install
sudo apt install gtkwave

Clone the repository
git clone https://github.com/laurivosandi/vhdl-exercise
Use make to compile the components and run the testbench:
cd path/to/vhdl-exercise
make

Expected output of the testbench:
alu_testbench.vhd:77:9:@360ns:(report note): Finished testing addition operation of ALU
alu_testbench.vhd:106:9:@1us:(report note): Finished testing subtraction operation of ALU
alu_testbench.vhd:135:9:@1640ns:(report note): Finished testing NAND operation of ALU
alu_testbench.vhd:166:9:@2280ns:(report note): Finished testing NOR operation of ALU

However there are few bugs in alu.vhd, find the bugs and correct them. If this is your first experience with VHDL, take a look here.

Assignment steps
Fork the repo on GitHub, clone your repo, fix mistakes, commit and push changes, 
send link to your GitHub repo where you have fixed the issues (5p)
Optional/extra: Expand ALU to 8 bits (2p)
Optional/extra: Add another opcode bit and implement multiplication so opcode(2) high means we're doing multiplication, 
opcode(1) in case of multiplication selects between higher and lower bits of the result and 
opcode(0) is used to negate the second operand of multiplication. (+5p)
