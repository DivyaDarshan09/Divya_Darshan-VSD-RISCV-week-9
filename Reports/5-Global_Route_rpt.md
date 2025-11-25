==========================================================================
global route report_tns
--------------------------------------------------------------------------
tns max 0.00

==========================================================================
global route report_wns
--------------------------------------------------------------------------
wns max 0.00

==========================================================================
global route report_worst_slack
--------------------------------------------------------------------------
worst slack max 5.95

==========================================================================
global route report_clock_min_period
--------------------------------------------------------------------------
clk period_min = 5.05 fmax = 198.08

==========================================================================
global route report_clock_skew
--------------------------------------------------------------------------
Clock clk
   0.85 source latency core.CPU_dmem_rd_data_a5[13]$DFF_P/CLK ^
  -0.73 target latency core.CPU_Xreg_value_a4[27][13]$SDFFE_PP0P/CLK ^
   0.00 CRPR
--------------
   0.11 setup skew


==========================================================================
global route report_checks -path_delay min
--------------------------------------------------------------------------
Startpoint: core.CPU_inc_pc_a2[5]$DFF_P
            (rising edge-triggered flip-flop clocked by clk)
Endpoint: core.CPU_inc_pc_a3[5]$DFF_P
          (rising edge-triggered flip-flop clocked by clk)
Path Group: clk
Path Type: min

Fanout     Cap    Slew   Delay    Time   Description
-----------------------------------------------------------------------------
                          0.00    0.00   clock clk (rise edge)
                          0.00    0.00   clock source latency
     1    0.12    0.00    0.00    0.00 ^ pll/CLK (avsdpll)
                                         CLK (net)
                  0.01    0.01    0.01 ^ clkbuf_0_CLK/A (sky130_fd_sc_hd__clkbuf_16)
     8    0.21    0.22    0.24    0.25 ^ clkbuf_0_CLK/X (sky130_fd_sc_hd__clkbuf_16)
                                         clknet_0_CLK (net)
                  0.22    0.01    0.26 ^ clkbuf_3_4_f_CLK/A (sky130_fd_sc_hd_clkbuf_16)
    14    0.21    0.22    0.32    0.57 ^ clkbuf_3_4_f_CLK/X (sky130_fd_sc_hd_clkbuf_16)
                                         clknet_3_4__leaf_CLK (net)
                  0.22    0.01    0.58 ^ clkbuf_leaf_4_CLK/A (sky130_fd_sc_hd__clkbuf_16)
    10    0.04    0.06    0.20    0.78 ^ clkbuf_leaf_4_CLK/X (sky130_fd_sc_hd__clkbuf_16)
                                         clknet_leaf_4_CLK (net)
                  0.06    0.00    0.78 ^ core.CPU_inc_pc_a2[5]$DFF_P/CLK (sky130_fd_sc_hd__dfxtp_1)
     1    0.00    0.04    0.30    1.09 ^ core.CPU_inc_pc_a2[5]$DFF_P/Q (sky130_fd_sc_hd__dfxtp_1)
                                         core.CPU_inc_pc_a2[5] (net)
                  0.04    0.00    1.09 ^ core.CPU_inc_pc_a3[5]$DFF_P/D (sky130_fd_sc_hd__dfxtp_1)
                                  1.09   data arrival time

                          0.00    0.00   clock clk (rise edge)
                          0.00    0.00   clock source latency
     1    0.12    0.00    0.00    0.00 ^ pll/CLK (avsdpll)
                                         CLK (net)
                  0.01    0.01    0.01 ^ clkbuf_0_CLK/A (sky130_fd_sc_hd__clkbuf_16)
     8    0.21    0.22    0.24    0.25 ^ clkbuf_0_CLK/X (sky130_fd_sc_hd__clkbuf_16)
                                         clknet_0_CLK (net)
                  0.22    0.01    0.26 ^ clkbuf_3_1_f_CLK/A (sky130_fd_sc_hd_clkbuf_16)
    13    0.22    0.23    0.33    0.58 ^ clkbuf_3_1_f_CLK/X (sky130_fd_sc_hd_clkbuf_16)
                                         clknet_3_1__leaf_CLK (net)
                  0.23    0.01    0.59 ^ clkbuf_leaf_3_CLK/A (sky130_fd_sc_hd__clkbuf_16)
    10    0.04    0.06    0.20    0.79 ^ clkbuf_leaf_3_CLK/X (sky130_fd_sc_hd__clkbuf_16)
                                         clknet_leaf_3_CLK (net)
                  0.06    0.00    0.79 ^ core.CPU_inc_pc_a3[5]$DFF_P/CLK (sky130_fd_sc_hd__dfxtp_1)
                          0.00    0.79   clock reconvergence pessimism
                         -0.03    0.76   library hold time
                                  0.76   data required time
