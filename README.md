# new
main.m
clc
clear
global busd lined filename
filename='powers3.xlsx';
busd = xlsread('busdatawo.xlsx');
lined = xlsread('linedatawo.xlsx');
powerflowdata
ybus
lfnewton
nrloadflow

powerflowdata.m
BMva = 100;
%--------READING BUS DATA-----------
bus = busd(:,1);
bustype = busd(:,2);
V = busd(:,3);
del = busd(:,4);
Pgen = busd(:,5)/BMva;
Qgen = busd(:,6)/BMva;
Pload = busd(:,7)/BMva;
Qload = busd(:,8)/BMva;
Qmin = busd(:,9)/BMva;
Qmax = busd(:,10)/BMva;
Qsh = busd(:,11)/BMva;
%--------READING LINE DATA-----------
lno = lined(:,1);
fb = lined(:,2);
tb = lined(:,3);
r = lined(:,4);
x = lined(:,5);
b = lined(:,6);
a = lined(:,7);
MVAlimit = lined(:,8);
%--------
nbus=length(bus);
nline=length(lno);
