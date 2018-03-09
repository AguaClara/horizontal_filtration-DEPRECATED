# Horizontal Filtration, Spring 2018
#### Clare O'Connor, Corson Chao, and Christopher Galantino
#### 3/1/2018

## Abstract
Briefly summarize your previous work, goals and objectives, what you have accomplished, and future work. (100 words max)

Horizontal filtration is a completely new innovation for the AguaClara team, arising from a desire to make the 1 L/s plants easier to make and ship by eliminating the Enclosed Stacked Rapid Sand Filter. To create a horizontal filter, aspects of the sedimentation tanks and current filter design will be used, such as the relationship between backwash and operational speed, as well as the design of the plate settlers. Initial experimentation with the settling of sand during upflow is promising for when construction of the filter prototype begins.

## Introduction

The plantita (1 L/s plant) is a difficult apparatus to construct and implement. Finding a way to make fabrication, assembly, and installation simpler, as well as downsize components, will greatly decrease the cost and make the technology more accessible for global communities.

The concept of an easy to implement, versatile water treatment plant correlates nicely with the [OrigamiWaterLab](https://github.com/OrigamiWaterLab) proposed by AguaClara engineer [Ethan Keller](https://github.com/ethan92429). Essentially, ingenious engineering is found in simplicity and resiliency. Fabricating a plant that transitions from flat into 3D is a innovative area of study that may become more possible with increased exploration.

With this idea in mind, one of the most difficult features to construct in an efficient, mass-producible way is the filter. Currently, the plantita’s filter is characterized by a vertical, enclosed stacked rapid sand filter (EStaRS) which is tall and unfriendly to ship in addition to its complicated geometry of 4 inlet manifolds and 3 outlet manifolds.

To combat these difficulties, a horizontal filter design has been proposed. This filter will not be stacked. Instead, it will use horizontal flow for filtration and vertical flow for backwash. The ratio of the horizontal flow area to the vertical flow area will be designed so that the bed will fluidize during backwash. The inlet and outlets will be designed so that sand/water separation doesn’t require slots. Water will exit through a geometry that has a plate settler style design to ensure that sand settles out and isn’t carried into the effluent. Both current filtration techniques and technologies from the plate settle design in the sedimentation tanks are used in the design of the horizontal filter. This technology might then also  be adapted to replace the slotted pipes in the current Stacked Rapid Sand Filters in the full-sized plants.

The goal is that these design innovations will simplify the current design and facilitate scaleup and mass production of AguaClara technologies.

## Methods


As the team is still waiting for materials, as of the first report, much of our work has been calculation, learning Fusion360, and some minor experiments when calculations didn't yield conclusive answers. These experiments focused on determining the length of the filter shelves (the adapted plate settles) which would allow sand to settle before climbing into the outlet and flowing out of the filter. To do this two tests were run.

Two similar apparatuses were constructed to determine the length of the fitler shelves based on how sand settled in angled tubes of different diameters. The first setup included a 1" diameter pipe as the filter body and 1/8" tube as an angled outlet(Figure 1) Forty-five degrees was chosen as the angle to allow the most sand to fall while not changing the flow too much. Sand, then water were poured in to see if sand would travel into the outlet during startup conditions. It did. From there the pumps were turned on to mimic water flow during filtration and backwash. The speed in the filter body was set to be the speed required for backwash, 9mm/s, and the speed in the angled outlet was set to the speed during operation 1.8mm/s as that is the maximum water velocity that should be experienced within the filter shelves. Upon completion of this test, a new apparatus was constructed.

| ![apparatus for testing length of filter shelves](images/small_diameter_outler.jpg) |
|:--:|
| *Figure 1. First experimental apparatus with 1" diameter filter and 1/8" outlet tube. Influent water comes in through the bottom and out through the angled outlet and the top.* |

The original idea for the new apparatus was to have a 1" angled tube stemming from the 1" filter. This proved nearly impossible to fabricate, so as in Figure 2, a 3/4" angled outlet pipe was used instead. In this test, the same steps were taken, dry sand was poured to determine how sand would travel. Then water was added, which caused sand to move several inches up into the outlet tube. However, the level of sand retreated once the pumps were turned on and operating at backwash and operational speeds.

| ![apparatus for testing length of filter shelves](images/one_inch_outlet.jpg) |
|:--:|
| *Figure 2. Second experimental apparatus with 1" diameter filter and 3/4" outlet tube. Influent water comes in through the bottom and out through the angled outlet and the top.* |

Explain the techniques you have used to acquire additional data and insights. Reserve fine detail for the Manual at the end of the report, but use this section to give an overview with enough detail for the reader to understand your Results and Analysis. Describe your apparatus, and have a justification for every decision you made and every parameter you chose in the design of the apparatus. Be especially careful to detail the conditions your experiments were conducted under, as this information is especially important for interpreting your results

Below, some example sections are given. Sectioning the report is meant to keep similar information together.  Continue making sections as necessary, or delete sections if you do not need them. Feel free to add subsubsections to further delineate the information. For example, under the Experimental Apparatus section below, the EStaRS team might consider having sections such as "Filter Design" and "Filter Fabrication".

### Experimental Apparatus
Explain your apparatus setup using enough detail such that future teams can recreate your apparatus. Make sure to explain why you built it this way.
* Design (calculations, constraints)

  $\frac{-b\pm\sqrt{b^2-4ac}}{2a}$
* Schematic (label parts)

  <img src="https://github.com/jillianwhiting/Jillian-Whiting/blob/master/Images/IMG_0009.jpg?raw=true" height=250 width=200>

* Image (from lab; label parts)
* Materials (dimensions, materials)
* Complications in construction
* If already constructed: write a brief summary of important constraints, include any revisions to apparatus, also reference the prior report where construction is described

### Procedure
Discuss your experimental procedure. How did you run your experiment? What were you testing? What were the values of relevant parameters?

## Results and Analysis
Present an observation (results), then explain what happened (analysis).  Each paragraph should focus on one aspect of your results. In that same paragraph, you should interpret that result.
In other words, there should not be two distinct paragraphs, but instead one paragraph containing one result and the interpretation and analysis of this result. Here are some guiding questions for results and analysis:

When describing your results, present your data, using the guidelines below:
* What happened? What did you find?
* Show your experimental data in a professional way.
```python
from aide_design.play import*
x = np.array([1,2,3,4,5])
y = np.array([1,2,3,4,5])
plt.figure('ax',(10,8))
plt.plot(x,y,'*')
plt.savefig('/Users/jillianwhiting/github/Jillian-Whiting/Images/linear')
plt.show()
```
![linear](https://github.com/jillianwhiting/Jillian-Whiting/blob/master/Images/linear.png?raw=true)
Figure 1: Captions are very important for figures. Captions go below figures.

After describing a particular result, within a paragraph, go on to connect your work to fundamental physics/chemistry/statics/fluid mechanics, or whatever field is appropriate. Analyze your results and compare with theoretical expectations; or, if you have not yet done the experiments, describe your expectations based on established knowledge. Include implications of your results. How will your results influence the design of AguaClara plants? If possible provide clear recommendations for design changes that should be adopted. Show your experimental data in a professional way using the following guidelines:
* Why did you get those results/data?
* Did these results line up with expectations?
* What went wrong?
* If the data do not support your hypothesis, is there another hypothesis that describes your new data?

## Conclusions
Explain what you have learned and how that influences your next steps. Why does what you discovered matter to AguaClara?

Make sure that you defend your conclusions with facts and results.

## Future Work
Describe your plan of action for the next several weeks of research. Detail the next steps for this team. How can AguaClara use what you discovered for future projects? Your suggestions for challenges for future teams are most welcome. Should research in this area continue?

Once the acrylic box for the team comes in, construction of the full filter will begin. This will include construction the filter shelves, sloped bottom, EPDM sealed doors, and the siphon to start backwash.

# Manual
The goal of this section is to provide all of the guidance that would be necessary for a future team to pick up your work where you left off. Please try to be thorough and put yourselves in the shoes of a newcomer to the project. Below are some recommended sections, but the manual will likely take a slightly different form for each team.

## Fabrication Details
Include any information related to the fabrication of equipment, experimental apparatuses, or technologies. Include the purpose of each step and the fabrication methods used. Reference appropriate safety precautions.

-for experiment  with sand settling: welded tubes at angles by cutting angled hole

## Special Components
If your subteam uses a particular part that is unique and you could foresee a future subteam needing to order it or learn more about it, please include basic information like the vendor where it was purchased, catalog/item number, and a link to any documentation.

-tank
-EPDM
-leather punch?
-EPDM adhesive

## Experimental Methods

### Filter Shelf Length Tests

|Table of  pump speed and sand length in outlet tube|||
|:----:|:---:|:---:|
|body speeds (rpm)|outlet speed (rpm)|sand length in tube(in)|
|:---:|:----:|:----:|
|73|11.4|1.1|
|80|11.4|1.1|
|50|11.4|1.1|
|87|11.4|1.05|
|73|15|1.5|
|73|19|1.95|
|73|23|4|
|73|11.4|1.1|


#### Experiment: 1" and 1/8"
1. First a mock filter was constructed using a 1" clear PVC pipe; in this pipe an angle hole was drilled at 45 degrees from the vertical around 5 inches from the top of the pipe. Into this hole, a small length of 1/8" tubing cut on one end to an angle of 45 degrees was inserted and glued. See Figure 1 above for an image of the apparatus.
2. Dry sand was poured from the top into the apparatus to if dry sand would move up the outlet tube when the sand level was two inches above the angled outlet. It did not.
3. An additional 500g of sand were poured in increments of 100g, this corresponded with an additional height of about 1.5ft in the 1" pipe. At no point did dry sand enter into the outlet tube.
4. Water was then slowly added into original amount of sand, during this process water carried sand into the first inch of the outlet tube.
5. Pumps were checked for proper flow rate to get proper water velocity in the outlet tube as corresponding to the outlet diameter and speed required for backwash and operation speed. The body of the filter was moving at a speed required for backwash and the outlet pull was at the speed required during operation as that should be the maximum velocity experienced in the filter shelves.
6. water pumped through the now, very wet sand. Sand was moved 3 inches up the length of the outlet tube. Preferential flow paths were observed as the apparatus was tilted.


#### Experiment: 1" and 3/4"

Clare! Finish this once you've eaten breakfast and probably before you go to work since you have to go to class kind of soon.
1. Originally, the plan had been to use 1" and 1" but fabrication of the experimental apparatus was extraordinarily challenging, so the outlet tube dimension was changed to reflect what was possible to construct.
    b. welded a .75" inched clear PVC tube to a new 1" diameter tube. ...
    c. add dry sand.
    d. fill with water.
    e. pump water though outlet at new relevant speed


### Sand Movement in Flat Filter shelves

This is an upcoming event, which has been included to assist in developing the organization structure of this section.
#### Set-up
#### Experiment

## Experimental Checklist
Another potential section could include a list of things that you need to check before running an experiment.

## Python Code

### Variables

Corson! You can bring the variables from the dimensional analysis code to here and then copy the code in a way that makes sense to you!

$g$: gravity
$\sigma$: dispersion
$a$: amplitude
$h$: water depth
$H$: distance from wave crest to trough (2$a$)
$T$: wave period
$\lambda$: wavelength
$k$: wavenumber
$c_p$: celerity (wave phase speed)
$P$: pressure
$F$: force
$u$, $w$: x-velocity, z-velocity components

```python
# Comment
```

## Fusion Drawings

The purpose of this filter assembly is for simplicity and easy fabrication. The filter exists within an acrylic box with an inflow and an outflow. The sand column itself exists in the middle with a filter shelf insert that can be added or removed.

The team must first calculate the dimensions of the sand filter space which will make up a section of the overall apparatus. To do this, HorFi takes into account the velocity at which water moves through a sand filter and the desired flow rate of the system. Since creating a 1 L/s apparatus would take all semester, the team begins with a scale model at 0.1 L/s.

Since the backwash velocity (V_backwash) is greater than the filter velocity (V_filter), it is the design constraint. With some math, the area of backwash (A_backwash) and area of flow (A_flow) may be calculated.


```python
V_filter = 1.8*(u.mm/u.s)
V_backwash = 9*(u.mm/u.s)  #the constraining velocity
Q_plant = .37*(u.L/u.s)  #the scale we are working with for our first iteration of the filter, manipulated to achieve desired width
A_backwash = Q_plant/V_backwash #plan view area of sand (x,y axis)
A_flow = Q_plant/V_filter  #cross sectional area of sand (x,z axis)
```
From here, the team must incorporate some knowledge on the depth in which water travels through a traditional AguaClara OStaRS filter. The filter backwash ratio is the ratio between settled sand height during filtration and expanded sand height during backwash. Because the filter backwash ratio is 1.3 (PiFiBw), which has been empirically determined, the team must determine a settled sand height first.

The team decides that with the scale model in mind, 4 cm of sand in the flow direction (filter_length) is a fair parameter to start with. With this one measurement, and the ratio between filter velocity and backwash velocity, all other parameters fall into place.

```python
PiFiBw = 1.3
filter_length = 3.65*u.inch  #manipulated to achieve desired height
filter_width = A_backwash/filter_length #the filter width is the width for BOTH areas
filter_height = A_flow/filter_width #height of sand
box_height = filter_height*PiFiBw #the height the expanded sand bed
#the box we ordered is 18 inch by 18 inch by 24 inch with wall thickness of 0.25 inches
print(box_height.to(u.inch)) #must be 0.25 less than actual because of thickness of the box floor ordered
print(filter_width.to(u.inch)) #must be 0.25*2 less than actual because of thickness of walls on either side
print('The height of the tank should be at least',box_height.to(u.inch),'with a cross-sectional width of',filter_width.to(u.inch),'(thicknesses omitted).')
>>> height is 23.72 inches, cross sectional width of 17.46 inches
```

With these dimensions calculated, the filter box can then be rendered as seen below in Figure X. (don't have figure numbers figured out yet)

![filter_box](https://raw.githubusercontent.com/AguaClara/horizontal_filtration/master/images/filter_box.JPG)

Notice the blue line on the filter box floor. Depending on the sand filter length determined and length needed for the filter shelves, this will be the location for the entrance and exit plates with the filter shelf insert the appropriate width to ensure a snug fit.

![filter_box](https://raw.githubusercontent.com/AguaClara/horizontal_filtration/master/images/filter_box_plates.JPG)

**Note:** We still need to determine the hole diameter for the entrance and exit plates so for now the Fusion rendition has a solid plate.

Between these plates will be the filter shelf insert, a series of angled shelves that serve to both shelter the holes during routine filtration and also return sand during backwash. Below is a filter shelf unit. T

```python

# To convert the document from markdown to pdf
pandoc Name_of_this_file.md -o TeamName_Research_Report.pdf
```