-----------------------------------------------------------------------------
                                  0.76   data required time
                                 -1.09   data arrival time
-----------------------------------------------------------------------------
                                  0.32   slack (MET)



==========================================================================
global route report_checks -path_delay max
--------------------------------------------------------------------------
Startpoint: core.CPU_src1_value_a3[2]$DFF_P
            (rising edge-triggered flip-flop clocked by clk)
Endpoint: core.CPU_Xreg_value_a4[3][18]$SDFFE_PP0P
          (rising edge-triggered flip-flop clocked by clk)
Path Group: clk
Path Type: max

Fanout     Cap    Slew   Delay    Time   Description
-----------------------------------------------------------------------------
                          0.00    0.00   clock clk (rise edge)
                          0.00    0.00   clock source latency
     1    0.12    0.00    0.00    0.00 ^ pll/CLK (avsdpll)
                                         CLK (net)
                  0.01    0.01    0.01 ^ clkbuf_0_CLK/A (sky130_fd_sc_hd__clkbuf_16)
     8    0.21    0.22    0.24    0.25 ^ clkbuf_0_CLK/X (sky130_fd_sc_hd__clkbuf_16)
                                         clknet_0_CLK (net)
                  0.22    0.01    0.26 ^ clkbuf_3_1_f_CLK/A (sky130_fd_sc_hd_clkbuf_16)
    13    0.22    0.23    0.33    0.58 ^ clkbuf_3_1_f_CLK/X (sky130_fd_sc_hd_clkbuf_16)
                                         clknet_3_1__leaf_CLK (net)
                  0.23    0.01    0.59 ^ clkbuf_leaf_67_CLK/A (sky130_fd_sc_hd__clkbuf_16)
    11    0.05    0.07    0.21    0.80 ^ clkbuf_leaf_67_CLK/X (sky130_fd_sc_hd__clkbuf_16)
                                         clknet_leaf_67_CLK (net)
                  0.07    0.00    0.80 ^ core.CPU_src1_value_a3[2]$DFF_P/CLK (sky130_fd_sc_hd__dfxtp_1)
    11    0.06    0.52    0.65    1.45 ^ core.CPU_src1_value_a3[2]$DFF_P/Q (sky130_fd_sc_hd__dfxtp_1)
                                         core.CPU_src1_value_a3[2] (net)
                  0.52    0.00    1.45 ^ 10761/A (sky130_fd_sc_hd__ha_1)
     8    0.04    0.19    0.45    1.90 v 10761/SUM (sky130_fd_sc_hd__ha_1)
                                         00040 (net)
                  0.19    0.00    1.90 v 07458/B_N (sky130_fd_sc_hd__nor2b_1)
     3    0.01    0.07    0.23    2.12 v 07458/Y (sky130_fd_sc_hd__nor2b_1)
                                         02570 (net)
                  0.07    0.00    2.12 v 07460/A3 (sky130_fd_sc_hd__o31ai_1)
     3    0.02    0.65    0.55    2.67 ^ 07460/Y (sky130_fd_sc_hd__o31ai_1)
                                         02572 (net)
                  0.65    0.00    2.68 ^ 07720/A1 (sky130_fd_sc_hd__a2111oi_0)
     1    0.01    0.23    0.31    2.98 v 07720/Y (sky130_fd_sc_hd__a2111oi_0)
                                         02828 (net)
                  0.23    0.00    2.98 v 07721/C (sky130_fd_sc_hd__or3_1)
     4    0.03    0.17    0.50    3.48 v 07721/X (sky130_fd_sc_hd__or3_1)
                                         02829 (net)
                  0.17    0.00    3.48 v 07891/A3 (sky130_fd_sc_hd__a311o_1)
     1    0.01    0.08    0.43    3.91 v 07891/X (sky130_fd_sc_hd__a311o_1)
                                         02995 (net)
                  0.08    0.00    3.91 v 07892/B (sky130_fd_sc_hd__xnor2_1)
     2    0.02    0.47    0.41    4.32 ^ 07892/Y (sky130_fd_sc_hd__xnor2_1)
                                         02996 (net)
                  0.47    0.00    4.32 ^ 07910/B1 (sky130_fd_sc_hd__o221ai_1)
     2    0.01    0.20    0.29    4.61 v 07910/Y (sky130_fd_sc_hd__o221ai_1)
                                         03014 (net)
                  0.20    0.00    4.61 v 07912/A4 (sky130_fd_sc_hd__a41oi_2)
    11    0.07    0.82    0.76    5.37 ^ 07912/Y (sky130_fd_sc_hd__a41oi_2)
                                         03016 (net)
                  0.83    0.01    5.38 ^ 09311/A (sky130_fd_sc_hd__nand2_1)
     1    0.01    0.17    0.17    5.54 v 09311/Y (sky130_fd_sc_hd__nand2_1)
                                         04156 (net)
                  0.17    0.00    5.54 v 09313/A1 (sky130_fd_sc_hd__a21oi_1)
     1    0.01    0.23    0.25    5.79 ^ 09313/Y (sky130_fd_sc_hd__a21oi_1)
                                         01017 (net)
                  0.23    0.00    5.79 ^ core.CPU_Xreg_value_a4[3][18]$SDFFE_PP0P/D (sky130_fd_sc_hd__dfxtp_1)
                                  5.79   data arrival time

                         11.00   11.00   clock clk (rise edge)
                          0.00   11.00   clock source latency
     1    0.12    0.00    0.00   11.00 ^ pll/CLK (avsdpll)
                                         CLK (net)
                  0.01    0.01   11.01 ^ clkbuf_0_CLK/A (sky130_fd_sc_hd__clkbuf_16)
     8    0.21    0.22    0.24   11.25 ^ clkbuf_0_CLK/X (sky130_fd_sc_hd__clkbuf_16)
                                         clknet_0_CLK (net)
                  0.22    0.01   11.26 ^ clkbuf_3_2_f_CLK/A (sky130_fd_sc_hd_clkbuf_16)
    18    0.26    0.27    0.35   11.61 ^ clkbuf_3_2_f_CLK/X (sky130_fd_sc_hd_clkbuf_16)
                                         clknet_3_2__leaf_CLK (net)
                  0.27    0.01   11.61 ^ clkbuf_leaf_75_CLK/A (sky130_fd_sc_hd__clkbuf_16)
    12    0.05    0.07    0.22   11.84 ^ clkbuf_leaf_75_CLK/X (sky130_fd_sc_hd__clkbuf_16)
                                         clknet_leaf_75_CLK (net)
                  0.07    0.00   11.84 ^ core.CPU_Xreg_value_a4[3][18]$SDFFE_PP0P/CLK (sky130_fd_sc_hd__dfxtp_1)
                          0.00   11.84   clock reconvergence pessimism
                         -0.09   11.74   library setup time
                                 11.74   data required time
