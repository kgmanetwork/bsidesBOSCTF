# Forensics:
# Mercury Challenge

After downloading the mercury.zip file, use 'unzip' command to extract the file (Note: Don't use 'zip -d', it won't work)

The extracted file is a hidden file named '.hg', so instead of using 'ls', use 'ls' with -a flag to show all the hidden file

Use 'cd' command to change working directory to '.hg'. By using 'ls' again, a list of a bunch of files and directories are shown. If we look at all those files, that will be a waste of time
So, instead of doing individual files one by one, we will use 'egrep' ('egrep' is a command that will look at all files that we are specified, line by line, to find a specific pattern and in
this case, it is 'flag') But with 'egrep' alone is not enough, we want to look carefully into every single file inside subdirectories, so we will use -r flag to ask egrep to look at those
subdirectories too

Use the command

egrep -e 'flag' -r *

Result of using command:
![image](https://user-images.githubusercontent.com/71739262/94349373-cedd8480-0011-11eb-88d7-83134f47d309.png)

So there is a file inside store/data/ directory named _yz_u1_yz_rk_y_w_e4_o_tgz_nz_zh_nz_ey_n_d_qw_zj_ey_z_d_ji_n2_jl_nj_e_k.i that is matched with what we need, but because it is a binary
file, so we can't use 'cat' to see the content of it. Instead, we will use 'strings' command ('strings' is a command that shows all the 'make sense' character inside a binary file)

Use the command:

strings _yz_u1_yz_rk_y_w_e4_o_tgz_nz_zh_nz_ey_n_d_qw_zj_ey_z_d_ji_n2_jl_nj_e_k.i

The result:

uflag{version_control_for_the_solar_system}

We don't need the 'u' at the beginning, so get rid of it and submit the flag!

![image](https://user-images.githubusercontent.com/71739262/94349381-e3ba1800-0011-11eb-87b9-07e50ac2a5b9.png)

