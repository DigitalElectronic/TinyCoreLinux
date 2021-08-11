# TinyCoreLinux
![8b8cfc5c57dfd820ed3d4e0728fb9295](https://user-images.githubusercontent.com/74788266/128921665-7f5be774-3c25-4910-81b1-142a860e4890.png)

<b>1º Download the image .ISO AutoBoot.</b>

    http://tinycorelinux.net/12.x/x86/release/TinyCore-current.iso

   

<b>2º Go to repository list web to select name of Application, The system have indiviual build.</b>

    http://distro.ibiblio.org/tinycorelinux/3.x/tcz/
    
    
3º <b>To install you need push the Right Button Mousse and Go to System-Option and click in where say Apps.</b><br>

![111111](https://user-images.githubusercontent.com/74788266/128923314-730ebd20-d905-43f0-bc27-58cdddaf1b71.jpg)
________________________________________________________________
Select the mirror where you want download the applications.  <sub> Repository APPs</sub> <br> 


 Go to /App/Browser and wait to the list.
_____________________________________________________________________________
<b>4º You need this "Apt" to minimal compiler ARM.</b>


            git.tcz
            
                compiletc.tcz
                                         
                       grub2-multi.tcz                       
                        
                                  unzip.tcz
                                  
                                       ncursesw-dev.tcz

_________________________________________________________________

    
    
<table class="editorDemoTable">
<tbody>
<tr>
<td><strong>Cross Compiler</strong></td>
</tr>
<tr>
<td>U-Boot</td>
</tr>
<tr>
<td>Compile C+ Code</td>
</tr>
<tr>
<td>Make Binary Files</td>
</tr>
</tbody>
</table>

<b> 2º How create a Binary Files </b>



![Acorn_Archimedes_A3020_2190336806](https://user-images.githubusercontent.com/74788266/129021458-73fac55d-ee6a-43ac-b79f-e848d483f7d5.jpg)




![cc](https://user-images.githubusercontent.com/74788266/128943365-bf02fa58-c99a-4481-a650-a212c5d9b1ff.png)

        May be clone repository.
        You need go to Folder u-boot/confgis/ to copy the name of board selected to command write. Example-> rpi_2_defconfig 


<b>1º Source Code Links Repository.</b>

        https://github.com/ARM-software/u-boot.git
      

 <b>2º Compile the folder with board configuration </b>
 
        Go to terminal and folder "u-boot".
        Write this commands:
                          make ARCH=arm rpi_2_defconfig 
                          make ARCH=arm CC=gcc rpi_2_defconfig 
                          make
                          
         Now you have a new .config file.         
         
         
 <b>3º Create Image or Binary Files depend how you desing.</b>       
 
            
            Write this;
            
               grub-mkimage 
               
               grub-mkimage -c u-boot.cfg -o 23.bin -O x86_64-efi -p boot
                  or 
               grub-mkimage -c u-boot.cfg -o 23.img -O x86_64-efi -p boot
               
               
   <b> 4º Adittional <b>
    
         
            # To more option in the output file write "grub-mkimage" to read help.
                 Or go to https://zoomadmin.com/HowToLinux/LinuxCommand/grub-mkimage you can look the options avaliable.
              
            # Now you have the files in the same folder where you compile before.
            
         