-----------------------------------------------------------------------------
                                 11.74   data required time
                                 -5.79   data arrival time
-----------------------------------------------------------------------------
                                  5.95   slack (MET)



==========================================================================
global route report_checks -unconstrained
--------------------------------------------------------------------------
Startpoint: core.CPU_src1_value_a3[2]$DFF_P
            (rising edge-triggered flip-flop clocked by clk)
Endpoint: core.CPU_Xreg_value_a4[3][18]$SDFFE_PP0P
          (rising edge-triggered flip-flop clocked by clk)
Path Group: clk
Path Type: max

Fanout     Cap    Slew   Delay    Time   Description
-----------------------------------------------------------------------------
                          0.00    0.00   clock clk (rise edge)
                          0.00    0.00   clock source latency
     1    0.12    0.00    0.00    0.00 ^ pll/CLK (avsdpll)
                                         CLK (net)
                  0.01    0.01    0.01 ^ clkbuf_0_CLK/A (sky130_fd_sc_hd__clkbuf_16)
     8    0.21    0.22    0.24    0.25 ^ clkbuf_0_CLK/X (sky130_fd_sc_hd__clkbuf_16)
                                         clknet_0_CLK (net)
                  0.22    0.01    0.26 ^ clkbuf_3_1_f_CLK/A (sky130_fd_sc_hd_clkbuf_16)
    13    0.22    0.23    0.33    0.58 ^ clkbuf_3_1_f_CLK/X (sky130_fd_sc_hd_clkbuf_16)
                                         clknet_3_1__leaf_CLK (net)
                  0.23    0.01    0.59 ^ clkbuf_leaf_67_CLK/A (sky130_fd_sc_hd__clkbuf_16)
    11    0.05    0.07    0.21    0.80 ^ clkbuf_leaf_67_CLK/X (sky130_fd_sc_hd__clkbuf_16)
                                         clknet_leaf_67_CLK (net)
                  0.07    0.00    0.80 ^ core.CPU_src1_value_a3[2]$DFF_P/CLK (sky130_fd_sc_hd__dfxtp_1)
    11    0.06    0.52    0.65    1.45 ^ core.CPU_src1_value_a3[2]$DFF_P/Q (sky130_fd_sc_hd__dfxtp_1)
                                         core.CPU_src1_value_a3[2] (net)
                  0.52    0.00    1.45 ^ 10761/A (sky130_fd_sc_hd__ha_1)
     8    0.04    0.19    0.45    1.90 v 10761/SUM (sky130_fd_sc_hd__ha_1)
                                         00040 (net)
                  0.19    0.00    1.90 v 07458/B_N (sky130_fd_sc_hd__nor2b_1)
     3    0.01    0.07    0.23    2.12 v 07458/Y (sky130_fd_sc_hd__nor2b_1)
                                         02570 (net)
                  0.07    0.00    2.12 v 07460/A3 (sky130_fd_sc_hd__o31ai_1)
     3    0.02    0.65    0.55    2.67 ^ 07460/Y (sky130_fd_sc_hd__o31ai_1)
                                         02572 (net)
                  0.65    0.00    2.68 ^ 07720/A1 (sky130_fd_sc_hd__a2111oi_0)
     1    0.01    0.23    0.31    2.98 v 07720/Y (sky130_fd_sc_hd__a2111oi_0)
                                         02828 (net)
                  0.23    0.00    2.98 v 07721/C (sky130_fd_sc_hd__or3_1)
     4    0.03    0.17    0.50    3.48 v 07721/X (sky130_fd_sc_hd__or3_1)
                                         02829 (net)
                  0.17    0.00    3.48 v 07891/A3 (sky130_fd_sc_hd__a311o_1)
     1    0.01    0.08    0.43    3.91 v 07891/X (sky130_fd_sc_hd__a311o_1)
                                         02995 (net)
                  0.08    0.00    3.91 v 07892/B (sky130_fd_sc_hd__xnor2_1)
     2    0.02    0.47    0.41    4.32 ^ 07892/Y (sky130_fd_sc_hd__xnor2_1)
                                         02996 (net)
                  0.47    0.00    4.32 ^ 07910/B1 (sky130_fd_sc_hd__o221ai_1)
     2    0.01    0.20    0.29    4.61 v 07910/Y (sky130_fd_sc_hd__o221ai_1)
                                         03014 (net)
                  0.20    0.00    4.61 v 07912/A4 (sky130_fd_sc_hd__a41oi_2)
    11    0.07    0.82    0.76    5.37 ^ 07912/Y (sky130_fd_sc_hd__a41oi_2)
                                         03016 (net)
                  0.83    0.01    5.38 ^ 09311/A (sky130_fd_sc_hd__nand2_1)
     1    0.01    0.17    0.17    5.54 v 09311/Y (sky130_fd_sc_hd__nand2_1)
                                         04156 (net)
                  0.17    0.00    5.54 v 09313/A1 (sky130_fd_sc_hd__a21oi_1)
     1    0.01    0.23    0.25    5.79 ^ 09313/Y (sky130_fd_sc_hd__a21oi_1)
                                         01017 (net)
                  0.23    0.00    5.79 ^ core.CPU_Xreg_value_a4[3][18]$SDFFE_PP0P/D (sky130_fd_sc_hd__dfxtp_1)
                                  5.79   data arrival time

                         11.00   11.00   clock clk (rise edge)
                          0.00   11.00   clock source latency
     1    0.12    0.00    0.00   11.00 ^ pll/CLK (avsdpll)
                                         CLK (net)
                  0.01    0.01   11.01 ^ clkbuf_0_CLK/A (sky130_fd_sc_hd__clkbuf_16)
     8    0.21    0.22    0.24   11.25 ^ clkbuf_0_CLK/X (sky130_fd_sc_hd__clkbuf_16)
                                         clknet_0_CLK (net)
                  0.22    0.01   11.26 ^ clkbuf_3_2_f_CLK/A (sky130_fd_sc_hd_clkbuf_16)
    18    0.26    0.27    0.35   11.61 ^ clkbuf_3_2_f_CLK/X (sky130_fd_sc_hd_clkbuf_16)
                                         clknet_3_2__leaf_CLK (net)
                  0.27    0.01   11.61 ^ clkbuf_leaf_75_CLK/A (sky130_fd_sc_hd__clkbuf_16)
    12    0.05    0.07    0.22   11.84 ^ clkbuf_leaf_75_CLK/X (sky130_fd_sc_hd__clkbuf_16)
                                         clknet_leaf_75_CLK (net)
                  0.07    0.00   11.84 ^ core.CPU_Xreg_value_a4[3][18]$SDFFE_PP0P/CLK (sky130_fd_sc_hd__dfxtp_1)
                          0.00   11.84   clock reconvergence pessimism
                         -0.09   11.74   library setup time
                                 11.74   data required time
