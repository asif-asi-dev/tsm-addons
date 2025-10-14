# TSM OCA Addons
This repository contains custom OCA modules developed to support the TSM project.

# Make repositories bring to one point
1. git clone https://github.com/asif-asi-dev/tsm-addons.git
2. cd tsm-addons
3. mkdir oca_sources
4. cd oca_sources
5. Add all repos are submodule
    - git submodule add -b 16.0 https://github.com/OCA/account-financial-reporting.git account-financial-reporting <br>
    - git submodule add -b 16.0 https://github.com/OCA/account-financial-tools.git account-financial-tools  
    - git submodule add -b 16.0 https://github.com/OCA/account-reconcile.git account-reconcile
    - git submodule add -b 16.0 https://github.com/OCA/cfed_tsm.git cfed_tsm
    - git submodule add -b 16.0 https://github.com/OCA/ddmrp.git ddmrp
   
7. cd ..
8. git add .gitmodules oca_sources/
9. git commit -m "Added 30+ OCA repos as submodules"
10. git push origin main
11. mkdir oca_addons
12. create merge_oca_addons.sh file with below detail
13. chmod +x merge_oca_addons.sh
14. 
      
# To clone to local
git clone --recurse-submodules https://github.com/asif-asi-dev/tsm-addons.git
git pull --recurse-submodules
git submodule update --remote --merge
./merge_oca_addons.sh


# If you already cloned without submodules
git clone https://github.com/asif-asi-dev/tsm-addons.git
cd tsm-addons
git submodule update --init --recursive
git pull --recurse-submodules
git submodule update --remote --merge
./merge_oca_addons.sh




