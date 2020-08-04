# rss_HumanHaman
This dataset consists of RSS data measured from smartphones carried by two human beings. Two users were required to stand at a certain distance from each other. In particular, distance = {0.2:0.2:2, 3:1:5}. For each distance, both smartphones will broadcast a BLE packet and also scan for the incoming packet for about 1min. The App is configured to log the following information: the truth distance, name of smartphone, MAC address of BLE chipset, the packet payload, RSS values, time elapsed, and timestamp. Two smartphones were used. The name of the smartphones is set to gryphonelab and HTC One M9, respectively. 

# Consolidated Dataset
The smartphone also collected BLE packets from other BLE devices in the vicinity. Hence, we only consolidate the data from the two smartphones used in this experiment and exclude the BLE packets from other devices. Furthermore, we also apply a moving average filter to obtain a much smoother RSS value. The timestamp, packet payload and MAC address are discarded as some of them contain sensitive information while other might not convey meaningful information. The final consolidated dataset consists of the following information:
<ul>
  <li>device name,</li>
  <li>time elapsed,</li>
  <li>rss (raw RSS value),</li>
  <li>mRSS10 (filtered RSS value with window size = 10),</li>
  <li>mRSS100 (filtered RSS value with window size = 100),</li>
  <li>distance, and</li>
  <li>label </li>
</ul>
** You can find these descriptions in the first row of each csv file.

We labeled the contact into high-risk contact and low-risk contact according to the distance between any two users. Specifically, a user is considered to be a high-risk contact when he/she has been in proximity (i.e., with distance less than the recommended physical distancing rule (2m)) with the infected individual.


# Body Positions
Both users were required to carry the smartphone on 3 different body positions.
Hence, there are 6 sets of measurement data, each set corresponding to different combination of body positions, as shown in Figure below.

<p align="center">
  <img alt="Smartphones carried by users on different body positions" 
       width="500" height="378"
       src="/_Figure/bodyPosition.png" />
</p>

The total data points for each experimental set is summarized as follows:
<ul>
  <li>Hand-to-hand (HH): 19,903</li>
  <li>Hand-to-phone (HP): 16,081</li>
  <li>Hand-to-backpack (HB): 10,330</li>
  <li>Pocket-to-backpack (PB): 19,161</li>
  <li>Pocket-to-pocket (PP): 24,151</li>
  <li>Backpack-to-backpack (BB): 34,092</li>
</ul>
You can find the measurement data for each of the above combination in the corresponding folder. 
In each folder, there are three csv files. The first one contains all the data, whereas the other two are the training and testing data.
In particular, we used 80%-20% rule when dividing the data into training and testing sets.

# Paper
Refer to the following paper for more information.
P. C. Ng, P. Spachos and K. N. Plataniotis, "COVID-19 and Your Smartphone: BLE-based Smart Contact Tracing," in IEEE System Journal, vol. x, no. x, pp. xx-xx, 2020 (submitted).
Preprint: https://arxiv.org/abs/2005.13754#:~:text=COVID%2D19%20and%20Your%20Smartphone%3A%20BLE%2Dbased%20Smart%20Contact%20Tracing,-Pai%20Chet%20Ng&text=The%20proposed%20Smart%20Contact%20Tracing,quickly%20determined%20the%20contact%20profile.


# Preliminary
The RSS distributions of each experimental set are shown as follows:
<p align="center">
  <img alt="Smartphones carried by users on different body positions" 
       src="/_Figure/hh.png" />
</p>

<p align="center">
  <img alt="Smartphones carried by users on different body positions" 
       src="/_Figure/hp.png" />
</p>

<p align="center">
  <img alt="Smartphones carried by users on different body positions" 
       src="/_Figure/hb.png" />
</p>

<p align="center">
  <img alt="Smartphones carried by users on different body positions" 
       src="/_Figure/pb.png" />
</p>

<p align="center">
  <img alt="Smartphones carried by users on different body positions" 
       src="/_Figure/pp.png" />
</p>

<p align="center">
  <img alt="Smartphones carried by users on different body positions" 
       src="/_Figure/bb.png" />
</p>