-----------------------------------------------------------------------------
                                 11.74   data required time
                                 -5.79   data arrival time
-----------------------------------------------------------------------------
                                  5.95   slack (MET)



==========================================================================
global route report_check_types -max_slew -max_cap -max_fanout -violators
--------------------------------------------------------------------------

==========================================================================
global route max_slew_check_slack
--------------------------------------------------------------------------
0.21674507856369019

==========================================================================
global route max_slew_check_limit
--------------------------------------------------------------------------
1.5035289525985718

==========================================================================
global route max_slew_check_slack_limit
--------------------------------------------------------------------------
0.1442

==========================================================================
global route max_fanout_check_slack
--------------------------------------------------------------------------
1.0000000150474662e+30

==========================================================================
global route max_fanout_check_limit
--------------------------------------------------------------------------
1.0000000150474662e+30

==========================================================================
global route max_capacitance_check_slack
--------------------------------------------------------------------------
0.012511934153735638

==========================================================================
global route max_capacitance_check_limit
--------------------------------------------------------------------------
0.021067000925540924

==========================================================================
global route max_capacitance_check_slack_limit
--------------------------------------------------------------------------
0.5939

==========================================================================
global route max_slew_violation_count
--------------------------------------------------------------------------
max slew violation count 0

==========================================================================
global route max_fanout_violation_count
--------------------------------------------------------------------------
max fanout violation count 0

