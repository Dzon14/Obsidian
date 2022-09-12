# Power density spectrum of periodic signals
### Continous-time
- The average power of a peridoic signal is $$P_{x}=\frac{1}{T_{p}}\int_{T_p}^{} \lvert x(t) \rvert ^{2} \ dt$$
Which leads to (using [[Fourierserie|fourier series]]) $$P_{x}= \sum_{k = - \infty}^{\infty}\lvert c_{k} \rvert ^{2}$$
where $\lvert c_{k} \rvert ^{2}$ is the average power of the kth term in the series. located at frequency $kF_{0}$ 
![[Pasted image 20220912140135.png|400]]
### Discrete-time
- The average power $$P_{x}= \frac{1}{N}\sum_{n=0}^{N-1}\lvert x(n) \rvert ^{2}$$
which leads to $$P_{x}= \sum_{k=0}^{N-1}\lvert c_k \rvert ^{2}$$
	where the coefficient is the avg power of the kth therm in the series, located at frequency $kf_{0}$. 
![[Pasted image 20220912140206.png|400]]

#el 