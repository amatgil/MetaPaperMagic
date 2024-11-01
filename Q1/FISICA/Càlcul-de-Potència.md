# Formules de càlcul de potència

- $$P_{dinàmica} = \alpha\cdot{}c\cdot{}V^2\cdot{}f_{clk}$$
  - $\alpha$: factor d'activitat (quants transistors estan encesos)
  - $c$: capacitància, una constant
  - $V$: voltatge
  - $f$: freqüencia del rellotge
- $$P_{estàtica} = I_{leak}\cdot{}V$$
- $$P_{total} = P_{dinàmica} + P_{estàtica}$$

- $$CPI = \frac{n_{cicles}}{n_{ins}}$$ (cicles per instrucció, promig de tota l'execució)

# Llei d'Amdhal
"El màxim speed-up aconseguible minimitzant el retard d'una part està limitat per la fracció que ocupa". És a dir, si millores una part, el total no pot millorar més que si la part és un no-res del total.

L'speed-up $S_t$ al millorar una part $P$ un factor $S$ és: $$S_t = \frac{1}{(1-P)+\frac{P}{S}}$$ El màxim possible s'aconsegueix quan $\frac{P}{S}$ és $0$.