==========================================================================
global route max_cap_violation_count
--------------------------------------------------------------------------
max cap violation count 0

==========================================================================
global route setup_violation_count
--------------------------------------------------------------------------
setup violation count 0

==========================================================================
global route hold_violation_count
--------------------------------------------------------------------------
hold violation count 0

==========================================================================
global route report_checks -path_delay max reg to reg
--------------------------------------------------------------------------
Startpoint: core.CPU_src1_value_a3[2]$DFF_P
            (rising edge-triggered flip-flop clocked by clk)
Endpoint: core.CPU_Xreg_value_a4[3][18]$SDFFE_PP0P
          (rising edge-triggered flip-flop clocked by clk)
Path Group: clk
Path Type: max

  Delay    Time   Description
---------------------------------------------------------
   0.00    0.00   clock clk (rise edge)
   0.00    0.00   clock source latency
   0.00    0.00 ^ pll/CLK (avsdpll)
   0.25    0.25 ^ clkbuf_0_CLK/X (sky130_fd_sc_hd__clkbuf_16)
   0.33    0.58 ^ clkbuf_3_1_f_CLK/X (sky130_fd_sc_hd_clkbuf_16)
   0.22    0.80 ^ clkbuf_leaf_67_CLK/X (sky130_fd_sc_hd__clkbuf_16)
   0.00    0.80 ^ core.CPU_src1_value_a3[2]$DFF_P/CLK (sky130_fd_sc_hd__dfxtp_1)
   0.65    1.45 ^ core.CPU_src1_value_a3[2]$DFF_P/Q (sky130_fd_sc_hd__dfxtp_1)
   0.45    1.90 v 10761/SUM (sky130_fd_sc_hd__ha_1)
   0.23    2.12 v 07458/Y (sky130_fd_sc_hd__nor2b_1)
   0.55    2.67 ^ 07460/Y (sky130_fd_sc_hd__o31ai_1)
   0.31    2.98 v 07720/Y (sky130_fd_sc_hd__a2111oi_0)
   0.50    3.48 v 07721/X (sky130_fd_sc_hd__or3_1)
   0.43    3.91 v 07891/X (sky130_fd_sc_hd__a311o_1)
   0.41    4.32 ^ 07892/Y (sky130_fd_sc_hd__xnor2_1)
   0.29    4.61 v 07910/Y (sky130_fd_sc_hd__o221ai_1)
   0.76    5.37 ^ 07912/Y (sky130_fd_sc_hd__a41oi_2)
   0.17    5.54 v 09311/Y (sky130_fd_sc_hd__nand2_1)
   0.25    5.79 ^ 09313/Y (sky130_fd_sc_hd__a21oi_1)
   0.00    5.79 ^ core.CPU_Xreg_value_a4[3][18]$SDFFE_PP0P/D (sky130_fd_sc_hd__dfxtp_1)
           5.79   data arrival time

  11.00   11.00   clock clk (rise edge)
   0.00   11.00   clock source latency
   0.00   11.00 ^ pll/CLK (avsdpll)
   0.25   11.25 ^ clkbuf_0_CLK/X (sky130_fd_sc_hd__clkbuf_16)
   0.36   11.61 ^ clkbuf_3_2_f_CLK/X (sky130_fd_sc_hd_clkbuf_16)
   0.23   11.84 ^ clkbuf_leaf_75_CLK/X (sky130_fd_sc_hd__clkbuf_16)
   0.00   11.84 ^ core.CPU_Xreg_value_a4[3][18]$SDFFE_PP0P/CLK (sky130_fd_sc_hd__dfxtp_1)
   0.00   11.84   clock reconvergence pessimism
  -0.09   11.74   library setup time
          11.74   data required time
