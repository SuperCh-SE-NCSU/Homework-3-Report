# Homework-3-Report
Zhewwei Hu, Liang Dong, Shupeng Niu<br/>
Apr. 2, 2015

## Theory1: COCOMO
#### List1: Scale factors

- Prec: Precedentness. 
> Precedentness indicates whether current work is highly based on previous work or not. If so, there will be less effort, because people will tend to be familiar with previous work. Otherwise more effort will be needed.

- Flex: Development flexibility.
> Development flexibility indicates whether one team can accept the changes of development requirements well or not. If the flexibility of one team is high, when requirements change, there will be less effort for them to adapt to new requirements.

- Resl: Rish resolution.
> Resl indicates whether one team has carried out enough risk analysis or not. If so, that team will understand their project's risk more precisely, and will take less effort.

- Team: Team cohension.
> Team indicates whether one team has high team cohension or not. If so, conflicts between team members will be less. Hence, the effort will also be reduced.

- Pmat: Process maturity.
> Pmat indicates whether one team is familiar with the development process or not. If so, they will have less errors occured, and take less effort to finish the project.

#### List2: Upside effort multipliers -- the things that, if increased, add to the development effort
- rely: Required software reliability
> If one team want to have high "rely", they have to do many more work, such as writing and passing different kinds of tests, considering security issues, and so on. These things will require more effort.

- data: Database size.
> If one team need bigger DB size, they have to ensure the relationship between different tables is OK. Also they should optimize the processing time of DB. These things will absoluately require more effort.

- cplx: Program complexity.
> The more complex a program is, the more effort one team will have.

- ruse: Software Reusability.
> If one team want to increase the software reusability, they may take more effort to make the code drier and write some interfaces or APIs.

- docu: Documentation requirements.
> If one team need more document during development,  they have to take more effort to design and write documentations.

- time: Execution time constraint.
> If one team want to decrease the response time from "ms" level to "ns" level, they have to optimize the code, database structure, deploy more efficient algorithm, and so on. So, these optimization need more effort.

- stor: Main storage constraint.
> If there are more strict storage constraint, the team may do extra work to redesign the data structure in order to take less storage and include more information, which need more effort.

- pvol: platform volatility
> If one project should be deployed on different platforms or it should use several platforms to development, the team member should be familiar with these platforms. Training time and compatibility problem may add effort.
 
#### List3: Downside effort multipliers -- the things that, if increased, reduce the development effort

- acap: Analyst capability.
> Highe ability of analysts in one team will decrease the effort linearly. Because they can analyse the requirements of project and make predetermination more precisely.

- pcap: Programmer capability.
> Highe ability of programmers in one team will decrease the effort linearly. Because they will write in "good" smell and leave less bugs, which can make less effort time to refactor methods.

- pcon: Programmer continuity.
> High continuity of programmers in one team will decrease the effort linearly. Because they will be more familiar with the project and need less time to train. Therefore, high "pcon" can decrease the effort.

- aexp: Analyst experience.
> Sufficient experience of analysts in one team will decrease the effort linearly. Because experienced analysts can help the whole team to make less errors, which may occur before.

- pexp: Programmer experience.
> Sufficient experience of programmers in one team will decrease the effort linearly. Because experienced programmers can write code with higher maintainability and extendability.

- ltex: Language and tool experience.
> High experience of programm languages and tools will decresde the effort linearly. Because team members will take less time to write code and debug under this situation.

- tool: Use of software tools
> Having excellent development tools during development is quite crucial and decrease the effort linearly. For instance, some IDE tools can make coding and debugging more efficient.

- site: Multisite development.
> If a project can be developed in multisite simultaneously and make few conflicts, effort will decrease linearly. And we can use version control tools, such as Git.

- sced: length of schedule
> If a project has sufficient time to develop, effort will decrease linearly. Because team members can do less work in unit time.

## Theory2: Treatments (management actions)
```
 @rx
 def improvePersonnel(): return dict(
   acap=[5],pcap=[5],pcon=[5], aexp=[5], pexp=[5], ltex=[5])
```
- Acap (analyst capability) -> very high<br/>
 Pcap (programmer capability) -> very high<br/>
 Pcon (programmer continuality) -> very high<br/>
 Aexp (analyst experience) -> very high<br/>
 Pexp (programmer experience) -> very high<br/>
 Ltex (language and tool experience) -> very high<br/>
- There factors are all personnel related. So these factors are all set to very high. And the personnel will be improved, the effort will be reduced.

```
@rx
def improveToolsTechniquesPlatform(): return dict(
   time=[3],stor=[3],pvol=[2],tool=[5], site=[6])
```
- Time (runtime pressure) -> nominal<br/>
Stor (main storage constraint) -> nominal<br/>
Pvol (platform volatility) -> low<br/>
Tool (use of software tools) -> very high<br/>
Site (multisite development) -> extra high<br/>
- Then the tool usage will be improved, and platform volatility will be more stable.

```
@rx
def reduceQuality():  return dict(
   rely = [1], docu=[1], time = [3], cplx = [1])
```
- Rely (required software reliability) -> very low<br/>
Docu (document required) -> very low<br/>
Time (runtime pressure) -> nominal<br/>
Cplx (program complexity) -> very low<br/>
- The reliability is very low, few documents and low complexity will reduce the quality of software.

## Theory3: Projects
#### Comparison1: Three key differences between flight and ground
- Flight:
```
kloc= xrange(7,418), cplx = [3,4,5,6], rely = [3,4,5]
```
  -	kloc (thousand line of code) range is less than 10,000<br/>
		cplx (program complexity) can be from nominal to extra high;
		rely (required software reliability) can be from nominal to very high.

-	Ground:
```
kloc=xrange(11,392), cplx = [1,2,3,4], rely = [1,2,3,4]
```
  -	kloc (thousand line of code) range is more than 10,000<br/>
		cplx (program complexity) can be from very low to high<br/>
		rely (required software reliability) can be from very low to high.

- Conclusion:
  - "Flight" has less code range
  - "Flight" has higher program complexity
  - "Flight" has higher required software reliability

#### Comparison2: Three key differences between osp and osp2
OSP:
```
Prec = [1,2], site = [3], tool = [2,3]
```
  -	Prec (Precedentedness) can be from very low to low<br/>
		Site (multisite development) can be nominal<br/>
		Tool (use of software tools) can be from low to nominal<br/>
OSP2:
```
Prec = [3,4,5], site = [6], tool = [5]
```
  -	Prec (Precedentedness) can be from nominal to very high<br/>
		Site (multisite development) can be extra high<br/>
		Tool (use of software tools) can be very high<br/>

- Conclusion:
  - "osp2" has higher precedentedness
  - "osp2" uses more multisite development
  - "osp2" uses more software tools
