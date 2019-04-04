--------------------------------------------------------------------------------
DISTFOLD - v0.1
--------------------------------------------------------------------------------
DISTFOLD is a modified version of CONFOLD that receives distances (in RR format) as input to build 3D models. It is not published yet. Please cite the original CONFOLD paper if you are using DISTFOLD.

--------------------------------------------------------------------------------
Install CNS Suite (last tested in a Ubuntu 16 system)
--------------------------------------------------------------------------------
1. To download CNS suite, provide your academic profile related 
   information at http://cns-online.org/cns_request/. An email
   with (a) link to download, (b) login, and (c) password
   will be sent to you. Follow the link, possibly
   http://cns-online.org/download/, and download 
   CNS suite "cns_solve_1.3_all_intel-mac_linux.tar.gz".
2. Unzip
```bash
tar xzvf cns_solve_1.3_all_intel-mac_linux.tar.gz
```
3. Change directory to cns_solve
```bash
cd cns_solve_1.3
```
4. Unhide the file '.cns_solve_env_sh'
```bash
mv .cns_solve_env_sh cns_solve_env.sh
```
5. Edit path in 'cns_solve_env.sh'; replace '_CNSsolve_location_' with CNS installation directory. For instance, if your CNS installation path is '/home/user/programs/cns_solve_1.3' replace '_CNSsolve_location_' with this path
```bash
vim cns_solve_env.sh
```
6. Test CNS installation
```bash
source cns_solve_env.sh
cd test 
../bin/run_tests -tidy *.inp
```
7. Change directory
```bash
cd ../../
```

--------------------------------------------------------------------------------
Configure and test 'distfold.pl'
--------------------------------------------------------------------------------
1. Update paths for the variables '$cns_suite' and '$program_dssp'
```bash
vim distfold.pl
```
```perl
my $program_dssp   = "$DIR_BASE/dssp-2.0.4-linux-amd64";
my $cns_suite      = "/home/bap54/CONFOLD2/confold2-v1.0/CNS-Suite/cns_solve_1.3";
```
2. Test the program:
```bash
cd test
rm -rf ./output
perl ../distfold.pl -rr ./1a3aA.dist.rr -ss ./1a3aA.ss_sa -o ./output
```

--------------------------------------------------------------------------------
Contact
--------------------------------------------------------------------------------
adhikarib@umsl.edu