---------------------------------------------------------
          11.74   data required time
          -5.79   data arrival time
---------------------------------------------------------
           5.95   slack (MET)



==========================================================================
global route report_checks -path_delay min reg to reg
--------------------------------------------------------------------------
Startpoint: core.CPU_inc_pc_a2[5]$DFF_P
            (rising edge-triggered flip-flop clocked by clk)
Endpoint: core.CPU_inc_pc_a3[5]$DFF_P
          (rising edge-triggered flip-flop clocked by clk)
Path Group: clk
Path Type: min

  Delay    Time   Description
---------------------------------------------------------
   0.00    0.00   clock clk (rise edge)
   0.00    0.00   clock source latency
   0.00    0.00 ^ pll/CLK (avsdpll)
   0.25    0.25 ^ clkbuf_0_CLK/X (sky130_fd_sc_hd__clkbuf_16)
   0.32    0.57 ^ clkbuf_3_4_f_CLK/X (sky130_fd_sc_hd_clkbuf_16)
   0.21    0.78 ^ clkbuf_leaf_4_CLK/X (sky130_fd_sc_hd__clkbuf_16)
   0.00    0.78 ^ core.CPU_inc_pc_a2[5]$DFF_P/CLK (sky130_fd_sc_hd__dfxtp_1)
   0.30    1.09 ^ core.CPU_inc_pc_a2[5]$DFF_P/Q (sky130_fd_sc_hd__dfxtp_1)
   0.00    1.09 ^ core.CPU_inc_pc_a3[5]$DFF_P/D (sky130_fd_sc_hd__dfxtp_1)
           1.09   data arrival time

   0.00    0.00   clock clk (rise edge)
   0.00    0.00   clock source latency
   0.00    0.00 ^ pll/CLK (avsdpll)
   0.25    0.25 ^ clkbuf_0_CLK/X (sky130_fd_sc_hd__clkbuf_16)
   0.33    0.58 ^ clkbuf_3_1_f_CLK/X (sky130_fd_sc_hd_clkbuf_16)
   0.21    0.79 ^ clkbuf_leaf_3_CLK/X (sky130_fd_sc_hd__clkbuf_16)
   0.00    0.79 ^ core.CPU_inc_pc_a3[5]$DFF_P/CLK (sky130_fd_sc_hd__dfxtp_1)
   0.00    0.79   clock reconvergence pessimism
  -0.03    0.76   library hold time
           0.76   data required time
