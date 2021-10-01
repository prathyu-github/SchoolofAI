![Image-LR-0.1](https://github.com/prathyu-github/SchoolofAI---Assignments/blob/main/session_2/A2-LR-0.1.JPG)
![Image-LR-0.2](https://github.com/prathyu-github/SchoolofAI---Assignments/blob/main/session_2/A2-LR-0.2.JPG)
![Image-LR-0.5](https://github.com/prathyu-github/SchoolofAI---Assignments/blob/main/session_2/A2-LR-0.5.JPG)
![Image-LR-0.8](https://github.com/prathyu-github/SchoolofAI---Assignments/blob/main/session_2/A2-LR-0.8.JPG)
![Image-LR-1](https://github.com/prathyu-github/SchoolofAI---Assignments/blob/main/session_2/A2-LR-1.0.JPG)
![Image-LR-2](https://github.com/prathyu-github/SchoolofAI---Assignments/blob/main/session_2/A2-LR-2.0.JPG)

#Feed forward 
	h1=i1*w1+i2*w2
	h2=i1*w3+i2*w4
	a_h1=σ(h1) = 1/1+e-h1
	a_h2=σ(h2) = 1/1+e-h2
	o1=w5*a_h1+w6*a_h2
	o2=w7*a_h1+w8*a_h2
	a_o1=σ(o1) = 1/1+e-o1
	a_o2=σ(o2) = 1/1+e-o2
	error E1= ½*(t1-a_o1)2 where t1, t2 are target values (expected outcomes)
	error E2= ½*(t2-a_o2)2
	E_tot=E1+E2
Back propagation starts here 
(∂E_t)/∂w5=(∂(E1+E2))/∂w5=∂E1/(∂a_o1)×(∂a_o1)/∂o1×∂o1/∂w5
∂E1/(∂a_o1)=()〖∂(½*(t1-a_o1)〗^2)/(∂a_o1)=(t1-a_o1)*(-1)=a_o1-t1
 (∂a_o1)/∂o1=(∂(σ(o1)))/∂o1=σ(o1)×(1-σ(o1))=a_o1×(1-a_o1)
∂o1/∂w5=a_h1
(∂E_t)/∂w5=(a_o1-t1)×a_o1×(1-a_o1)× a_h1
(∂E_t)/∂w6=(a_o1-t1)×a_o1×(1-a_o1)× a_h2
(∂E_t)/∂w7=(a_o2-t2)×a_o2×(1-a_o2)× a_h1
(∂E_t)/∂w8=(a_o2-t2)×a_o2×(1-a_o2)× a_h2

(∂E_t)/(∂a_h1)=(∂(E1+E2))/(∂a_h1)=∂E1/(∂a_o1)×(∂a_o1)/∂o1×∂o1/(∂a_h1)
∂E1/(∂a_h1)=(a_o1-t1)×a_o1×(1-a_o1)× w5
∂E1/(∂a_h2)=(a_o1-t1)×a_o1×(1-a_o1)× w6
∂E2/(∂a_h1)=(a_o2-t2)×a_o2×(1-a_o2)× w7
∂E2/(∂a_h2)=(a_o2-t2)×a_o2×(1-a_o2)× w8
∂(E1+E2)/(∂a_h1 )=((a_o1-t1)×a_o1×(1-a_o1 )× w5)+((a_o2-t2)×a_o2×(1-a_o2 )× w7)
∂(E1+E2)/(∂a_h2 )=((a_o1-t1)×a_o1×(1-a_o1 )× w6)+((a_o2-t2)×a_o2×(1-a_o2 )× w8)
Now one more layer backward
(∂E_t)/∂w1=(∂E_t)/(∂a_h1)×(∂a_h1)/∂h1×∂h1/∂w1
(∂E_t)/∂w1=(∂E_t)/(∂a_h1)×a_h1*(1-a_h1 )*∂h1/∂w1=(∂E_t)/(∂a_h1 )×a_h1*(1-a_h1 )*i1
(∂E_t)/∂w2=(∂E_t)/(∂a_h1 )×a_h1*(1-a_h1 )*i2
(∂E_t)/∂w3=(∂E_t)/(∂a_h2 )×a_h2*(1-a_h2 )*i1
(∂E_t)/∂w4=(∂E_t)/(∂a_h2 )×a_h2*(1-a_h2 )*i2




