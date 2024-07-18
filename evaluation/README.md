# Additional Details of Evaluation

<div align=center>
    <img src=".\epoch.png" height=500 />
</div>
<div align=center style="color:orange; 
    color: #999;
    padding: 2px;">
    <div class="formula">
    Fig. 1. Ablation on sampling number $C_n$ for multi-noise aware training.
    </div>
</div>


**Multi-scale noise-aware training perception scales.**

During each epoch of the model training process, we randomly sample $C_n$ noise vectors to composite a noise subset $\mathcal{S}_{sub} = \{N_1, N_2, ..., N_{C_n}\}$ to integrate one training iteration. 
To explore the effect of \methodthree on noise-resilient ability, we train 4 models with sampling number $C_n \in$ \{1,3,5,10\}. Figure 1 displays the model accuracy over training iterations with ``Read and Gate'' noise, the model with $C_n=1$ converges quickly, but it has an obvious performance bottleneck and fluctuating performance test on various noises. 
The model with $C_n=10$ performs better accuracy and stability, and there is about a 5\% performance improvement compared with $C_n=1$, but the training convergence time is about 3.3x that of $C_n=1$. With comprehensive consideration,  setting $C_n=3$ or $C_n=5$ is cost-effective, which training time is 1x and 1.2x, the accuracy improvement is 3\%\deleted{x} and 5\% of $C_n=1$.
As the number of samples increases, the noise space perceived by the model is more generalizable and robust, in this paper we adopt $C_n=3$.