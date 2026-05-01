RVT / standard NMOS:  
ndiff + nsdm + poly crossing  

LVT NMOS:  
ndiff + nsdm + poly crossing + lvtn marker  

### pmos lvt  
* W: 1.25um, L=0.5um

1. öncelikle pdiffusion bulunur.  
![1](magic/mos/pmos_lvt_1_source-drain.png)
 
2. ptranstistor ile transistor alanı oluşturulur.  
![2](magic/mos/pmos_lvt_2_ptransistor.png)

3. poly silicon extension bunulur.  
![3](magic/mos/pmos_lvt_3_polysilicon.png)

4. poly contant(pc) ile polysilicon <> locali bağlantısı yapılır.  
![4](magic/mos/pmos_lvt_4_pc.png)

5. pdiffusion contact(pdc) ile diffusion <> locali bağlantısı sağlanır.
![5](magic/mos/pmos_lvt_5_pdc.png)

6. locali ile gate, source drain contactları local interconenct seviyesine çıkarılır.  
![6](magic/mos/pmos_lvt_6_locali.png)

7. viali: locali katmanından bir üst metal katmana geçmek için kullanılır.  
   viali genellikle pdc, pc ile aynı boyutta tutulur.  
![7](magic/mos/pmos_lvt_7_viali.png)

8. metal1 ile tüm contact'lar metal1 seviyesine bağlanır.  
![8](magic/mos/pmos_lvt_8_metal1.png)

### nwell bulk
1. nwell yerleştirilir.
2. nsub_ndiff yerleştirilir. ve bu sayede nwell içinde n kuyusu açılır.
![2](magic/mos/nwellBulk_2_nsub_ndiffusion.png)

3. ndiff_ncontact, ile ndiffusion locali'ye bağlanır.  ndiffusion <> locali
![2](magic/mos/nwellBulk_3_ndiffusion_ncon.png)

4. locali katı
![2](magic/mos/nwellBulk_4_locali.png.png)

5. metal katı otomatik gelmezz!
