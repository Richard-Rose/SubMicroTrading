My name is Richard Rose and I am the author of the SubMicroTrading framework.

The source is released under a the Apache 2.0 license. You can opt for a support subscription please see www.SubMicroTrading.com or contact Low Latency Trading support@submicrotrading.com for more details.

SubMicroTrading is a highly concurrent component based algo trading framework almost 5 years in the making. Includes components for various market data and trading sessions including ETI, UTP, Millenium, Fix, FastFix, CME MDP.

It was developed to see if java could be made as fast as C++ for a real trading application, achieving single digit microsecond latency as required for a number of strats running in colocation.

4 micros average tick to trade, wire to wire at 800,000 ticks/second
(2 micros java process internal time)

This project is not maintained, my advice to anyone reading this is look at Peter Lawrey's Chronicle Products. Its possible my FIX engine and persistence are faster, but I have never benchmarked so thats just conjecture at this point. Whats for sure is he has built out his product and still maintains it and has split into sub projects so you can use just the bits you want.

Sample benchmark, replaying CME fast fix using tcpreplay at max replay, measured in an independent lab using TipOff.

I would also say that Java has improved alot in last 10 years and Java 9 using byte instead of char is a big win, if you can live with a little bit of jitter at the P99 end from G1 garbage collection then forget pooling and keep it simple ... pooling patterns just take us back to C and early C++ days of mem leaks ... even if you are careful, the next person to touch the code can/WILL break it. I would also suggest looking at the Azul pause less GC (I last benchmarked it in 2010!).

Please dont contact me directly about this product, I have had many emails and as I work full time I cannot help.

Good luck

Richard
