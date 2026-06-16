#review
Given,

$$  
c_1v_1 + c_2v_2 + \cdots + c_nv_n = 0  
$$

Ask one question:

_**"Do you have at least one coefficient $(c_i)$ such that $(c_i \neq 0)$?"**_

| Scenario 1                                                                                                                     | Scenario 2                                                      |
| ------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------- |
| **Yes, there exists a coefficient (c_k \neq 0)**                                                                               | **No, all coefficients are zero**                               |
| Solve for (v_k):                                                                                                               | The only solution is:                                           |
| $$v_k = -\frac{c_1}{c_k}v_1 - \cdots - \frac{c_{k-1}}{c_k}v_{k-1} - \frac{c_{k+1}}{c_k}v_{k+1} - \cdots - \frac{c_n}{c_k}v_n$$ | $$c_1=c_2=\cdots=c_n=0$$                                        |
| (v_k) is a linear combination of the remaining vectors.                                                                        | No vector can be written as a linear combination of the others. |
| A vector is redundant.                                                                                                         | No vector is redundant.                                         |
| **Linearly Dependent**                                                                                                         | **Linearly Independent**                                        |

## Memory Trick

| Question                                   | Answer          |
| ------------------------------------------ | --------------- |
| At least one $(c_i \neq 0)$?               | **Dependent**   |
| Only solution is $(c_1=c_2=\cdots=c_n=0)$? | **Independent** |
