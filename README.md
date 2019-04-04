--------------------------------------------------------------------------------
DISTFOLD - v0.1
--------------------------------------------------------------------------------
DISTFOLD is a modified version of CONFOLD that receives distances (in RR format) as input to build 3D models. It is not published yet. Please cite the original CONFOLD paper if you are using DISTFOLD.

--------------------------------------------------------------------------------
Installing CNS Suite
--------------------------------------------------------------------------------
1. To download CNS suite, provide your academic profile related 
   information at http://cns-online.org/cns_request/. An email
   with (a) link to download, (b) login, and (c) password
   will be sent to you. Follow the link, possibly
   http://cns-online.org/download/, and download 
   CNS suite "cns_solve_1.3_all_intel-mac_linux.tar.gz".
2. Unzip
```bash
   $ tar xzvf cns_solve_1.3_all_intel-mac_linux.tar.gz
```
3. Change directory to cns_solve
   $ cd cns_solve_1.3
4. Unhide the file '.cns_solve_env_sh'
   $ mv .cns_solve_env_sh cns_solve_env.sh
5. Edit (a) 'cns_solve_env.sh' and (b) 'cns_solve_env' to replace
   '_CNSsolve_location_' with CNS installation directory.
   For instance, if your CNS installation path is
   '/home/user/programs/cns_solve_1.3' replace
   '_CNSsolve_location_' with this path
6. Test CNS installation
   $ source cns_solve_env.sh
   $ cd test 
   $ ../bin/run_tests -tidy *.inp


--------------------------------------------------------------------------------
Contact
--------------------------------------------------------------------------------
adhikarib@umsl.edu

