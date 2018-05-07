### Horizontal Filtration, Spring 2018
#### Clare O'Connor, Corson Chao, and Christopher Galantino
#### 5/7/2018

<div class="alert alert-block alert-danger">
Please do not delete my comments. On the next submission I will use them to see if the issues were addressed and then I will delete them. If you disagree with a comment, just add your own underneath it.
</div>

## Abstract
Horizontal filtration is a completely new innovation for the AguaClara team, arising from a desire to make the 1 L/s plants easier to make and ship through replacing the Enclosed Stacked Rapid Sand Filter. To create a horizontal filter, aspects of the sedimentation tanks and current filter design will be used, such as the relationship between backwash and operational speed, as well as the design of the plate settlers. Initial experimentation with the settling of sand during upflow demonstrated the feasibility of angled plates as a method of sand retention.



<div class="alert alert-block alert-danger">
~Focus on concise writing. Use as few words as possible to get your point across.

~Consider explicitly stating that your goals are to design and build a horizontal filter.
</div>

## Table of Contents
1. Introduction
2. Description of Apparatus
3. Challenges and Future Work
4. Manual
  - Special Components
  - Fabrication Details
  - Design
    - Python
    - Fusion360
  - Experiments
      - Methods


## Introduction

The AguaClara plantita (1 L/s plant) is a difficult apparatus to construct and implement. Finding a way to make fabrication, assembly, and installation simpler, as well as downsize components, will greatly decrease the cost and make the technology more accessible for global communities.

