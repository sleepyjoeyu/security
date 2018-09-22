scap-check,yml
- Based on {{ scap_profile }} to trigger RHEL6/7 openscap scanning 
- Fetch the final report file to ansible host (/data, must allow awx to read/write)
- The report will be put into a folder named by its hostname.



check-change.yml
- Based on {{ check_path }} to select the template source to compare with managed node's file content
- {{ check_path }} should include the complete folder structure and file.
  ie. {{ check_path }}/etc/sysctl.conf will be used to compared with managed node's /etc/sysctl.conf 
- admin can keep multiple {{ check_path }} as the different target template source. So it could be easier to check with 
  different pourpose service, ie. AP, DB, etc 

