# Asynchronous_fifo_new
# Asynchronous FIFO in Verilog

A parameterized asynchronous FIFO for transferring data between independent write and read clock domains.

## Features
- Independent write and read clocks
- Gray-code pointers with two-stage synchronizers
- Full and empty flag generation
- Registered read output
- Active-high synchronous resets

## Modules
- fifo_mem
- wr_ptr_handler
- rd_ptr_handler
- synchronizer
- top_fifo

## Default Configuration
- Data width: 8 bits
- FIFO depth: 8 entries
- Address width: 3 bits

## Usage Notes
- Requires D = 2**PTR_SIZE and PTR_SIZE >= 2.
- Coordinate resets in both clock domains.
- Keep read and write enables low during reset.
- Data output is valid after an accepted read.

## Project Status
RTL implementation added. Testbench and verification results will be added later.

## Author
Ankush Pandey