The concept of an easy to implement, versatile water treatment plant correlates nicely with the [OrigamiWaterLab](https://github.com/OrigamiWaterLab) proposed by AguaClara engineer [Ethan Keller](https://github.com/ethan92429). OrigamiWaterLab is the concept of creating a easily producible filtration system, built from easily transportable flat parts, similar in concept to the creation of origami. Essentially, ingenious engineering is found in simplicity and resiliency. Fabricating a plant that transitions from flat into 3D is a innovative area of study that may become more possible with increased exploration. With more work, this concept could become a new direction for AguaClara plants.

With this idea in mind, one of the most difficult features to construct efficiently is the filter, which is both time and labor intensive to create. Currently, the 1L/s plant’s filter is characterized by a vertical, enclosed stacked rapid sand filter (EStaRS) which is tall and cumbersome to ship in addition to having a complicated geometry of 4 inlet manifolds and 3 outlet manifolds.

<div class="alert alert-block alert-danger">
great improvement. For next submission focus on continuing to revise for concise and crisp writing.
</div>

To combat these difficulties, the horizontal filtration team has proposed a horizontal filter design. This filter will not be stacked. Instead, it will use horizontal flow for filtration and vertical flow for backwash. The ratio of the horizontal flow area to the vertical flow area will be designed so that the bed will fluidize during backwash. The inlet and outlets will be designed so that sand/water separation doesn’t require slots. Additionally, this innovation in the horizontal filter could ultimately eliminate the need for slots on the OStaRS (Open Stacked Rapid Sand) filter, as is used in the full-size AguaClara plants. In the horizontal filter, water will enter and exit through a geometry that has a plate settler style design to ensure that sand settles out and isn’t carried into the effluent. This design for the horizontal filter will utilize both current filtration techniques and technologies from the plate settle design in the sedimentation tanks.

The goal is that these design innovations will simplify the current design and facilitate scaleup and mass production of AguaClara technologies.

## Apparatus

The follow section describes the first iteration of the horizontal filter. Upon it's construction, the team determined that further iterations would be needed to build a filter with components that are precise and consistent. In response, the team designed a full Fusion360 model of the filter assembly, on which the next iteration will be based. This Fusion360 plan has been attached in the Manual of this report and includes current and past designs. In this section, the explanation of the apparatus will focus on the challenges with this design, and the changes that were made in the updated design.

<div class="alert alert-block alert-danger">
Minor spelling/grammar issues
</div>

* Design
  - As an overview, the horizontal filter consists of 4 main parts: the acrylic box, the entrance/exits plates, filter shelves, and the center plates. In Figure 1 below, each of those parts are labelled.

<center>

|  ![]()<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/images/labeled_real_box.PNG?raw=true" >|
|:----:|
| Figure 1: This is a photo of the apparatus as currently constructed.|
</center>

<div class="alert alert-block alert-danger">
~fesf?

Figure X?
</div>

  -   Acrylic Box: The box was bought premade from a website (See list of parts below) It has a thickness of 1/4" and its size is the overarching constraint of the design.

  <div class="alert alert-block alert-danger">
~bow?

No period at the end of a sentence
  </div>

  - Entrance and Exit plates: In the side-view image, the entrance and exit plates are only minimally seen. Though not yet constructed in reality, a thickness of 1/4" will be sufficient for those walls.
  - Filter Shelves: In the built filter there are 36 filter shelves which act as retaining plates for the sand in the filter by providing a surface for the sand to settle on to, and by blocking the exit holes. As built, the plates are angled at 60 degrees from the horizontal with an angle cut underneath on the outside edge to help the shelves fit more snugly against the inside walls of the entrance and exit plates. At angles steeper than 60, this additional cut proved impossible to fabricate.  In the updated design the shelf angle was changed to 55 degrees so the additional outside angling would be possible. In addition the space constraint of the shelves changed slightly with the change in angle, so that in total there will be fewer shelves on each side. Below is an image of the filter shelves being inserted in to the  insert assembly. Note the acrylic shelves; these will be 1/8" PVC in the next iteration ,as the acrylic was extremely brittle and offered no flexibility if the shelves were not cut perfectly and would snap during insertion and removal.

  <div class="alert alert-block alert-danger">
revise for spelling/verb use

center all figures and label them all. Refer to them by their figure #.
  </div>

  <center>

  |<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/images/inserting_shelves4.jpeg?raw=true" >|
  |:---:|
  |Figure 2: Construction of the filter insert.|

  </center>



  - Center plates: The center plates support the filter shelves. As built, two center plates are used separating the filter into three sections. In the new model there will be three center plates, one in the center and two  that are one inch from the edge of the box. Notches are cut in the plates to allow the filter shelves, which are also notched, to fit together without coming loose.  Using three plates instead of two will prevent the shelves from warping and developing an uneven spacing as seen in the image. In addition, corners will be cut out to allow water to run between the sections in the filter, in the channels under each shelf. This can be seen with more description in the Manual section.

#### Additonal parts  
  Several additional parts will be necessary to develop once the filter in forward operation is functional. One of these is the siphon system. The siphon is used to initiate the upward flow in the filter. While designing a siphon isn't difficult on its own, the challenge will come from sealing it into the top of the box while maintaining the ability to adjust the filter insert should maintenance be necessary . This will require a robust gasket system, which is the other major additional component of the system. To seal the edges of the plates within the tank a gasket will be necessary as well, but given that that gasket will be static within the system it should be simpler to design than the top backwash gasket.
## Future Work


As the Horizontal filtration team continues, fabricating the update design will be priority. This will include creating a jig, from which the filter shelves and center plates can be constructed, as well as using a CNC machine to make the entrance and exit plates. From there, adding EPDM foam gaskets will allow tests of the system in forward filtration mode. After success in forward filtration, efforts can be made to develop the components for backwash, most importantly the siphon system and the backwash doors. Developing a good seal in the doors is likely to be the largest challenge. Further work beyond backwash could go into constructing the system so that the siphon valve is connected to the backwash doors making it easier to operate.


  <div class="alert alert-block alert-danger">
  Delete the prompt

  Consider explaining what the siphone and gasket are in the apparatus section.
  </div>

# Manual
  This section outlines fabrication and component details not otherwise specified in the body of the report.

  <div class="alert alert-block alert-danger">
  Delete te prompt
  </div>

## Special Components

Acrylic Box: An acrylic container of specifications 18x18x24" bought from [Shop Pop Displays](http://www.shoppopdisplays.com/P_PED-ACRYLIC-CLEAR-FLAT/clear-acrylic-pedestal.html) in order to act as an observable smaller model of the designed horizontal filter.

Ethylene Propylene Diene Monomer Rubber(EPDM): Sheets of EPDM will be used as seals to cover the holes in the entrance and exit plates during backwash. EPDM will also be used in maintaining water tightness when potentially using gaskets for sealing. (McMaster-Carr)

PVC Sheets: Sheets will be cut into the forms of the shelves, entrance/exit plates, and the filter shelf holders. (McMaster-Carr)

Aluminum Angle Iron: Stabilizer for one version of the gasket system. (McMaster-Carr)

1/8" Router Bit: Router will be used to cut holes in PVC (McMaster-Carr)

Stainless Steel Phillips Screw, Washer, Split Lock Washer, Hex Nut: These components will be used to fasten the gasket system securely to the tank. (McMaster-Carr)

<div class="alert alert-block alert-danger">
Include where to get these from?

What is EPDM

Last entry is formatted differently from the rest.
</div>

## Fabrication Details


####  Initial Filter design

<div class="alert alert-block alert-danger">
~Remove hyphen from the header.
</div>

1. Center plates- the center plates were cut to shape using the band saw.  The slits were cut by making 1/8" holes using the drill press, 1/8"  was chosen as it is the thickness of the filter shelves. Drilling the holes made it possible to keep a fairly straight cut to the proper depth while avoiding the problem of having two cuts and no way to get the middle out. The location of the holes and the angle of the cut was pre-drawn onto the PVC. In future iterations it is recommended that a stencil be cut out, and then the plates be cut using a CNC Router as following the stencil. This will likely provide more control and uniformity between cuts.
<center>

|<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/images/Hole%20cut.JPG?raw=true" >|
|:---:|
|Figure 3: This sketch illustrates the fabrication method used to cut notches in both the center plates and filter shelves. The blue circle was drilled out first, then two cuts parallel to the outer edges of the hole were made using the band saw. This technique left a rounded notch in the plates, but maintained a decent degree of consistency over made cuts.
</center>
<div class="alert alert-block alert-danger">
~Photos for these steps? It is hard for me to picture.

</div>

2. Filter shelf - The filter shelves were cut from a sheet of 1/8" PVC. To cut in the notches into the shelves the same techniques as with the filter plates was used, but varied for the different thickness. First a 1/4" hole (for the thickness of the center plates) was drilled at a measured location on the shelf with the drill press. The location of the notches depends on the number and location of the center plates. In the built model this was chosen to be at the 1/3 and 2/3 distances along the width of the shelf, to create 3 even sections. The update design, however, uses 3 plates.  Upon drilling the holes, the notch was cut using the band saw. To get the angled edge of the shelf, a jig was constructed, first by the team and later by Tim Brock, of the machine shop. The jig provided an angled surface to attach the shelf through as it was led through the band saw at an angle. This process required much precision and care. While it works, potential other methods of shelf fabrication should be explored. One option is to cut the shelves at an angle as a first step, to avoid needing to shave thin strips after holes have been drilled. this would save time and be less wasteful of the plastic.

<div class="alert alert-block alert-danger">
How did you predetermine the location for the 1/4" hole?

Revise the sentence "This process required much precious and care"

Why should other options be explored? What were the problems?
</div>

3. Entrance/Exit Plates - Currently, the entrance and exit plates are only fabricated so they fit into the acrylic box. The main plates were cut in the machine shop using the large bandsaw and sanded so they would sit flush in the box. The team expected a change in methods and decided not to proceed with cutting the holes.

<div class="alert alert-block alert-danger">
Again - be consistent with formatting

Please use full sentences
</div>

##### Preliminary Gasket work
  Some work was started on designing the gasket system for the filter. Aluminum Angle Iron was cut and drilled, as was EPDM rubber. This process proved unreliable as a fabrication method for several reasons including: inexperience with the materials, incomplete Fusion360 design, and imprecision with the methods, once of which involved freehanding a cut in the EPDM while it was held down by several clamps. More exploration in this area will be done. One potential option is to use EPDM foam rather than EPDM. EPDM foam is a rubbery foam that may compress more evening with fewer components, though it will need to be purchased and tested for ease of use as well as water tightness.

<div class="alert alert-block alert-danger">
Revise for spelling.

Rethink the first sentence, it is a filler.

Remember to mention the gasket in the apparatus section above so that we know what it is used for.
</div>


## Python Code, Fusion, and Calculations

<div class="alert alert-block alert-danger">
Consider calling this section Design with python code, fusion as subheaders.
</div>

The following will be a combination of calculations and [Fusion](https://cornell47.autodesk360.com/g/projects/20180202115885156/data/?tryNew=true) drawings to serve as a guide in how the filter was designed and to provide a visual representation for each measurement.

The purpose of this filter assembly is for simplicity and easy fabrication. The filter exists within an acrylic box with an inflow and an outflow as the empty cavities that don't contain the sand filtering section. The sand column section itself exists in the middle of the filter box with a filter shelf insert that can be added or removed. The image below is a cross-sectional view of the overall filter concept. While the filter gates are open, water flows in through one side, experiences sand filtration, and then exits out the other side as clean effluent. The angled pieces in the middle are the filter shelves which serve to keep sand out of the influent/effluent channels.

<center>

|![filter_assembly](https://github.com/AguaClara/horizontal_filtration/blob/master/images/filter.jpg?raw=true)|
|:---:|
| Figure 4: Schematic of the first iteration of the filter|
</center>

<div class="alert alert-block alert-danger">
This section really confused me and I still don't fully understand the apparatus? What part is the sand? Can you add labels to the drawing with the major aspects.

Also please label all figures with numbers and captions!

Also thoroughly revise the paragraph description for clarity and understanding.
</div>

The team first calculated the dimensions of the sand filter space which will make up a section of the overall apparatus. To do this, HorFi (Horizontal Filtration Team) took into account the velocity at which water moves through a sand filter and the desired flow rate of the system. As the goal was to create a model, the size constraint on the filter was determined by what size box would be easy to use. This constraint resulted in a filter with a 0.37 L/s flow capacity.
<div class="alert alert-block alert-danger">
Change of verb tense.

Be consistent throughout

Also before you referred to yourself as "the team" now you are "HorFi" (Pick one or the other)
</div>

Since the backwash velocity (V_backwash) is necessarily greater than the filter velocity (V_filter) as the volumetric flow is the same while cross-sectional area is less, it is the principal design constraint. With some math, the area of backwash (A_backwash) and area of flow (A_flow) may be calculated.


With these dimensions calculated, the filter box can then be rendered as seen below.
<center>

|![filter_box](https://raw.githubusercontent.com/AguaClara/horizontal_filtration/master/images/filter_box.JPG)|
|:---:|
|Figure 5: Rendering of the outermost box of the filter. Within this box the filter insert will be placed. This geometry constrains much of the design.|

</center>


<div class="alert alert-block alert-danger">
Technical writing errors.

I'm confused by the blue lines? Will they be placed across the middle one? Inconsistent with later figures.
</div>

The entrance and exit plates are what separate the inflow and outflow from the body of the sand filter as well as confine the filter shelf assembly. They are perforated to allow the flow of water.

<div class="alert alert-block alert-danger">
fix "confien"

How big are the perforations?
</div>
<center>

|![entrance_exit_plates](https://github.com/AguaClara/horizontal_filtration/blob/master/images/Filter_entrance_exit_plates.JPG?raw=true)|
|:---:|
|Figure 6: Rendering of entrance plates with hole design. The holes are located with 2 at each filter shelf with the height above the filter shelf defined as 1 cm. The layout of the holes was staggered to prevent too high of a stress at a location where all the holes were lined up.|
</center>

<div class="alert alert-block alert-danger">
How did you decide how many holes and where to put them?
</div>

These plates may then be placed within the filter box, as seen below. Depending on the length of the filter insert assembly, the spacing of the plates will be adjusted accordingly, as the length of the filter insert, as set by the length of the filer and flow constraints, determines how far apart the entrance and exit plates need to be. The idea is that they would be fully secured once the apparatus is in use and only the insert would remain removable.

<div class="alert alert-block alert-danger">
How does the width of the filter insert assembly affect the spacing of the plates?

What is the filter insert assembly?
</div>

<center>

|![filter_box_plates](https://raw.githubusercontent.com/AguaClara/horizontal_filtration/master/images/filter_box_plates.JPG)|
|:---:|
|Figure 7: Rendering of the entrance and exit plates placed into the fitler box|
</center>

Between these plates will be the filter shelf insert, a series of suspended, angled shelves that serve to both shelter the holes during routine filtration and also return sand during backwash. Below is a filter plate, a component of the filter shelf insert that keeps the filter shelves rigid and at the correct height.

<center>

|![filter_plate](https://github.com/AguaClara/horizontal_filtration/blob/master/images/Filter_plate.JPG?raw=true)|
|:---:|
|Figure 8: A center plate|
</center>



The notches are where the shelves and the bottom plate are placed. The bottom plate serves as a recirculator. During backwash, there is the possibility that dead zones in the far side of the filter will occur. To remedy this, the angled bottom plate provides an upward path for incoming water to ensure all sand is cleaned. Below is a filter shelf followed by the bottom plate. The angle was set at a minimum of 15 degrees.
<center?

|![filter_shelf](https://github.com/AguaClara/horizontal_filtration/blob/master/images/Filter_shelf.JPG?raw=true)|
|:---:|
|Figure 9: A filter shelf|

|![bottom_plate](https://github.com/AguaClara/horizontal_filtration/blob/master/images/Bottom_plate.JPG?raw=true)|
|:---:|
|Figure 10: Replace this

</center>

The current plan is to have 3 of the plates perpendicularly oriented with respect to the entrance and exit plates to provide support for the long filter shelf pieces. This following image depicts this concept.

<div class="alert alert-block alert-danger">
I don't see perpendicular plates?

How would that add to the stability?
</div>

![filter_assembly](https://github.com/AguaClara/horizontal_filtration/blob/master/images/Insert_assembly_front_plate_removed.JPG?raw=true)

The number of filter shelves to add is determined by the distance between respective shelves. This will be optimized by investigating how far sand will travel before settling on the plates due to the velocities of this system. This was performed experimentally (see earlier in the report) as well as theoretically below. The team considered both laminar and turbulent settling velocity situations.

<div class="alert alert-block alert-danger">
It was briefly mentioned in the abstract, but where are the actual results of this section.

Do not refer to anything as "above" or "below". There are many things above and below. Give it a label and refer to that label.
</div>






<div class="alert alert-block alert-danger">
reconsider use of "constructed" in the first sentence.

Somewhere along the line I confused filter plates and filter shelves.

Try not to interrupt thoughts with images. As I read this, I am noticing that I am struggling with comprehensive due to the organization of the report. The text is so fragmented.
</div>





<div class="alert alert-block alert-danger">
Are these channels inside the sandy area?

Is this a top down view?
</div>


<div class="alert alert-block alert-danger">
What is this figure?
</div>


<div class="alert alert-block alert-danger">
I am confused about the purpose and fabrication of this channel.

Also still confused about where the sand is.
</div>



# Appendix

### Experiments

#### Methods

To determine the initial parameters, the team conducted several experiments with the flow of water in relation to the sand. These experiments were done to verify hypotheses when calculations didn't yield conclusive answers. The experiments focused on determining the length of the filter shelves, the adapted plate settlers, which would allow sand to settle before climbing into the outlet and flowing out of the filter. To do this two tests were run.

Two similar apparatuses were constructed to determine the length of the filter shelves based on how sand settled in angled tubes of different diameters. The first setup included a 1" diameter pipe as the filter body and 1/8" tube as an angled outlet(Figure 1) Forty-five degrees was chosen as the angle to allow the most sand to fall while not changing the flow too much. Sand, then water were poured in to see if sand would travel into the outlet during startup conditions. It did. From there the pumps were turned on to mimic water flow during filtration and backwash. The speed in the filter body was set to be the speed required for backwash, 9mm/s, and the speed in the angled outlet was set to the speed during operation 1.8mm/s as that is the maximum water velocity that should be experienced within the filter shelves. Upon completion of this test, a new apparatus was constructed.
<center>

| ![apparatus for testing length of filter shelves](https://github.com/AguaClara/horizontal_filtration/blob/master/images/small_diameter_outler.jpg?raw=true) |
|:--:|
| *Figure 1. First experimental apparatus with 1" diameter filter and 1/8" outlet tube. Influent water comes in through the bottom and out through the angled outlet and the top.* |
</center>

The original idea for the new apparatus was to have a 1" angled tube stemming from the 1" filter. This proved nearly impossible to fabricate, so as in Figure 2, a 3/4" angled outlet pipe was used instead. In this test, the same steps were taken, dry sand was poured to determine how sand would travel. Then water was added, which caused sand to move several inches up into the outlet tube. However, the level of sand retreated once the pumps were turned on and operating at backwash and operational speeds. More elaboration on these filter experiments are below in experimental procedures.

<center>

| ![apparatus for testing length of filter shelves](https://github.com/AguaClara/horizontal_filtration/blob/master/images/one_inch_outlet.jpg?raw=true) |
|:--:|
| *Figure 2. Second experimental apparatus with 1" diameter filter and 3/4" outlet tube. Influent water comes in through the bottom and out through the angled outlet and the top.* |
</center>

## Experimental Methods

### Filter Shelf Length Tests
  Several tests were run in order to determine the upflow path of sand during backwash. A tube was used to simulate the main body of the filter  with a smaller angled tube branching off the main body. The outlet branch allowed the team to measure how far sand would rise in the outlet, which could inform the length of the filter shelves given the velocities expected in the filter. Additionally, an understanding of the speeds required to drive sand into an outlet could further inform aspects of the OStaRS, specifically the necessity of the slotted pipes.

<div class="alert alert-block alert-danger">
~~fix these tests were ran"
</div>

#### Experiment: 1" and 1/8"
1. First a mock filter was constructed using a 1" clear PVC pipe; in this pipe an angle hole was drilled at 45 degrees from the vertical around 5 inches from the top of the pipe. Into this hole, a small length of 1/8" tubing cut on one end to an angle of 45 degrees was inserted and glued. See Figure 1 above for an image of the apparatus.
2. Dry sand was poured from the top into the apparatus to see if dry sand would move up the outlet tube when the sand level was two inches above the angled outlet. It did not.
3. An additional 500g of sand were poured in increments of 100g, this corresponded with an additional height of about 1.5ft in the 1" pipe. At no point did dry sand enter into the outlet tube.
4. Water was then slowly added into original amount of sand, during this process water carried sand into the first inch of the outlet tube.
5. Pumps were checked for proper flow rate to get proper water velocity in the outlet tube as corresponding to the outlet diameter and speed required for backwash and operation speed. The water within the body of the filter was moving at a speed required for backwash and the outlet pull was at the speed required during operation as that should be the maximum velocity experienced in the filter shelves.
6.Water was then pumped through the very wet sand. Sand moved around 3 inches up the length of the outlet tube. Preferential flow paths were observed as the apparatus was tilted.

#### Experiment: 1" and 3/4"

1. Originally, the plan had been to use 1" and 1" but fabrication of the experimental apparatus was extraordinarily challenging, so the outlet tube dimension was changed to reflect what was possible to construct. Because of this a 3/4" inch pipe was used instead. Using a hole saw an angled hole was drilled in to the main 1" tube. The 3/4" pipe was then also cut on one end with the same size hole saw bit. This meant that the curvature of each piece fit together more snugly than had the 3/4" pipe been sliced flat. Then the two pieces were welded together.
2. Sand was poured into the container to a level of around 4 inches above the opening of the angled outlet. Sand settled slightly into the angled tube.
3. The apparatus was filled with water, and the inlets and outlets were hooked up to their respective pumps and waste lines. At this point the sand rose in the outlet column to a length of around 3 inches.
4. The pumps were reset to work at the new speeds needed to pull water through the outlet at 1.8mm/s and through the main filter at 9mm/s. As the sand in the main column fluidized the sand dropped in the outlet column down to a length of 1.1" which remained constant over the several minutes the pumps were on.
5. The pumps speeds were altered away from what would be useful during operation to develop a sense for what effect that could have on the effectiveness of the filter shelves. Below is a table of the values obtained.

<div class="alert alert-block alert-danger">
These two procedures seems similar. Can there just be one set of procedures then simple xplanations about the size differences?

Clare- I considered that thye were very similar but for clarity's sake I though it would be better to have them separately, as they are a bit different. I find that writing parallel procedures as one unit requires the reader to hold too much information at once. I will, however, add a brief sentence to mention the similarity.
</div>

<center>

#### **Table of  pump speed and sand length in outlet tube**
|filter speed (RPM)|outlet speed (RPM)|sand length in tube (in)|
|:---:|:----:|:----:|
|73|11.4|1.1|
|80|11.4|1.1|
|50|11.4|1.1|
|87|11.4|1.05|
|73|15|1.5|
|73|19|1.95|
|73|23|4|
|73|11.4|1.1|
</center>

From this data it is apparent that changing the speed that the water is being pulled out affects the height of sand in the filter shelf, but changing the overall flow does not, which makes sense as any water not pulled from the outlet just increases the flow through the unregulated outlet. With the proper pump speeds of 73 RPM influent, and 11.4 RPM pulled out the angled outlet, the length the sand travels into the outlet, 1.1", is a small enough distance to make the actual construction feasible. The influent and effluent speeds differ due to the actual model having multiple holes to create outflow but in this one hole model, the amount that would be measured going into the other holes was just left as waste outflow rather than along with the effluent. The python code below explains the significance of these values and how they were determined.

<div class="alert alert-block alert-danger">
There is no python code below. Run-on sentences.
</div>


### Variables
- **A note on the coordinate system**: length is used to mean parallel to flow direction, so filter length is the horizontal distance the water flows within the sand section of the filter. Width the direction perpendicular to flow direction; center plates are spaced along the width of the filter. Height is the vertical direction.

##### Calculation of Backwash and Flow Area
- $V_{filter}$=***V_filter***=Velocity of filtration
- $V_{backwash}$=***V_backwash***=Velocity of water during backwash
- $Q_{plant}$=***Q_plant***=Water flow through plant
- $A_{backwash}$=***A_backwash***=Area of backwash
- $A_{flow}$=***A_flow***=Cross sectional area of sand/area of flow

##### Calculation of Filter Box Dimensions
- $\pi_{FiBw}$=***PiFiBw***=Volume increase ratio due to sand bed fluidization
- $l_{filter}$=***filter_length***=Length of filter
- $w_{filter}$=***filter_width***=Width of filter
- $h_{filter}$=***filter_height***=Height of entire filter
- $h_{box}$=***box_height***=Height of utilized box model

##### Calculation of Necessary Filter Shelf Length
- $\nu$=Kinematic viscosity
- $\rho_{sand}$=***rho_sand***=Density of particle
- $\rho_{water}$=***rho_water***=Density of water
- $\nu_{water}$=***nu_water***=kinematic viscosity of Water
- $d_{sand}$=***d_sand***=Diameter of sand particles
- $SF$=***SF***=Safety factor
- $\theta_{settling}$=***angle_settling***= Angle of filter shelves
- $V_{setting}$=***V_settling***=Velocity until the sand settles
- $V_{capture}$=***V_capture***=Safe estimate of velocity needed to capture the sand
- $V_{\alpha}$=***V_alpha***=Filter speed
- $V_{actual}$=***V_actual***=Filter speed after filter shelf
- $\alpha$=***alpha***=angle of shelves
- $l_{shelf}$=***L***=Length of filter shelf

##### Filter Shelf Dimension and Spacing Calculations
- $d_{shelf}$=***space_shelf***=Spacing between filter shelves (top to top)
- $d_{holes}$=***diam_holes***=Diameter of the holes in walls
- $N_{holes}$=***num_holes***=Number of holes on either side
- $\pi_{orifice}$=***pi_orifice***=Shrinking coefficient of water through area
- $h_{hole}$=***headloss_hole***=Headloss through the hole
- $t_{shelf}$=***thickness_shelf***=The thickness of the shelves
- $d_{sandlift}$=***space_sandlift***=Safety factor for sand to lift
- $d_{abovehole}$=***space_above_hole***=The spacing between the hole and the bottom of the Shelf
- $l_{vert}$=***L_vert***=Spacing between shelves, top to top=***space_shelf***
- $l_{shelf}$=***L***=Length of filter shelf
- $l_{notch}$=***L_notch***=Length of the notch into the filter Shelf
- $l_{horizontal}$=***L_horizontal***=Length of horizontal component of filter shelf
- $l_{insert}$=***insert_length***=Length of the filter insert to which the filter shelves are connected

<div class="alert alert-block alert-danger">
Maybe it would be best to separate out all of the python and put it in one section with these variable definitions.

Consider the usability of the current format.
</div>

Below is the equation for terminal settling velocity where d is diameter, $\nu$ is kinematic viscosity. This is used for laminar flow.

$$ Vt = \frac{d^2g}{18\nu}(\frac{\rho_{particle}-\rho_{H2O}}{\rho_{H2O}}) $$

After consultation with Professor Monroe Weber Shirk, it is necessary to also make calculations with turbulence in mind since sand settles rather quickly and experiences drag.

$$ Vt = \sqrt\frac{4g}{3Cd}\frac{\rho_{sand}-\rho_{H2O}}{\rho_{H2O}}    $$


```python
from aide_design.play import*
V_filter = 1.8*(u.mm/u.s)
V_backwash = 9*(u.mm/u.s)  #the constraining velocity
Q_plant = .37*(u.L/u.s)  #the scale we are working with for our first iteration of the filter, manipulated to achieve desired width
A_backwash = Q_plant/V_backwash #plan view area of sand (x,y axis)
A_flow = Q_plant/V_filter  #cross sectional area of sand (x,z axis)
```
From here, the team incorporated some knowledge on the depth in which water travels through a traditional AguaClara  Open Stacked Rapid Sand (OStaRS) filter. The filter backwash ratio is the ratio between settled sand height during filtration and expanded sand height during backwash. Because the filter backwash ratio is 1.3 (PiFiBw), which has been empirically determined, the team determined a settled sand height first.

<div class="alert alert-block alert-danger">
I thought you were mostly comparing it to the EStaRS figure. Why the change to OStaRS? (Also I don't think you've defined what the O in OStaRS means)
</div>

The team decided that with the scale model in mind, 3.65 inches of sand in the flow direction (filter_length) is a fair parameter to start with. With this one measurement, and the ratio between filter velocity and backwash velocity, all other parameters fall into place.

<div class="alert alert-block alert-danger">
Why is it s fair parameter to start with?
</div>

```python
PiFiBw = 1.3
filter_length = 3.65*u.inch  #manipulated to achieve desired height
filter_width = A_backwash/filter_length #the filter width is the width for BOTH areas
filter_height = A_flow/filter_width
filter_height #height of sand
box_height = filter_height*PiFiBw #the height the expanded sand bed
box_height
#the box we ordered is 18 inch by 18 inch by 24 inch with wall thickness of 0.25 inches
print(box_height.to(u.inch)) #must be 0.25 less than actual because of thickness of the box floor ordered
print(filter_width.to(u.inch)) #must be 0.25*2 less than actual because of thickness of walls on either side
print('The height of the tank should be at least',box_height.to(u.inch),'with a cross-sectional width of',filter_width.to(u.inch),'(thicknesses omitted).')
>>> height is 23.72 inches, cross sectional width of 17.46 inches
```

```python
SF =2 #safety factor suggested by AguaClara Engineer Ethan Keller

rho_sand = 1602*u.kg/u.m**3 #density of sand
rho_water = 1000*u.kg/u.m**3 #density of water at 20 C
nu_water = (pc.viscosity_kinematic(293*u.K)) #kinematic viscosity of water at 20 C
d_sand = 0.5*u.mm #diameter of sand particle
alpha = 55*u.degrees #angle of filter shelves
V_alpha=1.8*u.mm/u.second
 #filter speed!

V_actual = V_alpha/np.cos(alpha) #speed within the angled shelf
S=(1*u.inch).to(u.mm) #distance between shelves (above or below)

V_settling1=((d_sand**2)*pc.gravity/(18*nu_water))*((rho_sand-rho_water)/rho_water)
V_settling1.to(u.mm/u.s)  #settling velocity (Vt) without drag and turbulence
>>>82 mm/s
V_capture1 = V_settling1/SF #Capture velocity with safety factor incorporated
V_capture1.to(u.mm/u.s) #initial capture velocity
>>>41 mm/s

Re = (V_backwash)*(1*u.inch)/(nu_water)
Re.magnitude #Reynold's number for drag coefficient calc
Cd = 0.2 #drag coefficient corresponding with ~10^7
V_settling2 = np.sqrt(((4*pc.gravity*d_sand)/(3*Cd))*((rho_sand-rho_water)/rho_water))
V_settling2.to(u.mm/u.s)
>>> 140 mm/s #this velocity uses the drag coefficient based of the Reynolds number
V_capture2 = V_settling2/2
>>> 70 mm/s #alternative capture velocity

L1 = ((V_actual*S/V_capture1-S)/(np.cos(alpha)*np.sin(alpha)))
L2 = (S/np.cos(alpha))*((V_actual/V_capture2)-(1/np.sin(alpha)))
L1.to(u.inch)
L2.to(u.inch)
>>L1 = -1.96 inches
>>L2 = -2.05 inches
```
These lengths make the team believe that the length of the filter shelf is arbitrary due to their negative value. This seemed to correlate with the experiments as well.

<div class="alert alert-block alert-danger">
Is it physically possible to have negative values? Could there be an error here?

Please more thoroughly explain this reasoning.
</div>

From here, the team worked to calculate and parametrize the filter shelf insert. The following calculations are the steps used in calculating the filter shelf length. That is, how far into the filter they must protrude.



<div class="alert alert-block alert-danger">
explain what length of insert is

Is this length perpendicular to the wall or the length of the actually fabricated piece that is then put at an angle?
</div>

```python
#we decided that the diameter of a hole should be 0.25 inches and we worked from there.
space_shelf = 0.25*filter_length #this relationship was determined by Monroe as a reasonable measure. space_shelf is the total space between respective shelves. It is the same thing as L_vert.
>>space_shelf = .9125 inches (2.318 cm)

diam_holes = 0.25*u.inch
num_holes = filter_height.to(u.cm)/space_shelf.to(u.cm)
>>> num_holes = 20

#what is the headloss? (due to wall in middle of insert, there will be twice as many holes)
pi_orifice = 0.62
headloss_hole= pc.head_orifice(diam_holes,pi_orifice,Q_plant/(2*num_holes))
>>>headloss_hole = 1.13 cm

thickness_shelf = 0.125*u.inch #acrylic shelf
space_sandlift = 1*u.cm  #space_sandlift was a guessed value of a safety for how high the sand would climb in between adjacent plate shelves
space_above_hole = space_shelf-diam_holes-thickness_shelf/np.sin(alpha)-space_sandlift
space_above_hole.to(u.cm)
>> space_above_hole = .2952 cm #space above hole
L_vert = (diam_holes+thickness_shelf/np.sin(alpha)+space_sandlift+space_above_hole)
L_vert.to(u.cm)
>>>L_vert = 2.3177 cm
L = L_vert/(np.sin(alpha))
L.to(u.cm)
>> L = 2.82945 cm #length of filter shelf
L_notch = L/4 #for support of the material
>> L_notch = .70736 cm

L_horizontal = L*np.cos(alpha)
>> L_horizontal = 1.62291 cm

insert_length = 2*L_horizontal+filter_length
>> length_insert = 12.517 cm
```
From these calculations and the given constraints, the length of the filter shelves is 2.829 cm and the length of the insert is 12.517 cm. With these values, the overall apparatus could be fabricated in Fusion.

### Fusion360

### Stress and Displacement Analysis

In order to see how plausible this design is, a stress test was performed on the acrylic box with the expected hydrostatic forces in mind.
<center>

|![stress_test](https://github.com/AguaClara/horizontal_filtration/blob/master/images/stress.PNG?raw=true)]|
|:---:|
|Figure X: Stress calc on box|
</center>

This stress analysis could then be translated into an approximate displacement of the box itself.

<center>

|![displacement](https://github.com/AguaClara/horizontal_filtration/blob/master/images/displacement.PNG?raw=true)|
|:---:|
|Figure X: displacement|
</center>

Since the walls would only flex a max of 2.88 mm, the design is structurally sound.

<div class="alert alert-block alert-danger">
How did you do this?

Is this another appendix? Appendices should be referred to in the body of the text, not introduce new ideas.

If you have different topics in an appendix, you should label each separate section with "Appendix A: Stress and Displacement Analysis of the Filter Box"
</div>



# To convert the document from markdown to pdf
pandoc Name_of_this_file.md -o TeamName_Research_Report.pdf
```