---------------------------------------------------------
           0.76   data required time
          -1.09   data arrival time
---------------------------------------------------------
           0.32   slack (MET)



==========================================================================
global route critical path target clock latency max path
--------------------------------------------------------------------------
0

==========================================================================
global route critical path target clock latency min path
--------------------------------------------------------------------------
0

==========================================================================
global route critical path source clock latency min path
--------------------------------------------------------------------------
0

==========================================================================
global route critical path delay
--------------------------------------------------------------------------
5.7932

==========================================================================
global route critical path slack
--------------------------------------------------------------------------
5.9516

==========================================================================
global route slack div critical path delay
--------------------------------------------------------------------------
102.734240

==========================================================================
global route report_power
--------------------------------------------------------------------------
Group                  Internal  Switching    Leakage      Total
                          Power      Power      Power      Power (Watts)
----------------------------------------------------------------
Sequential             4.38e-03   5.23e-04   9.27e-09   4.90e-03  39.7%
Combinational          8.62e-04   2.06e-03   9.55e-09   2.92e-03  23.7%
Clock                  2.46e-03   2.05e-03   2.04e-09   4.51e-03  36.6%
Macro                  0.00e+00   0.00e+00   0.00e+00   0.00e+00   0.0%
Pad                    0.00e+00   0.00e+00   0.00e+00   0.00e+00   0.0%
----------------------------------------------------------------
Total                  7.71e-03   4.63e-03   2.09e-08   1.23e-02 100.0%
                          62.5%      37.5%       0.0%