#!/bin/bash
###################################################################################
# Fix ESXi & Unbuntu noisey syslog bug 
# For Ubuntu 20.04.4
# David Harrop 
# June 2022
# kills a stream of of sda syslog entries that makes syslog annoying to work with 
###################################################################################

cat <<EOF | sudo tee -a /etc/multipath.conf
blacklist {
  device {
    vendor "VMware"
    product "Virtual disk"
  }
}
EOF

sudo systemctl restart multipathd.service
