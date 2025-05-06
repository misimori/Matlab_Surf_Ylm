# 
## Computing a general surface coordnates by spherical harmonic expansion

 We know that any surface is characterized by two parameters, ex. $\mathrm{u}$ and $\mathrm{v}$. So, if the surface is continuous we can represent $x,y,z$ coordinates of that surface by: $x=x(\mathrm{u},\mathrm{v}), y=y(\mathrm{u},\mathrm{v})$ , and $z=z(\mathrm{u},\mathrm{v})$. We take the parameters to be zenith and azimuthal angels in spherical coordinate system $( \mathrm{u} = \theta, \mathrm{v}= \varphi )$ to describe a general surface. Therefore, in Cartesian coordinates the surface is described as $x=x(\theta ,\varphi )$, $y=y(\theta ,\varphi )$, and $z=z(\theta ,\varphi )$. Also, the surface in spherical coordinate  would be $\theta =\theta , \varphi =\varphi , r=r(\theta ,\varphi )$. For example, the equation of a sphere with radius $R$ will be $\theta =\theta, \varphi =\varphi, r=R$.

<img src="https://github.com/misimori/Matlab_Surf_Ylm/blob/13c5d93fdb6923e8117685ad3549c60db4389904/fig1.png" width=70% height=70%>


The spherical harmonics are defined as $Y_{\ell }^m (\theta ,\varphi )=N_{\ell ,m} \,P_{\ell }^{|m|} (\cos \theta )\,{e}^{im\varphi }$.

 $N_{\ell ,m}$ is normalization prefactor, which is equal to $N_{\ell ,m} =\sqrt{\frac{2\ell +1}{4\pi }\frac{(\ell -m)!}{(\ell +m)!}}$,  and 
$N_{\ell ,-m} ={(-1)}^m \sqrt{\frac{2\ell +1}{4\pi }\frac{(\ell -m)!}{(\ell +m)!}}$ , ($m>0$).


   $P_{\ell }^m (\cos \theta )$ is associate Legendre function. We have ($m>0$): $P_{\ell }^{-m} (\cos \theta )={(-1)}^m \frac{(\ell -m)!}{(\ell +m)!}P_{\ell }^m (\cos \theta )$. So:

$$Y_{\ell }^{-m} (\theta ,\varphi )=\sqrt{\frac{2\ell +1}{4\pi }\frac{(\ell +m)!}{(\ell -m)!}}{(-1)}^m \frac{(\ell -m)!}{(\ell +m)!}P_{\ell }^m (\cos \theta )\,{e}^{-im\varphi } =N_{\ell ,-m} P_{\ell }^m (\cos \theta )\,{e}^{-im\varphi }$$

 The spherical harmonics form a complete basis set in Hilbert space of square integrable functions, and are normalized and orthogonal: $\int_0^{2\pi } \int_0^{\pi } Y_{\ell_1 ,m_1 } (\theta ,\varphi )Y_{\ell_2 ,m_2 }^* (\theta ,\varphi )\sin \theta \,\,{d}\theta \,\,{d}\varphi =\delta_{\ell_1 ,\ell_2 } \delta_{m_1 ,m_2 }$, where $\delta_{a,b}$ is Kronecker delta function, and $Y_{\ell ,m}^*$ is the complex conjugate of $Y_{\ell ,m}$. Any function can be expressed as a linear combination of spherical harmonics:

$$x(\theta ,\varphi )=\sum_{\ell =0}^{\infty } \sum_{m=-\ell }^{\ell } a_{\ell ,m}^x Y_{\ell }^m (\theta ,\varphi ) \Longrightarrow a_{\ell ,m}^x =\int_0^{2\pi } \int_0^{\pi } x(\theta ,\varphi )Y_{\ell ,m}^* (\theta ,\varphi )\,\,\sin \theta \,{d}\theta \,{d}\varphi $$


$$y(\theta ,\varphi )=\sum_{\ell =0}^{\infty } \sum_{m=-\ell }^{\ell } a_{\ell ,m}^y Y_{\ell }^m (\theta ,\varphi ) \Longrightarrow a_{\ell ,m}^y =\int_0^{2\pi } \int_0^{\pi } y(\theta ,\varphi )Y_{\ell ,m}^* (\theta ,\varphi )\,\,\sin \theta \,{d}\theta \,{d}\varphi $$

$$z(\theta ,\varphi )=\sum_{\ell =0}^{\infty } \sum_{m=-\ell }^{\ell } a_{\ell ,m}^z Y_{\ell }^m (\theta ,\varphi ) \Longrightarrow a_{\ell ,m}^z =\int_0^{2\pi } \int_0^{\pi } z(\theta ,\varphi )Y_{\ell ,m}^* (\theta ,\varphi )\,\,\sin \theta \,{d}\theta \,{d}\varphi $$

$a_{\ell ,m}^x$, $a_{\ell ,m}^y$, and $a_{\ell ,m}^z$ are the expansion coefficients which we are going to calculate for a given surface.







