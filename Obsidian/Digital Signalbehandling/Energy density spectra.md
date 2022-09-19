## Energy density spectra
- Very important in applications like wireless communications.
**Magnitude relation:**
$$\lvert Y(\omega) \rvert = \lvert H(\omega) \rvert \lvert X(\omega) \rvert$$By squaring this it tells us that the energy density spectra of the input and output signals $$\begin{align} S_{xx}(\omega) = \lvert X(\omega) \rvert^{2} \\ S_{yy}= \lvert Y(\omega) \rvert^{2} \\ \\ \text{Are related as} \\ \\ S_{yy}(\omega)= \lvert H(\omega) \rvert^{2}S_{xx}(\omega) \end{align}$$
![[Pasted image 20220919140126.png|500]]
Integration of $S_{yy}(\omega)$ tells us the energy of the output signal. 
$$E_{y}= \frac{1}{2\pi} \int_{-\pi}^{\pi} \lvert H(\omega) \rvert^{2}S_{xx}(\omega) \ d \omega$$

#el 