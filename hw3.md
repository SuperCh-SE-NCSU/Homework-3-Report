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
 
