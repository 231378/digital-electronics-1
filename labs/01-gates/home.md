# Lab 1: Josef Kaplan

### De Morgan's laws

1. Equations of all three versions of logic function f(c,b,a):

   ![Logic function](images/1.png)

2. Listing of VHDL architecture from design file (`design.vhd`) for all three functions. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture dataflow of demorgan is
begin
    f_org_o  <= (not(b_i) and a_i) or (not(c_i) and not(b_i));
    f_nand_o <= (((b_i nand b_i) nand ((a_i nand a_i) nand c_i)) nand '1');
    f_nor_o  <= (b_i nor (a_i nor (c_i nor c_i)));
end architecture dataflow;
```

3. Complete table with logic functions' values:

| **c** | **b** |**a** | **f(c,b,a)_ORG** | **f(c,b,a)_NAND** | **f(c,b,a)_NOR** |
| :-: | :-: | :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 1 | 1 | 1 |
| 0 | 0 | 1 | 1 | 1 | 1 |
| 0 | 1 | 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 | 0 | 0 |
| 1 | 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 | 1 | 1 |
| 1 | 1 | 0 | 0 | 0 | 0 |
| 1 | 1 | 1 | 0 | 0 | 0 |

![your figure](https://github.com/231378/digital-electronics-1/blob/main/labs/01-gates/images/2.png)

### Distributive laws

1. Screenshot with simulated time waveforms. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   ![your figure](https://github.com/231378/digital-electronics-1/blob/main/labs/01-gates/images/3.png)
   
   ![your figure](https://github.com/231378/digital-electronics-1/blob/main/labs/01-gates/images/4.png)
   
2. Link to your public EDA Playground example:

   [Odkaz](https://www.edaplayground.com/x/jeJb)
