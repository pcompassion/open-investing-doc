**You:**

what is "standard" matrix for linear map ?

------------------

**ChatGPT:**

The "standard matrix" of a linear map refers to the matrix representation of that map with respect to the standard bases of the domain and codomain vector spaces.

To be more specific, let <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi><mo>:</mo><msup><mi mathvariant="double-struck">R</mi><mi>n</mi></msup><mo>→</mo><msup><mi mathvariant="double-struck">R</mi><mi>m</mi></msup></mrow><annotation encoding="application/x-tex">T: \mathbb{R}^n \to \mathbb{R}^m</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T<span class="mspace" style="margin-right: 0.2778em;">:<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 0.6889em;">R<span class="vlist" style="height: 0.6644em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n<span class="mspace" style="margin-right: 0.2778em;">→<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 0.6889em;">R<span class="vlist" style="height: 0.6644em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">m be a linear transformation. Let <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msub><mi>e</mi><mn>1</mn></msub><mo separator="true">,</mo><msub><mi>e</mi><mn>2</mn></msub><mo separator="true">,</mo><mo>…</mo><mo separator="true">,</mo><msub><mi>e</mi><mi>n</mi></msub></mrow><annotation encoding="application/x-tex">e_1, e_2, \dots, e_n</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.625em; vertical-align: -0.1944em;">e<span class="vlist" style="height: 0.3011em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">1​<span class="vlist" style="height: 0.15em;">,<span class="mspace" style="margin-right: 0.1667em;">e<span class="vlist" style="height: 0.3011em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">2​<span class="vlist" style="height: 0.15em;">,<span class="mspace" style="margin-right: 0.1667em;">…<span class="mspace" style="margin-right: 0.1667em;">,<span class="mspace" style="margin-right: 0.1667em;">e<span class="vlist" style="height: 0.1514em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n​<span class="vlist" style="height: 0.15em;"> be the standard basis for <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi mathvariant="double-struck">R</mi><mi>n</mi></msup></mrow><annotation encoding="application/x-tex">\mathbb{R}^n</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6889em;">R<span class="vlist" style="height: 0.6644em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n where <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msub><mi>e</mi><mi>i</mi></msub></mrow><annotation encoding="application/x-tex">e_i</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.5806em; vertical-align: -0.15em;">e<span class="vlist" style="height: 0.3117em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">i​<span class="vlist" style="height: 0.15em;"> is the vector with a 1 in the i-th position and zeros elsewhere. Let's determine how <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi></mrow><annotation encoding="application/x-tex">T</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T acts on each of these standard basis vectors:

<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi><mo stretchy="false">(</mo><msub><mi>e</mi><mn>1</mn></msub><mo stretchy="false">)</mo><mo separator="true">,</mo><mi>T</mi><mo stretchy="false">(</mo><msub><mi>e</mi><mn>2</mn></msub><mo stretchy="false">)</mo><mo separator="true">,</mo><mo>…</mo><mo separator="true">,</mo><mi>T</mi><mo stretchy="false">(</mo><msub><mi>e</mi><mi>n</mi></msub><mo stretchy="false">)</mo></mrow><annotation encoding="application/x-tex">T(e_1), T(e_2), \dots, T(e_n)</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T(e<span class="vlist" style="height: 0.3011em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">1​<span class="vlist" style="height: 0.15em;">),<span class="mspace" style="margin-right: 0.1667em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T(e<span class="vlist" style="height: 0.3011em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">2​<span class="vlist" style="height: 0.15em;">),<span class="mspace" style="margin-right: 0.1667em;">…<span class="mspace" style="margin-right: 0.1667em;">,<span class="mspace" style="margin-right: 0.1667em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T(e<span class="vlist" style="height: 0.1514em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n​<span class="vlist" style="height: 0.15em;">)

Each of these vectors <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi><mo stretchy="false">(</mo><msub><mi>e</mi><mi>i</mi></msub><mo stretchy="false">)</mo></mrow><annotation encoding="application/x-tex">T(e_i)</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T(e<span class="vlist" style="height: 0.3117em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">i​<span class="vlist" style="height: 0.15em;">) can be written as a column vector in <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi mathvariant="double-struck">R</mi><mi>m</mi></msup></mrow><annotation encoding="application/x-tex">\mathbb{R}^m</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6889em;">R<span class="vlist" style="height: 0.6644em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">m. The standard matrix <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>A</mi></mrow><annotation encoding="application/x-tex">A</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;">A of <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi></mrow><annotation encoding="application/x-tex">T</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T is the m x n matrix whose columns are these vectors:

<span class="katex-error" title="ParseError: KaTeX parse error: Expected 'EOF', got '&amp;' at position 3: | &amp;̲ | &amp; &amp; | \\
T(e…" style="color: rgb(204, 0, 0);">| &amp; | &amp; &amp; | \\
T(e_1) &amp; T(e_2) &amp; \dots &amp; T(e_n) \\
| &amp; | &amp; &amp; |
\end{bmatrix} \]
In essence, to get the standard matrix for a linear transformation, apply the transformation to each of the standard basis vectors of the domain, and use the resulting vectors as columns of the matrix.
The significance of the standard matrix is that, given a vector \( v \) in \( \mathbb{R}^n \), the product \( Av \) is equal to \( T(v) \). The matrix multiplication essentially computes the action of the linear transformation on \( v \).

------------------

**You:**

why some of your mathjx format is broken for display? i should install some plugin ?

------------------

**ChatGPT:**

I apologize for the inconvenience. The formatting issue is not on your end, but rather on how the text is being rendered in this interface.

Let me try to provide a clearer representation of the information:

Given a linear transformation <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi><mo>:</mo><msup><mi mathvariant="double-struck">R</mi><mi>n</mi></msup><mo>→</mo><msup><mi mathvariant="double-struck">R</mi><mi>m</mi></msup></mrow><annotation encoding="application/x-tex">T: \mathbb{R}^n \rightarrow \mathbb{R}^m</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T<span class="mspace" style="margin-right: 0.2778em;">:<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 0.6889em;">R<span class="vlist" style="height: 0.6644em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n<span class="mspace" style="margin-right: 0.2778em;">→<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 0.6889em;">R<span class="vlist" style="height: 0.6644em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">m, if we apply this transformation to the standard basis vectors <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msub><mi>e</mi><mn>1</mn></msub><mo separator="true">,</mo><msub><mi>e</mi><mn>2</mn></msub><mo separator="true">,</mo><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mo separator="true">,</mo><msub><mi>e</mi><mi>n</mi></msub></mrow><annotation encoding="application/x-tex">e_1, e_2, ..., e_n</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.625em; vertical-align: -0.1944em;">e<span class="vlist" style="height: 0.3011em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">1​<span class="vlist" style="height: 0.15em;">,<span class="mspace" style="margin-right: 0.1667em;">e<span class="vlist" style="height: 0.3011em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">2​<span class="vlist" style="height: 0.15em;">,<span class="mspace" style="margin-right: 0.1667em;">...,<span class="mspace" style="margin-right: 0.1667em;">e<span class="vlist" style="height: 0.1514em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n​<span class="vlist" style="height: 0.15em;"> of <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi mathvariant="double-struck">R</mi><mi>n</mi></msup></mrow><annotation encoding="application/x-tex">\mathbb{R}^n</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6889em;">R<span class="vlist" style="height: 0.6644em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n, we'll get the vectors:

<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi><mo stretchy="false">(</mo><msub><mi>e</mi><mn>1</mn></msub><mo stretchy="false">)</mo><mo separator="true">,</mo><mi>T</mi><mo stretchy="false">(</mo><msub><mi>e</mi><mn>2</mn></msub><mo stretchy="false">)</mo><mo separator="true">,</mo><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mo separator="true">,</mo><mi>T</mi><mo stretchy="false">(</mo><msub><mi>e</mi><mi>n</mi></msub><mo stretchy="false">)</mo></mrow><annotation encoding="application/x-tex">T(e_1), T(e_2), ..., T(e_n)</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T(e<span class="vlist" style="height: 0.3011em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">1​<span class="vlist" style="height: 0.15em;">),<span class="mspace" style="margin-right: 0.1667em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T(e<span class="vlist" style="height: 0.3011em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">2​<span class="vlist" style="height: 0.15em;">),<span class="mspace" style="margin-right: 0.1667em;">...,<span class="mspace" style="margin-right: 0.1667em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T(e<span class="vlist" style="height: 0.1514em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n​<span class="vlist" style="height: 0.15em;">)

The standard matrix <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>A</mi></mrow><annotation encoding="application/x-tex">A</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;">A of <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi></mrow><annotation encoding="application/x-tex">T</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T is constructed by placing each of these vectors as columns in the matrix:

<math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><mi>A</mi><mo>=</mo><mrow><mo fence="true">[</mo><mtable rowspacing="0.16em" columnalign="center center center center" columnspacing="1em"><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mi mathvariant="normal">∣</mi></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mi mathvariant="normal">∣</mi></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mo lspace="0em" rspace="0em">…</mo></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mi mathvariant="normal">∣</mi></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mrow><mi>T</mi><mo stretchy="false">(</mo><msub><mi>e</mi><mn>1</mn></msub><mo stretchy="false">)</mo></mrow></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mrow><mi>T</mi><mo stretchy="false">(</mo><msub><mi>e</mi><mn>2</mn></msub><mo stretchy="false">)</mo></mrow></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mo lspace="0em" rspace="0em">…</mo></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mrow><mi>T</mi><mo stretchy="false">(</mo><msub><mi>e</mi><mi>n</mi></msub><mo stretchy="false">)</mo></mrow></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mi mathvariant="normal">∣</mi></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mi mathvariant="normal">∣</mi></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mo lspace="0em" rspace="0em">…</mo></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mi mathvariant="normal">∣</mi></mstyle></mtd></mtr></mtable><mo fence="true">]</mo></mrow></mrow><annotation encoding="application/x-tex">A =
\begin{bmatrix}
| &amp; | &amp; \dots &amp; | \\
T(e_1) &amp; T(e_2) &amp; \dots &amp; T(e_n) \\
| &amp; | &amp; \dots &amp; |
\end{bmatrix} </annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;">A<span class="mspace" style="margin-right: 0.2778em;">=<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 3.6em; vertical-align: -1.55em;"><span class="vlist" style="height: 2.05em;"><span style="top: -2.25em;"><span class="pstrut" style="height: 3.155em;">⎣<span style="top: -3.397em;"><span class="pstrut" style="height: 3.155em;"><span style="height: 0.016em; width: 0.6667em;"><svg xmlns="http://www.w3.org/2000/svg" width="0.6667em" height="0.016em" viewBox="0 0 666.67 16" preserveAspectRatio="xMinYMin" style="width: 0.6667em;"><path d="M319 0 H403 V16 H319z M319 0 H403 V16 H319z"></path></svg><span style="top: -4.05em;"><span class="pstrut" style="height: 3.155em;">⎡​<span class="vlist" style="height: 1.55em;"><span class="vlist" style="height: 2.05em;"><span style="top: -4.21em;"><span class="pstrut" style="height: 3em;">∣<span style="top: -3.01em;"><span class="pstrut" style="height: 3em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T(e<span class="vlist" style="height: 0.3011em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">1​<span class="vlist" style="height: 0.15em;">)<span style="top: -1.81em;"><span class="pstrut" style="height: 3em;">∣​<span class="vlist" style="height: 1.55em;"><span class="arraycolsep" style="width: 0.5em;"><span class="arraycolsep" style="width: 0.5em;"><span class="vlist" style="height: 2.05em;"><span style="top: -4.21em;"><span class="pstrut" style="height: 3em;">∣<span style="top: -3.01em;"><span class="pstrut" style="height: 3em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T(e<span class="vlist" style="height: 0.3011em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">2​<span class="vlist" style="height: 0.15em;">)<span style="top: -1.81em;"><span class="pstrut" style="height: 3em;">∣​<span class="vlist" style="height: 1.55em;"><span class="arraycolsep" style="width: 0.5em;"><span class="arraycolsep" style="width: 0.5em;"><span class="vlist" style="height: 2.05em;"><span style="top: -4.21em;"><span class="pstrut" style="height: 3em;">…<span style="top: -3.01em;"><span class="pstrut" style="height: 3em;">…<span style="top: -1.81em;"><span class="pstrut" style="height: 3em;">…​<span class="vlist" style="height: 1.55em;"><span class="arraycolsep" style="width: 0.5em;"><span class="arraycolsep" style="width: 0.5em;"><span class="vlist" style="height: 2.05em;"><span style="top: -4.21em;"><span class="pstrut" style="height: 3em;">∣<span style="top: -3.01em;"><span class="pstrut" style="height: 3em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T(e<span class="vlist" style="height: 0.1514em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n​<span class="vlist" style="height: 0.15em;">)<span style="top: -1.81em;"><span class="pstrut" style="height: 3em;">∣​<span class="vlist" style="height: 1.55em;"><span class="vlist" style="height: 2.05em;"><span style="top: -2.25em;"><span class="pstrut" style="height: 3.155em;">⎦<span style="top: -3.397em;"><span class="pstrut" style="height: 3.155em;"><span style="height: 0.016em; width: 0.6667em;"><svg xmlns="http://www.w3.org/2000/svg" width="0.6667em" height="0.016em" viewBox="0 0 666.67 16" preserveAspectRatio="xMinYMin" style="width: 0.6667em;"><path d="M263 0 H347 V16 H263z M263 0 H347 V16 H263z"></path></svg><span style="top: -4.05em;"><span class="pstrut" style="height: 3.155em;">⎤​<span class="vlist" style="height: 1.55em;">When you have this standard matrix <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>A</mi></mrow><annotation encoding="application/x-tex">A</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;">A, given any vector <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>v</mi></mrow><annotation encoding="application/x-tex">v</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.4306em;"><span class="mord mathnormal" style="margin-right: 0.03588em;">v in <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi mathvariant="double-struck">R</mi><mi>n</mi></msup></mrow><annotation encoding="application/x-tex">\mathbb{R}^n</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6889em;">R<span class="vlist" style="height: 0.6644em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n, the product <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>A</mi><mi>v</mi></mrow><annotation encoding="application/x-tex">Av</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;">A<span class="mord mathnormal" style="margin-right: 0.03588em;">v gives <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi><mo stretchy="false">(</mo><mi>v</mi><mo stretchy="false">)</mo></mrow><annotation encoding="application/x-tex">T(v)</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T(<span class="mord mathnormal" style="margin-right: 0.03588em;">v).

You don't need to install any plugins. If the formatting is unclear, please let me know, and I'll do my best to represent it in a more readable manner.



------------------

**You:**

ok for R^n space, i can see what standard basis is, 
but say, we are talking about vector space of polyonmial function, it's not [1, 0, 0] , [0,1,0] and so on. 
so how to make e1 so that T(e1) makes sense concerning 'standard' matrix

------------------

**ChatGPT:**

Great observation! The concept of a "standard basis" isn't restricted to <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi mathvariant="double-struck">R</mi><mi>n</mi></msup></mrow><annotation encoding="application/x-tex">\mathbb{R}^n</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6889em;">R<span class="vlist" style="height: 0.6644em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n. Different vector spaces have their own "standard" or "natural" bases that make sense in their context.

For the vector space of polynomials (let's take polynomials of degree <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>n</mi></mrow><annotation encoding="application/x-tex">n</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.4306em;">n or less for simplicity), the standard basis is typically the set of monomials. For polynomials of degree <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mn>2</mn></mrow><annotation encoding="application/x-tex">2</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6444em;">2 or less, the standard basis is:

<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mo stretchy="false">{</mo><mn>1</mn><mo separator="true">,</mo><mi>x</mi><mo separator="true">,</mo><msup><mi>x</mi><mn>2</mn></msup><mo stretchy="false">}</mo></mrow><annotation encoding="application/x-tex">\{ 1, x, x^2 \}</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1.0641em; vertical-align: -0.25em;">{1,<span class="mspace" style="margin-right: 0.1667em;">x,<span class="mspace" style="margin-right: 0.1667em;">x<span class="vlist" style="height: 0.8141em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">2}

In this basis, the polynomial <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mn>3</mn><mo>+</mo><mn>2</mn><mi>x</mi><mo>−</mo><msup><mi>x</mi><mn>2</mn></msup></mrow><annotation encoding="application/x-tex">3 + 2x - x^2</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.7278em; vertical-align: -0.0833em;">3<span class="mspace" style="margin-right: 0.2222em;">+<span class="mspace" style="margin-right: 0.2222em;"><span class="strut" style="height: 0.7278em; vertical-align: -0.0833em;">2x<span class="mspace" style="margin-right: 0.2222em;">−<span class="mspace" style="margin-right: 0.2222em;"><span class="strut" style="height: 0.8141em;">x<span class="vlist" style="height: 0.8141em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">2 would be represented as the coordinate vector:

<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mo fence="true">[</mo><mtable rowspacing="0.16em" columnalign="center" columnspacing="1em"><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>3</mn></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>2</mn></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mrow><mo>−</mo><mn>1</mn></mrow></mstyle></mtd></mtr></mtable><mo fence="true">]</mo></mrow><annotation encoding="application/x-tex">\begin{bmatrix} 3 \\ 2 \\ -1 \end{bmatrix}</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 3.6em; vertical-align: -1.55em;"><span class="vlist" style="height: 2.05em;"><span style="top: -2.25em;"><span class="pstrut" style="height: 3.155em;">⎣<span style="top: -3.397em;"><span class="pstrut" style="height: 3.155em;"><span style="height: 0.016em; width: 0.6667em;"><svg xmlns="http://www.w3.org/2000/svg" width="0.6667em" height="0.016em" viewBox="0 0 666.67 16" preserveAspectRatio="xMinYMin" style="width: 0.6667em;"><path d="M319 0 H403 V16 H319z M319 0 H403 V16 H319z"></path></svg><span style="top: -4.05em;"><span class="pstrut" style="height: 3.155em;">⎡​<span class="vlist" style="height: 1.55em;"><span class="vlist" style="height: 2.05em;"><span style="top: -4.21em;"><span class="pstrut" style="height: 3em;">3<span style="top: -3.01em;"><span class="pstrut" style="height: 3em;">2<span style="top: -1.81em;"><span class="pstrut" style="height: 3em;">−1​<span class="vlist" style="height: 1.55em;"><span class="vlist" style="height: 2.05em;"><span style="top: -2.25em;"><span class="pstrut" style="height: 3.155em;">⎦<span style="top: -3.397em;"><span class="pstrut" style="height: 3.155em;"><span style="height: 0.016em; width: 0.6667em;"><svg xmlns="http://www.w3.org/2000/svg" width="0.6667em" height="0.016em" viewBox="0 0 666.67 16" preserveAspectRatio="xMinYMin" style="width: 0.6667em;"><path d="M263 0 H347 V16 H263z M263 0 H347 V16 H263z"></path></svg><span style="top: -4.05em;"><span class="pstrut" style="height: 3.155em;">⎤​<span class="vlist" style="height: 1.55em;">

If you had a linear transformation <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi></mrow><annotation encoding="application/x-tex">T</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T that acts on this polynomial space, to find the standard matrix with respect to this basis, you'd evaluate:

<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi><mo stretchy="false">(</mo><mn>1</mn><mo stretchy="false">)</mo></mrow><annotation encoding="application/x-tex">T(1)</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T(1)
<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi><mo stretchy="false">(</mo><mi>x</mi><mo stretchy="false">)</mo></mrow><annotation encoding="application/x-tex">T(x)</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T(x)
<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi><mo stretchy="false">(</mo><msup><mi>x</mi><mn>2</mn></msup><mo stretchy="false">)</mo></mrow><annotation encoding="application/x-tex">T(x^2)</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1.0641em; vertical-align: -0.25em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T(x<span class="vlist" style="height: 0.8141em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">2)

And you'd use these as columns in your matrix, just like before.

For example, consider a transformation that differentiates polynomials. For the basis {1, x, x^2}, the transformation of differentiation gives:

<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi><mo stretchy="false">(</mo><mn>1</mn><mo stretchy="false">)</mo><mo>=</mo><mn>0</mn></mrow><annotation encoding="application/x-tex">T(1) = 0</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T(1)<span class="mspace" style="margin-right: 0.2778em;">=<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 0.6444em;">0
<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi><mo stretchy="false">(</mo><mi>x</mi><mo stretchy="false">)</mo><mo>=</mo><mn>1</mn></mrow><annotation encoding="application/x-tex">T(x) = 1</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T(x)<span class="mspace" style="margin-right: 0.2778em;">=<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 0.6444em;">1
<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi><mo stretchy="false">(</mo><msup><mi>x</mi><mn>2</mn></msup><mo stretchy="false">)</mo><mo>=</mo><mn>2</mn><mi>x</mi></mrow><annotation encoding="application/x-tex">T(x^2) = 2x</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1.0641em; vertical-align: -0.25em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T(x<span class="vlist" style="height: 0.8141em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">2)<span class="mspace" style="margin-right: 0.2778em;">=<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 0.6444em;">2x

If we were looking at polynomials of degree 2 or less, then the standard matrix representation of differentiation, with respect to the basis {1, x, x^2}, would be:

<math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><mi>A</mi><mo>=</mo><mrow><mo fence="true">[</mo><mtable rowspacing="0.16em" columnalign="center center center" columnspacing="1em"><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>1</mn></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>2</mn></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd></mtr></mtable><mo fence="true">]</mo></mrow></mrow><annotation encoding="application/x-tex">A =
\begin{bmatrix}
0 &amp; 1 &amp; 0 \\
0 &amp; 0 &amp; 2 \\
0 &amp; 0 &amp; 0 \\
\end{bmatrix} </annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;">A<span class="mspace" style="margin-right: 0.2778em;">=<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 3.6em; vertical-align: -1.55em;"><span class="vlist" style="height: 2.05em;"><span style="top: -2.25em;"><span class="pstrut" style="height: 3.155em;">⎣<span style="top: -3.397em;"><span class="pstrut" style="height: 3.155em;"><span style="height: 0.016em; width: 0.6667em;"><svg xmlns="http://www.w3.org/2000/svg" width="0.6667em" height="0.016em" viewBox="0 0 666.67 16" preserveAspectRatio="xMinYMin" style="width: 0.6667em;"><path d="M319 0 H403 V16 H319z M319 0 H403 V16 H319z"></path></svg><span style="top: -4.05em;"><span class="pstrut" style="height: 3.155em;">⎡​<span class="vlist" style="height: 1.55em;"><span class="vlist" style="height: 2.05em;"><span style="top: -4.21em;"><span class="pstrut" style="height: 3em;">0<span style="top: -3.01em;"><span class="pstrut" style="height: 3em;">0<span style="top: -1.81em;"><span class="pstrut" style="height: 3em;">0​<span class="vlist" style="height: 1.55em;"><span class="arraycolsep" style="width: 0.5em;"><span class="arraycolsep" style="width: 0.5em;"><span class="vlist" style="height: 2.05em;"><span style="top: -4.21em;"><span class="pstrut" style="height: 3em;">1<span style="top: -3.01em;"><span class="pstrut" style="height: 3em;">0<span style="top: -1.81em;"><span class="pstrut" style="height: 3em;">0​<span class="vlist" style="height: 1.55em;"><span class="arraycolsep" style="width: 0.5em;"><span class="arraycolsep" style="width: 0.5em;"><span class="vlist" style="height: 2.05em;"><span style="top: -4.21em;"><span class="pstrut" style="height: 3em;">0<span style="top: -3.01em;"><span class="pstrut" style="height: 3em;">2<span style="top: -1.81em;"><span class="pstrut" style="height: 3em;">0​<span class="vlist" style="height: 1.55em;"><span class="vlist" style="height: 2.05em;"><span style="top: -2.25em;"><span class="pstrut" style="height: 3.155em;">⎦<span style="top: -3.397em;"><span class="pstrut" style="height: 3.155em;"><span style="height: 0.016em; width: 0.6667em;"><svg xmlns="http://www.w3.org/2000/svg" width="0.6667em" height="0.016em" viewBox="0 0 666.67 16" preserveAspectRatio="xMinYMin" style="width: 0.6667em;"><path d="M263 0 H347 V16 H263z M263 0 H347 V16 H263z"></path></svg><span style="top: -4.05em;"><span class="pstrut" style="height: 3.155em;">⎤​<span class="vlist" style="height: 1.55em;">This is just an example, but it shows how you'd construct the "standard" matrix for a linear transformation on a polynomial space.



------------------

**You:**

ok, good, but polynormial space is just an example, so 
"standard matrix" implies this sort of representing arbitrary vector space with (1,0,0) (0,1,0) is always possible?

------------------

**ChatGPT:**

No, the concept of the "standard matrix" as defined for <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi mathvariant="double-struck">R</mi><mi>n</mi></msup></mrow><annotation encoding="application/x-tex">\mathbb{R}^n</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6889em;">R<span class="vlist" style="height: 0.6644em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n with basis vectors like <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mo stretchy="false">(</mo><mn>1</mn><mo separator="true">,</mo><mn>0</mn><mo separator="true">,</mo><mn>0</mn><mo stretchy="false">)</mo><mo separator="true">,</mo><mo stretchy="false">(</mo><mn>0</mn><mo separator="true">,</mo><mn>1</mn><mo separator="true">,</mo><mn>0</mn><mo stretchy="false">)</mo><mo separator="true">,</mo><mo>…</mo></mrow><annotation encoding="application/x-tex">(1,0,0), (0,1,0), \ldots</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;">(1,<span class="mspace" style="margin-right: 0.1667em;">0,<span class="mspace" style="margin-right: 0.1667em;">0),<span class="mspace" style="margin-right: 0.1667em;">(0,<span class="mspace" style="margin-right: 0.1667em;">1,<span class="mspace" style="margin-right: 0.1667em;">0),<span class="mspace" style="margin-right: 0.1667em;">… is specific to Euclidean space. But the general idea of representing a linear transformation with a matrix relative to some chosen basis extends to arbitrary vector spaces, though the choice of basis and its representation may vary.

For arbitrary vector spaces, the concept goes as follows:


- Choose a basis for your vector space. This basis may not look like
(
1
,
0
,
0
)
,
(
0
,
1
,
0
)
,
…
(1,0,0), (0,1,0), \ldots
(1,
0,
0),
(0,
1,
0),
… but is a set of linearly independent vectors that span your space.
- For each basis vector, apply the linear transformation to it.
- Represent the transformed vector in terms of the chosen basis.
- The coefficients obtained in step 3 form columns of the matrix representation of the linear transformation with respect to the chosen basis.

The term "standard matrix" (in the context of <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi mathvariant="double-struck">R</mi><mi>n</mi></msup></mrow><annotation encoding="application/x-tex">\mathbb{R}^n</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6889em;">R<span class="vlist" style="height: 0.6644em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n) implies using the standard basis for Euclidean space. But in general vector spaces, the term "matrix representation of a linear transformation with respect to a basis" is more appropriate. The choice of basis can greatly affect the matrix representation. Some bases can simplify the matrix considerably.

For example, in a vector space of 2x2 matrices, the basis could be:

<math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><mrow><mo fence="true">[</mo><mtable rowspacing="0.16em" columnalign="center center" columnspacing="1em"><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>1</mn></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd></mtr></mtable><mo fence="true">]</mo></mrow><mo separator="true">,</mo><mrow><mo fence="true">[</mo><mtable rowspacing="0.16em" columnalign="center center" columnspacing="1em"><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>1</mn></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd></mtr></mtable><mo fence="true">]</mo></mrow><mo separator="true">,</mo><mrow><mo fence="true">[</mo><mtable rowspacing="0.16em" columnalign="center center" columnspacing="1em"><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>1</mn></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd></mtr></mtable><mo fence="true">]</mo></mrow><mo separator="true">,</mo><mrow><mo fence="true">[</mo><mtable rowspacing="0.16em" columnalign="center center" columnspacing="1em"><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>1</mn></mstyle></mtd></mtr></mtable><mo fence="true">]</mo></mrow></mrow><annotation encoding="application/x-tex">\begin{bmatrix}
1 &amp; 0 \\
0 &amp; 0
\end{bmatrix},
\begin{bmatrix}
0 &amp; 1 \\
0 &amp; 0
\end{bmatrix},
\begin{bmatrix}
0 &amp; 0 \\
1 &amp; 0
\end{bmatrix},
\begin{bmatrix}
0 &amp; 0 \\
0 &amp; 1
\end{bmatrix} </annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 2.4em; vertical-align: -0.95em;"><span class="mopen delimcenter" style="top: 0em;">[<span class="vlist" style="height: 1.45em;"><span style="top: -3.61em;"><span class="pstrut" style="height: 3em;">1<span style="top: -2.41em;"><span class="pstrut" style="height: 3em;">0​<span class="vlist" style="height: 0.95em;"><span class="arraycolsep" style="width: 0.5em;"><span class="arraycolsep" style="width: 0.5em;"><span class="vlist" style="height: 1.45em;"><span style="top: -3.61em;"><span class="pstrut" style="height: 3em;">0<span style="top: -2.41em;"><span class="pstrut" style="height: 3em;">0​<span class="vlist" style="height: 0.95em;"><span class="mclose delimcenter" style="top: 0em;">]<span class="mspace" style="margin-right: 0.1667em;">,<span class="mspace" style="margin-right: 0.1667em;"><span class="mopen delimcenter" style="top: 0em;">[<span class="vlist" style="height: 1.45em;"><span style="top: -3.61em;"><span class="pstrut" style="height: 3em;">0<span style="top: -2.41em;"><span class="pstrut" style="height: 3em;">0​<span class="vlist" style="height: 0.95em;"><span class="arraycolsep" style="width: 0.5em;"><span class="arraycolsep" style="width: 0.5em;"><span class="vlist" style="height: 1.45em;"><span style="top: -3.61em;"><span class="pstrut" style="height: 3em;">1<span style="top: -2.41em;"><span class="pstrut" style="height: 3em;">0​<span class="vlist" style="height: 0.95em;"><span class="mclose delimcenter" style="top: 0em;">]<span class="mspace" style="margin-right: 0.1667em;">,<span class="mspace" style="margin-right: 0.1667em;"><span class="mopen delimcenter" style="top: 0em;">[<span class="vlist" style="height: 1.45em;"><span style="top: -3.61em;"><span class="pstrut" style="height: 3em;">0<span style="top: -2.41em;"><span class="pstrut" style="height: 3em;">1​<span class="vlist" style="height: 0.95em;"><span class="arraycolsep" style="width: 0.5em;"><span class="arraycolsep" style="width: 0.5em;"><span class="vlist" style="height: 1.45em;"><span style="top: -3.61em;"><span class="pstrut" style="height: 3em;">0<span style="top: -2.41em;"><span class="pstrut" style="height: 3em;">0​<span class="vlist" style="height: 0.95em;"><span class="mclose delimcenter" style="top: 0em;">]<span class="mspace" style="margin-right: 0.1667em;">,<span class="mspace" style="margin-right: 0.1667em;"><span class="mopen delimcenter" style="top: 0em;">[<span class="vlist" style="height: 1.45em;"><span style="top: -3.61em;"><span class="pstrut" style="height: 3em;">0<span style="top: -2.41em;"><span class="pstrut" style="height: 3em;">0​<span class="vlist" style="height: 0.95em;"><span class="arraycolsep" style="width: 0.5em;"><span class="arraycolsep" style="width: 0.5em;"><span class="vlist" style="height: 1.45em;"><span style="top: -3.61em;"><span class="pstrut" style="height: 3em;">0<span style="top: -2.41em;"><span class="pstrut" style="height: 3em;">1​<span class="vlist" style="height: 0.95em;"><span class="mclose delimcenter" style="top: 0em;">]But again, the choice of basis is up to you, and the resulting matrix will vary accordingly.



------------------

**You:**

ok, i'm trying to understand 
The point of this subsection is to show that matrix multiplication corresponds to composition of transformations, that is, the standard matrix for 
T
◦
U
 is the product of the standard matrices for 
T
 and for 
U
.
 It should be hard to believe that our complicated formula for matrix multiplication actually means something intuitive such as “chaining two transformations together”!


I was under impression, that "matrix product" equal "composing transformation" would need assertion (that there's standard matrix for transformation , then i would need (1,0,0).. vector as i undersand it) .. 
am i wrong on this interpretation?

------------------

**ChatGPT:**

Your understanding is on the right track. The statement you're referring to is a foundational result that connects matrix multiplication with the composition of linear transformations. To clarify, let's break it down:


- **Linear Transformations and Their Matrices**: If you have a linear transformation from
R
n
\mathbb{R}^n
R
n to
R
m
\mathbb{R}^m
R
m (denoted
T
:
R
n
→
R
m
T: \mathbb{R}^n \rightarrow \mathbb{R}^m
T
:
R
n
→
R
m), and if you have a basis for
R
n
\mathbb{R}^n
R
n, then there is a unique matrix representation of that transformation with respect to that basis. For the standard basis in
R
n
\mathbb{R}^n
R
n (which is
(
1
,
0
,
…
,
0
)
,
(
0
,
1
,
0
,
…
,
0
)
,
…
(1,0,\dots,0), (0,1,0,\dots,0), \ldots
(1,
0,
…
,
0),
(0,
1,
0,
…
,
0),
…), we get what's called the "standard matrix" of
T
T
T.
- **Matrix Product Equals Composition**: Now, suppose you have two linear transformations:
   - U
   :
   R
   k
   →
   R
   n
   U: \mathbb{R}^k \rightarrow \mathbb{R}^n
   U
   :
   R
   k
   →
   R
   n with standard matrix
   A
   A
   A
   - T
   :
   R
   n
   →
   R
   m
   T: \mathbb{R}^n \rightarrow \mathbb{R}^m
   T
   :
   R
   n
   →
   R
   m with standard matrix
   B
   B
   B
Then, the composition of these transformations is
T
∘
U
:
R
k
→
R
m
T \circ U: \mathbb{R}^k \rightarrow \mathbb{R}^m
T
∘
U
:
R
k
→
R
m. The key result is that the standard matrix of
T
∘
U
T \circ U
T
∘
U is the product of the matrices
B
B
B and
A
A
A, in that order. Symbolically, if
C
C
C is the standard matrix of
T
∘
U
T \circ U
T
∘
U, then
C
=
B
A
C = BA
C
=
BA.
- **Intuition and the (1,0,...,0) Vector**: When we talk about the standard matrix of a transformation, we're essentially asking: "What happens to each of the standard basis vectors under this transformation?" These vectors, like
(
1
,
0
,
0
,
…

)
(1,0,0,\dots)
(1,
0,
0,
…
), are convenient because:
   - They span
   R
   n
   \mathbb{R}^n
   R
   n.
   - Each of them "picks out" a single coordinate, which makes it easy to figure out the action of the transformation on that coordinate.
But the assertion that "matrix product equals composing transformation" doesn't solely rely on the basis vectors being of the form
(
1
,
0
,
…
,
0
)
(1,0,\dots,0)
(1,
0,
…
,
0). The result holds true for any basis, but the standard basis is the most convenient for our typical matrix representations in
R
n
\mathbb{R}^n
R
n.

In essence, you're right: this is a deep and surprising result! The formula for matrix multiplication, which at first seems arbitrary and computational, has this beautiful geometric interpretation: it captures the chaining together of two transformations.



------------------

**You:**

ok, so statement "The point of this subsection is to show that matrix multiplication corresponds to composition of transformations," is generally true beyond R^n

and the proof using "standard matrix" is only partially proving the statement for R^n spaces? or it can be extended to arbitrary spaces (which I find hard to how to apply "standard" as you first described, for example for 2*2 matrix space, would the standard basis will be form of (2*2 matrix, 0, 0) ?

------------------

**ChatGPT:**

Absolutely right. The relationship between matrix multiplication and composition of transformations is a general fact, but the notion of "standard matrices" and the way they're often introduced is closely tied to <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi mathvariant="double-struck">R</mi><mi>n</mi></msup></mrow><annotation encoding="application/x-tex">\mathbb{R}^n</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6889em;">R<span class="vlist" style="height: 0.6644em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n.

Let's clarify a bit:


- **General Statement**: For any two linear transformations
U
U
U and
T
T
T (from and to vector spaces that allow composition), the matrix representation of their composition
T
∘
U
T \circ U
T
∘
U (with respect to appropriate bases) is the product of their respective matrix representations.
- **Proof in
R
n
\mathbb{R}^n
R
n**: This is often where students first encounter the concept. In
R
n
\mathbb{R}^n
R
n, the "standard matrix" of a transformation is its matrix representation with respect to the standard basis (like
(
1
,
0
,
0
,
…

)
,
(
0
,
1
,
0
,
…

)
,
…
(1,0,0,\dots), (0,1,0,\dots), \ldots
(1,
0,
0,
…
),
(0,
1,
0,
…
),
…). This provides a concrete setting in which to demonstrate the general fact. By showing it's true in this specific context, it provides an example of the broader principle.
- **Generalizing to Other Vector Spaces**: To generalize to other vector spaces (like the space of 2x2 matrices, polynomial spaces, function spaces, etc.), we do the following:
   - First, pick bases for your domain and codomain spaces. These don't need to be "standard" in the
   R
   n
   \mathbb{R}^n
   R
   n sense. They just need to be bases.
   - For each transformation, find its matrix representation with respect to these bases.
   - Show that the composition of the transformations corresponds to the multiplication of these matrices.
For instance, in the vector space of 2x2 matrices, a possible basis is the set of matrices:
[
1
0
0
0
]
,
[
0
1
0
0
]
,
[
0
0
1
0
]
,
[
0
0
0
1
]
\begin{bmatrix}
1 & 0 \\
0 & 0
\end{bmatrix},
\begin{bmatrix}
0 & 1 \\
0 & 0
\end{bmatrix},
\begin{bmatrix}
0 & 0 \\
1 & 0
\end{bmatrix},
\begin{bmatrix}
0 & 0 \\
0 & 1
\end{bmatrix}
[
1
0​
0
0​
]
,
[
0
0​
1
0​
]
,
[
0
1​
0
0​
]
,
[
0
0​
0
1​
]This basis has the same "standard" spirit as the
R
n
\mathbb{R}^n
R
n basis, but it's tailored to 2x2 matrices. For other spaces, you'd pick appropriate bases, but the underlying principle of matrix multiplication reflecting composition remains the same.



------------------

**You:**

ok so "standard matrix" makes sense when we talk about R^n (unless there's notion of standard basis in a vector space in question)

------------------

**ChatGPT:**

Yes, exactly. The term "standard matrix" is most directly associated with <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi mathvariant="double-struck">R</mi><mi>n</mi></msup></mrow><annotation encoding="application/x-tex">\mathbb{R}^n</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6889em;">R<span class="vlist" style="height: 0.6644em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n because of the well-understood "standard basis" in that context. When we're working in <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi mathvariant="double-struck">R</mi><mi>n</mi></msup></mrow><annotation encoding="application/x-tex">\mathbb{R}^n</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6889em;">R<span class="vlist" style="height: 0.6644em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n, the standard basis is:

<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msub><mi>e</mi><mn>1</mn></msub><mo>=</mo><mrow><mo fence="true">[</mo><mtable rowspacing="0.16em" columnalign="center" columnspacing="1em"><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>1</mn></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mi><mi mathvariant="normal">⋮</mi><mpadded height="0em" voffset="0em"><mspace mathbackground="black" width="0em" height="1.5em"></mspace></mpadded></mi></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd></mtr></mtable><mo fence="true">]</mo></mrow><mo separator="true">,</mo><msub><mi>e</mi><mn>2</mn></msub><mo>=</mo><mrow><mo fence="true">[</mo><mtable rowspacing="0.16em" columnalign="center" columnspacing="1em"><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>1</mn></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mi><mi mathvariant="normal">⋮</mi><mpadded height="0em" voffset="0em"><mspace mathbackground="black" width="0em" height="1.5em"></mspace></mpadded></mi></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd></mtr></mtable><mo fence="true">]</mo></mrow><mo separator="true">,</mo><mo>…</mo><mo separator="true">,</mo><msub><mi>e</mi><mi>n</mi></msub><mo>=</mo><mrow><mo fence="true">[</mo><mtable rowspacing="0.16em" columnalign="center" columnspacing="1em"><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>0</mn></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mi><mi mathvariant="normal">⋮</mi><mpadded height="0em" voffset="0em"><mspace mathbackground="black" width="0em" height="1.5em"></mspace></mpadded></mi></mstyle></mtd></mtr><mtr><mtd><mstyle scriptlevel="0" displaystyle="false"><mn>1</mn></mstyle></mtd></mtr></mtable><mo fence="true">]</mo></mrow></mrow><annotation encoding="application/x-tex">e_1 = \begin{bmatrix} 1 \\ 0 \\ \vdots \\ 0 \end{bmatrix}, e_2 = \begin{bmatrix} 0 \\ 1 \\ \vdots \\ 0 \end{bmatrix}, \ldots, e_n = \begin{bmatrix} 0 \\ 0 \\ \vdots \\ 1 \end{bmatrix}</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.5806em; vertical-align: -0.15em;">e<span class="vlist" style="height: 0.3011em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">1​<span class="vlist" style="height: 0.15em;"><span class="mspace" style="margin-right: 0.2778em;">=<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 5.46em; vertical-align: -2.48em;"><span class="vlist" style="height: 2.95em;"><span style="top: -2.011em;"><span class="pstrut" style="height: 3.816em;">⎣<span style="top: -3.158em;"><span class="pstrut" style="height: 3.816em;"><span style="height: 1.816em; width: 0.6667em;"><svg xmlns="http://www.w3.org/2000/svg" width="0.6667em" height="1.816em" viewBox="0 0 666.67 1816" preserveAspectRatio="xMinYMin" style="width: 0.6667em;"><path d="M319 0 H403 V1816 H319z M319 0 H403 V1816 H319z"></path></svg><span style="top: -5.6111em;"><span class="pstrut" style="height: 3.816em;">⎡​<span class="vlist" style="height: 2.45em;"><span class="vlist" style="height: 2.98em;"><span style="top: -5.8275em;"><span class="pstrut" style="height: 3.6875em;">1<span style="top: -4.6275em;"><span class="pstrut" style="height: 3.6875em;">0<span style="top: -2.7675em;"><span class="pstrut" style="height: 3.6875em;">⋮<span class="mord rule" style="border-right-width: 0em; border-top-width: 1.5em; bottom: 0em;"><span style="top: -1.5675em;"><span class="pstrut" style="height: 3.6875em;">0​<span class="vlist" style="height: 2.48em;"><span class="vlist" style="height: 2.95em;"><span style="top: -2.011em;"><span class="pstrut" style="height: 3.816em;">⎦<span style="top: -3.158em;"><span class="pstrut" style="height: 3.816em;"><span style="height: 1.816em; width: 0.6667em;"><svg xmlns="http://www.w3.org/2000/svg" width="0.6667em" height="1.816em" viewBox="0 0 666.67 1816" preserveAspectRatio="xMinYMin" style="width: 0.6667em;"><path d="M263 0 H347 V1816 H263z M263 0 H347 V1816 H263z"></path></svg><span style="top: -5.6111em;"><span class="pstrut" style="height: 3.816em;">⎤​<span class="vlist" style="height: 2.45em;"><span class="mspace" style="margin-right: 0.1667em;">,<span class="mspace" style="margin-right: 0.1667em;">e<span class="vlist" style="height: 0.3011em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">2​<span class="vlist" style="height: 0.15em;"><span class="mspace" style="margin-right: 0.2778em;">=<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 5.46em; vertical-align: -2.48em;"><span class="vlist" style="height: 2.95em;"><span style="top: -2.011em;"><span class="pstrut" style="height: 3.816em;">⎣<span style="top: -3.158em;"><span class="pstrut" style="height: 3.816em;"><span style="height: 1.816em; width: 0.6667em;"><svg xmlns="http://www.w3.org/2000/svg" width="0.6667em" height="1.816em" viewBox="0 0 666.67 1816" preserveAspectRatio="xMinYMin" style="width: 0.6667em;"><path d="M319 0 H403 V1816 H319z M319 0 H403 V1816 H319z"></path></svg><span style="top: -5.6111em;"><span class="pstrut" style="height: 3.816em;">⎡​<span class="vlist" style="height: 2.45em;"><span class="vlist" style="height: 2.98em;"><span style="top: -5.8275em;"><span class="pstrut" style="height: 3.6875em;">0<span style="top: -4.6275em;"><span class="pstrut" style="height: 3.6875em;">1<span style="top: -2.7675em;"><span class="pstrut" style="height: 3.6875em;">⋮<span class="mord rule" style="border-right-width: 0em; border-top-width: 1.5em; bottom: 0em;"><span style="top: -1.5675em;"><span class="pstrut" style="height: 3.6875em;">0​<span class="vlist" style="height: 2.48em;"><span class="vlist" style="height: 2.95em;"><span style="top: -2.011em;"><span class="pstrut" style="height: 3.816em;">⎦<span style="top: -3.158em;"><span class="pstrut" style="height: 3.816em;"><span style="height: 1.816em; width: 0.6667em;"><svg xmlns="http://www.w3.org/2000/svg" width="0.6667em" height="1.816em" viewBox="0 0 666.67 1816" preserveAspectRatio="xMinYMin" style="width: 0.6667em;"><path d="M263 0 H347 V1816 H263z M263 0 H347 V1816 H263z"></path></svg><span style="top: -5.6111em;"><span class="pstrut" style="height: 3.816em;">⎤​<span class="vlist" style="height: 2.45em;"><span class="mspace" style="margin-right: 0.1667em;">,<span class="mspace" style="margin-right: 0.1667em;">…<span class="mspace" style="margin-right: 0.1667em;">,<span class="mspace" style="margin-right: 0.1667em;">e<span class="vlist" style="height: 0.1514em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n​<span class="vlist" style="height: 0.15em;"><span class="mspace" style="margin-right: 0.2778em;">=<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 5.46em; vertical-align: -2.48em;"><span class="vlist" style="height: 2.95em;"><span style="top: -2.011em;"><span class="pstrut" style="height: 3.816em;">⎣<span style="top: -3.158em;"><span class="pstrut" style="height: 3.816em;"><span style="height: 1.816em; width: 0.6667em;"><svg xmlns="http://www.w3.org/2000/svg" width="0.6667em" height="1.816em" viewBox="0 0 666.67 1816" preserveAspectRatio="xMinYMin" style="width: 0.6667em;"><path d="M319 0 H403 V1816 H319z M319 0 H403 V1816 H319z"></path></svg><span style="top: -5.6111em;"><span class="pstrut" style="height: 3.816em;">⎡​<span class="vlist" style="height: 2.45em;"><span class="vlist" style="height: 2.98em;"><span style="top: -5.8275em;"><span class="pstrut" style="height: 3.6875em;">0<span style="top: -4.6275em;"><span class="pstrut" style="height: 3.6875em;">0<span style="top: -2.7675em;"><span class="pstrut" style="height: 3.6875em;">⋮<span class="mord rule" style="border-right-width: 0em; border-top-width: 1.5em; bottom: 0em;"><span style="top: -1.5675em;"><span class="pstrut" style="height: 3.6875em;">1​<span class="vlist" style="height: 2.48em;"><span class="vlist" style="height: 2.95em;"><span style="top: -2.011em;"><span class="pstrut" style="height: 3.816em;">⎦<span style="top: -3.158em;"><span class="pstrut" style="height: 3.816em;"><span style="height: 1.816em; width: 0.6667em;"><svg xmlns="http://www.w3.org/2000/svg" width="0.6667em" height="1.816em" viewBox="0 0 666.67 1816" preserveAspectRatio="xMinYMin" style="width: 0.6667em;"><path d="M263 0 H347 V1816 H263z M263 0 H347 V1816 H263z"></path></svg><span style="top: -5.6111em;"><span class="pstrut" style="height: 3.816em;">⎤​<span class="vlist" style="height: 2.45em;">

The "standard matrix" of a linear transformation <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi></mrow><annotation encoding="application/x-tex">T</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T from <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi mathvariant="double-struck">R</mi><mi>n</mi></msup></mrow><annotation encoding="application/x-tex">\mathbb{R}^n</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6889em;">R<span class="vlist" style="height: 0.6644em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n to <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi mathvariant="double-struck">R</mi><mi>m</mi></msup></mrow><annotation encoding="application/x-tex">\mathbb{R}^m</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6889em;">R<span class="vlist" style="height: 0.6644em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">m is the matrix whose columns are the images of these standard basis vectors under <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi></mrow><annotation encoding="application/x-tex">T</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T.

When moving to other vector spaces, the notion of a "standard" basis is less clear, unless there's a conventionally accepted basis for that space (like monomials for polynomial spaces). In general, you could have many possible bases for a given vector space, and the matrix representation of a linear transformation will depend on the chosen basis.

So, when discussing matrix representations of linear transformations in arbitrary vector spaces, it's more precise to talk about "the matrix representation of <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>T</mi></mrow><annotation encoding="application/x-tex">T</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">T with respect to a particular basis" rather than using the term "standard matrix" unless there's a widely accepted "standard" basis for that space.



------------------

**You:**

so let's go back. "The point of this subsection is to show that matrix multiplication corresponds to composition of transformations"

I first need to state, that any linear map can be represented as matrix, 
then, matrix multiplication corresponds to composition, 
what's the sketch idea how to prove the two staetements?

------------------

**ChatGPT:**

Absolutely, let's tackle these two points step-by-step.

### 1. Any Linear Map Can Be Represented as a Matrix
**Sketch of the Proof**:


- **Pick a Basis**: Start by picking bases for your domain and codomain vector spaces. Let's say the vector space of the domain is
V
V
V with basis
B
V
=
{
v
1
,
v
2
,
…
,
v
n
}
B_V = \{ v_1, v_2, \dots, v_n \}
B
V​
=
{
v
1​
,
v
2​
,
…
,
v
n​
} and the vector space of the codomain is
W
W
W with basis
B
W
=
{
w
1
,
w
2
,
…
,
w
m
}
B_W = \{ w_1, w_2, \dots, w_m \}
B
W​
=
{
w
1​
,
w
2​
,
…
,
w
m​
}.
- **Act on the Basis Vectors**: For any linear transformation
T
:
V
→
W
T: V \rightarrow W
T
:
V
→
W, apply
T
T
T to each basis vector of
V
V
V. This means we'll find
T
(
v
1
)
,
T
(
v
2
)
,
…
,
T
(
v
n
)
T(v_1), T(v_2), \dots, T(v_n)
T(
v
1​
),
T(
v
2​
),
…
,
T(
v
n​
).
- **Express in Terms of the Codomain Basis**: Each of the transformed vectors, like
T
(
v
i
)
T(v_i)
T(
v
i​
), can be expressed as a linear combination of the basis vectors of
W
W
W. For instance:
T
(
v
1
)
=
a
11
w
1
+
a
21
w
2
+
⋯
+
a
m
1
w
m
T(v_1) = a_{11} w_1 + a_{21} w_2 + \dots + a_{m1} w_m
T(
v
1​
)
=
a
11​
w
1​
+
a
21​
w
2​
+
⋯
+
a
m1​
w
m​

T
(
v
2
)
=
a
12
w
1
+
a
22
w
2
+
⋯
+
a
m
2
w
m
T(v_2) = a_{12} w_1 + a_{22} w_2 + \dots + a_{m2} w_m
T(
v
2​
)
=
a
12​
w
1​
+
a
22​
w
2​
+
⋯
+
a
m2​
w
m​

⋮
\vdots
⋮

- **Construct the Matrix**: Using the coefficients from the above linear combinations, construct the matrix representation
A
A
A of the transformation
T
T
T. The matrix will be
m
×
n
m \times n
m
×
n with columns given by the coefficients corresponding to each
T
(
v
i
)
T(v_i)
T(
v
i​
).

### 2. Matrix Multiplication Corresponds to Composition of Transformations
**Sketch of the Proof**:


- **Two Transformations**: Consider two linear transformations:
U
:
U
→
V
U: U \rightarrow V
U
:
U
→
V and
T
:
V
→
W
T: V \rightarrow W
T
:
V
→
W. Let's say we've already found their matrix representations
A
U
A_U
A
U​
and
A
T
A_T
A
T​
with respect to chosen bases.
- **Composition**: The composition
T
∘
U
T \circ U
T
∘
U means applying
U
U
U first and then
T
T
T.
- **Action on a Vector**: Take any vector
x
x
x in the domain of
U
U
U. When you compute
T
∘
U
(
x
)
T \circ U (x)
T
∘
U(x), you're first mapping
x
x
x using
U
U
U and then taking the result and mapping it with
T
T
T.
- **Matrix Representation of Composition**: Now, using the matrices, this action is equivalent to first multiplying
x
x
x by
A
U
A_U
A
U​
(which gives the vector
U
(
x
)
U(x)
U(x)) and then multiplying the result by
A
T
A_T
A
T​
. This is equivalent to multiplying
x
x
x by the product matrix
A
T
×
A
U
A_T \times A_U
A
T​
×
A
U​
.
- **Equivalence**: Thus, you can show that for any vector
x
x
x:
T
∘
U
(
x
)
T \circ U (x)
T
∘
U(x)
is equivalent to
A
T
×
A
U
×
x
A_T \times A_U \times x
A
T​
×
A
U​
×
x
where
A
T
×
A
U
A_T \times A_U
A
T​
×
A
U​
is the matrix multiplication of
A
T
A_T
A
T​
and
A
U
A_U
A
U​
.

By showing this equivalence for any vector <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>x</mi></mrow><annotation encoding="application/x-tex">x</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.4306em;">x, you demonstrate that matrix multiplication corresponds to the composition of transformations.



------------------

**You:**

how do you prove step 5? by brute force?

------------------

**ChatGPT:**

Step 5 can be proven more systematically than just brute force, though the approach does involve direct computation using the definitions of matrix multiplication and the action of the transformations. Here's a more detailed breakdown:

**Proof of Step 5**:


- **Matrix Representations**:
Let's assume we have matrix representations for the linear maps:
   - U
   :
   U
   →
   V
   U: U \rightarrow V
   U
   :
   U
   →
   V is represented by matrix
   A
   U
   A_U
   A
   U​
   .
   - T
   :
   V
   →
   W
   T: V \rightarrow W
   T
   :
   V
   →
   W is represented by matrix
   A
   T
   A_T
   A
   T​
   .
Let's assume bases for
U
,
V
,
U, V,
U,
V, and
W
W
W are
B
U
,
B
V
,
B_U, B_V,
B
U​
,
B
V​
, and
B
W
B_W
B
W​
respectively.
- **Action on a Vector in the Basis of U**:

Let's take a vector
x
x
x from the domain of
U
U
U. Express
x
x
x in terms of the basis
B
U
B_U
B
U​
:
x
=
∑
i
x
i
u
i
x = \sum_{i} x_i u_i
x
=
∑
i​
x
i​
u
i​
where
u
i
u_i
u
i​
are the basis vectors of
B
U
B_U
B
U​
.
- **Compute U(x)**:

The result of
U
(
x
)
U(x)
U(x) is:
U
(
x
)
=
∑
i
x
i
U
(
u
i
)
U(x) = \sum_{i} x_i U(u_i)
U(x)
=
∑
i​
x
i​
U(u
i​
)

Using the matrix representation
A
U
A_U
A
U​
, the vector
U
(
x
)
U(x)
U(x) in terms of basis
B
V
B_V
B
V​
is
A
U
×
x
A_U \times x
A
U​
×
x.
- **Compute T(U(x))**:

We then apply
T
T
T to the result:
T
(
U
(
x
)
)
=
T
(
∑
i
x
i
U
(
u
i
)
)
=
∑
i
x
i
T
(
U
(
u
i
)
)
T(U(x)) = T(\sum_{i} x_i U(u_i)) = \sum_{i} x_i T(U(u_i))
T(
U(x))
=
T(
∑
i​
x
i​
U(u
i​
))
=
∑
i​
x
i​
T(
U(u
i​
))

Using the matrix representation
A
T
A_T
A
T​
, the vector
T
(
U
(
x
)
)
T(U(x))
T(
U(x)) in terms of basis
B
W
B_W
B
W​
is given by multiplying the vector
A
U
×
x
A_U \times x
A
U​
×
x by the matrix
A
T
A_T
A
T​
. Hence, it's
A
T
×
(
A
U
×
x
)
A_T \times (A_U \times x)
A
T​
×
(A
U​
×
x).
- **Matrix Multiplication**:

By the associative property of matrix multiplication,
A
T
×
(
A
U
×
x
)
A_T \times (A_U \times x)
A
T​
×
(A
U​
×
x) is equivalent to
(
A
T
×
A
U
)
×
x
(A_T \times A_U) \times x
(A
T​
×
A
U​
)
×
x.
- **Conclusion**:

Since
T
∘
U
(
x
)
=
T
(
U
(
x
)
)
T \circ U (x) = T(U(x))
T
∘
U(x)
=
T(
U(x)) and we've shown that this is represented by
(
A
T
×
A
U
)
×
x
(A_T \times A_U) \times x
(A
T​
×
A
U​
)
×
x, it follows that the matrix representation of the composed transformation
T
∘
U
T \circ U
T
∘
U is
A
T
×
A
U
A_T \times A_U
A
T​
×
A
U​
.

While this involves computation, it's structured and based on the properties and definitions of matrix multiplication and the actions of the transformations. It's not just aimless "brute force" but a methodical application of the properties we know.



------------------

**You:**

so, then, critical part is "By the associative property of matrix multiplication" 
how can we prove it ?

------------------

**ChatGPT:**

The associative property of matrix multiplication, which states that for any matrices <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>A</mi><mo separator="true">,</mo><mi>B</mi><mo separator="true">,</mo></mrow><annotation encoding="application/x-tex">A, B,</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.8778em; vertical-align: -0.1944em;">A,<span class="mspace" style="margin-right: 0.1667em;"><span class="mord mathnormal" style="margin-right: 0.05017em;">B, and <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>C</mi></mrow><annotation encoding="application/x-tex">C</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;"><span class="mord mathnormal" style="margin-right: 0.07153em;">C (with appropriate dimensions for multiplication):

<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mo stretchy="false">(</mo><mi>A</mi><mo>×</mo><mi>B</mi><mo stretchy="false">)</mo><mo>×</mo><mi>C</mi><mo>=</mo><mi>A</mi><mo>×</mo><mo stretchy="false">(</mo><mi>B</mi><mo>×</mo><mi>C</mi><mo stretchy="false">)</mo></mrow><annotation encoding="application/x-tex">(A \times B) \times C = A \times (B \times C)</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;">(A<span class="mspace" style="margin-right: 0.2222em;">×<span class="mspace" style="margin-right: 0.2222em;"><span class="strut" style="height: 1em; vertical-align: -0.25em;"><span class="mord mathnormal" style="margin-right: 0.05017em;">B)<span class="mspace" style="margin-right: 0.2222em;">×<span class="mspace" style="margin-right: 0.2222em;"><span class="strut" style="height: 0.6833em;"><span class="mord mathnormal" style="margin-right: 0.07153em;">C<span class="mspace" style="margin-right: 0.2778em;">=<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 0.7667em; vertical-align: -0.0833em;">A<span class="mspace" style="margin-right: 0.2222em;">×<span class="mspace" style="margin-right: 0.2222em;"><span class="strut" style="height: 1em; vertical-align: -0.25em;">(<span class="mord mathnormal" style="margin-right: 0.05017em;">B<span class="mspace" style="margin-right: 0.2222em;">×<span class="mspace" style="margin-right: 0.2222em;"><span class="strut" style="height: 1em; vertical-align: -0.25em;"><span class="mord mathnormal" style="margin-right: 0.07153em;">C)

can be proven using the definition of matrix multiplication.

**Proof**:

Let's break this down step-by-step:


- **Matrix Entries**:

Given matrices <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>A</mi></mrow><annotation encoding="application/x-tex">A</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;">A of size <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>m</mi><mo>×</mo><mi>n</mi></mrow><annotation encoding="application/x-tex">m \times n</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6667em; vertical-align: -0.0833em;">m<span class="mspace" style="margin-right: 0.2222em;">×<span class="mspace" style="margin-right: 0.2222em;"><span class="strut" style="height: 0.4306em;">n, <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>B</mi></mrow><annotation encoding="application/x-tex">B</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;"><span class="mord mathnormal" style="margin-right: 0.05017em;">B of size <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>n</mi><mo>×</mo><mi>p</mi></mrow><annotation encoding="application/x-tex">n \times p</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6667em; vertical-align: -0.0833em;">n<span class="mspace" style="margin-right: 0.2222em;">×<span class="mspace" style="margin-right: 0.2222em;"><span class="strut" style="height: 0.625em; vertical-align: -0.1944em;">p, and <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>C</mi></mrow><annotation encoding="application/x-tex">C</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;"><span class="mord mathnormal" style="margin-right: 0.07153em;">C of size <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>p</mi><mo>×</mo><mi>q</mi></mrow><annotation encoding="application/x-tex">p \times q</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.7778em; vertical-align: -0.1944em;">p<span class="mspace" style="margin-right: 0.2222em;">×<span class="mspace" style="margin-right: 0.2222em;"><span class="strut" style="height: 0.625em; vertical-align: -0.1944em;"><span class="mord mathnormal" style="margin-right: 0.03588em;">q, the entry in the <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi>i</mi><mrow><mi>t</mi><mi>h</mi></mrow></msup></mrow><annotation encoding="application/x-tex">i^{th}</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.8491em;">i<span class="vlist" style="height: 0.8491em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">th row and <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi>j</mi><mrow><mi>t</mi><mi>h</mi></mrow></msup></mrow><annotation encoding="application/x-tex">j^{th}</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1.0435em; vertical-align: -0.1944em;"><span class="mord mathnormal" style="margin-right: 0.05724em;">j<span class="vlist" style="height: 0.8491em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">th column of the product matrix <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>A</mi><mi>B</mi></mrow><annotation encoding="application/x-tex">AB</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;">A<span class="mord mathnormal" style="margin-right: 0.05017em;">B is given by:

<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mo stretchy="false">(</mo><mi>A</mi><mi>B</mi><msub><mo stretchy="false">)</mo><mrow><mi>i</mi><mi>j</mi></mrow></msub><mo>=</mo><msubsup><mo>∑</mo><mrow><mi>k</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></msubsup><msub><mi>A</mi><mrow><mi>i</mi><mi>k</mi></mrow></msub><msub><mi>B</mi><mrow><mi>k</mi><mi>j</mi></mrow></msub></mrow><annotation encoding="application/x-tex">(AB)_{ij} = \sum_{k=1}^{n} A_{ik} B_{kj}</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1.0361em; vertical-align: -0.2861em;">(A<span class="mord mathnormal" style="margin-right: 0.05017em;">B)<span class="vlist" style="height: 0.3117em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">ij​<span class="vlist" style="height: 0.2861em;"><span class="mspace" style="margin-right: 0.2778em;">=<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 1.104em; vertical-align: -0.2997em;"><span class="mop op-symbol small-op" style="position: relative; top: 0em;">∑<span class="vlist" style="height: 0.8043em;"><span style="top: -2.4003em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.03148em;">k=1<span style="top: -3.2029em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n​<span class="vlist" style="height: 0.2997em;"><span class="mspace" style="margin-right: 0.1667em;">A<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.03148em;">ik​<span class="vlist" style="height: 0.15em;"><span class="mord mathnormal" style="margin-right: 0.05017em;">B<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: -0.0502em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">kj​<span class="vlist" style="height: 0.2861em;">

Similarly, the entry in the <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi>j</mi><mrow><mi>t</mi><mi>h</mi></mrow></msup></mrow><annotation encoding="application/x-tex">j^{th}</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1.0435em; vertical-align: -0.1944em;"><span class="mord mathnormal" style="margin-right: 0.05724em;">j<span class="vlist" style="height: 0.8491em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">th row and <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi>l</mi><mrow><mi>t</mi><mi>h</mi></mrow></msup></mrow><annotation encoding="application/x-tex">l^{th}</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.8491em;"><span class="mord mathnormal" style="margin-right: 0.01968em;">l<span class="vlist" style="height: 0.8491em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">th column of the product matrix <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>B</mi><mi>C</mi></mrow><annotation encoding="application/x-tex">BC</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;"><span class="mord mathnormal" style="margin-right: 0.07153em;">BC is:

<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mo stretchy="false">(</mo><mi>B</mi><mi>C</mi><msub><mo stretchy="false">)</mo><mrow><mi>j</mi><mi>l</mi></mrow></msub><mo>=</mo><msubsup><mo>∑</mo><mrow><mi>r</mi><mo>=</mo><mn>1</mn></mrow><mi>p</mi></msubsup><msub><mi>B</mi><mrow><mi>j</mi><mi>r</mi></mrow></msub><msub><mi>C</mi><mrow><mi>r</mi><mi>l</mi></mrow></msub></mrow><annotation encoding="application/x-tex">(BC)_{jl} = \sum_{r=1}^{p} B_{jr} C_{rl}</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1.0361em; vertical-align: -0.2861em;">(<span class="mord mathnormal" style="margin-right: 0.07153em;">BC)<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">j<span class="mord mathnormal mtight" style="margin-right: 0.01968em;">l​<span class="vlist" style="height: 0.2861em;"><span class="mspace" style="margin-right: 0.2778em;">=<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 1.104em; vertical-align: -0.2997em;"><span class="mop op-symbol small-op" style="position: relative; top: 0em;">∑<span class="vlist" style="height: 0.8043em;"><span style="top: -2.4003em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.02778em;">r=1<span style="top: -3.2029em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">p​<span class="vlist" style="height: 0.2997em;"><span class="mspace" style="margin-right: 0.1667em;"><span class="mord mathnormal" style="margin-right: 0.05017em;">B<span class="vlist" style="height: 0.3117em;"><span style="top: -2.55em; margin-left: -0.0502em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">j<span class="mord mathnormal mtight" style="margin-right: 0.02778em;">r​<span class="vlist" style="height: 0.2861em;"><span class="mord mathnormal" style="margin-right: 0.07153em;">C<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: -0.0715em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.02778em;">r<span class="mord mathnormal mtight" style="margin-right: 0.01968em;">l​<span class="vlist" style="height: 0.15em;">


- **Compute
(
A
B
)
C
(AB)C
(A
B)
C**:

The <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi>i</mi><mrow><mi>t</mi><mi>h</mi></mrow></msup></mrow><annotation encoding="application/x-tex">i^{th}</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.8491em;">i<span class="vlist" style="height: 0.8491em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">th row, <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi>l</mi><mrow><mi>t</mi><mi>h</mi></mrow></msup></mrow><annotation encoding="application/x-tex">l^{th}</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.8491em;"><span class="mord mathnormal" style="margin-right: 0.01968em;">l<span class="vlist" style="height: 0.8491em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">th column entry of the matrix product <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mo stretchy="false">(</mo><mi>A</mi><mi>B</mi><mo stretchy="false">)</mo><mi>C</mi></mrow><annotation encoding="application/x-tex">(AB)C</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;">(A<span class="mord mathnormal" style="margin-right: 0.05017em;">B)<span class="mord mathnormal" style="margin-right: 0.07153em;">C is:

<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mo stretchy="false">(</mo><mo stretchy="false">(</mo><mi>A</mi><mi>B</mi><mo stretchy="false">)</mo><mi>C</mi><msub><mo stretchy="false">)</mo><mrow><mi>i</mi><mi>l</mi></mrow></msub><mo>=</mo><msubsup><mo>∑</mo><mrow><mi>j</mi><mo>=</mo><mn>1</mn></mrow><mi>p</mi></msubsup><mo stretchy="false">(</mo><mi>A</mi><mi>B</mi><msub><mo stretchy="false">)</mo><mrow><mi>i</mi><mi>j</mi></mrow></msub><msub><mi>C</mi><mrow><mi>j</mi><mi>l</mi></mrow></msub></mrow><annotation encoding="application/x-tex">((AB)C)_{il} = \sum_{j=1}^{p} (AB)_{ij} C_{jl}</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;">((A<span class="mord mathnormal" style="margin-right: 0.05017em;">B)<span class="mord mathnormal" style="margin-right: 0.07153em;">C)<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">i<span class="mord mathnormal mtight" style="margin-right: 0.01968em;">l​<span class="vlist" style="height: 0.15em;"><span class="mspace" style="margin-right: 0.2778em;">=<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 1.2401em; vertical-align: -0.4358em;"><span class="mop op-symbol small-op" style="position: relative; top: 0em;">∑<span class="vlist" style="height: 0.8043em;"><span style="top: -2.4003em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">j=1<span style="top: -3.2029em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">p​<span class="vlist" style="height: 0.4358em;">(A<span class="mord mathnormal" style="margin-right: 0.05017em;">B)<span class="vlist" style="height: 0.3117em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">ij​<span class="vlist" style="height: 0.2861em;"><span class="mord mathnormal" style="margin-right: 0.07153em;">C<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: -0.0715em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">j<span class="mord mathnormal mtight" style="margin-right: 0.01968em;">l​<span class="vlist" style="height: 0.2861em;">
<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mo>=</mo><msubsup><mo>∑</mo><mrow><mi>j</mi><mo>=</mo><mn>1</mn></mrow><mi>p</mi></msubsup><mrow><mo fence="true">(</mo><msubsup><mo>∑</mo><mrow><mi>k</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></msubsup><msub><mi>A</mi><mrow><mi>i</mi><mi>k</mi></mrow></msub><msub><mi>B</mi><mrow><mi>k</mi><mi>j</mi></mrow></msub><mo fence="true">)</mo></mrow><msub><mi>C</mi><mrow><mi>j</mi><mi>l</mi></mrow></msub></mrow><annotation encoding="application/x-tex">= \sum_{j=1}^{p} \left( \sum_{k=1}^{n} A_{ik} B_{kj} \right) C_{jl}</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.3669em;">=<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 1.2401em; vertical-align: -0.4358em;"><span class="mop op-symbol small-op" style="position: relative; top: 0em;">∑<span class="vlist" style="height: 0.8043em;"><span style="top: -2.4003em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">j=1<span style="top: -3.2029em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">p​<span class="vlist" style="height: 0.4358em;"><span class="mspace" style="margin-right: 0.1667em;"><span class="mopen delimcenter" style="top: 0em;">(<span class="mop op-symbol small-op" style="position: relative; top: 0em;">∑<span class="vlist" style="height: 0.8043em;"><span style="top: -2.4003em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.03148em;">k=1<span style="top: -3.2029em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n​<span class="vlist" style="height: 0.2997em;"><span class="mspace" style="margin-right: 0.1667em;">A<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.03148em;">ik​<span class="vlist" style="height: 0.15em;"><span class="mord mathnormal" style="margin-right: 0.05017em;">B<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: -0.0502em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">kj​<span class="vlist" style="height: 0.2861em;"><span class="mclose delimcenter" style="top: 0em;">)<span class="mspace" style="margin-right: 0.1667em;"><span class="mord mathnormal" style="margin-right: 0.07153em;">C<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: -0.0715em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">j<span class="mord mathnormal mtight" style="margin-right: 0.01968em;">l​<span class="vlist" style="height: 0.2861em;">


- **Compute
A
(
B
C
)
A(BC)
A(
BC)**:

The <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi>i</mi><mrow><mi>t</mi><mi>h</mi></mrow></msup></mrow><annotation encoding="application/x-tex">i^{th}</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.8491em;">i<span class="vlist" style="height: 0.8491em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">th row, <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi>l</mi><mrow><mi>t</mi><mi>h</mi></mrow></msup></mrow><annotation encoding="application/x-tex">l^{th}</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.8491em;"><span class="mord mathnormal" style="margin-right: 0.01968em;">l<span class="vlist" style="height: 0.8491em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">th column entry of the matrix product <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>A</mi><mo stretchy="false">(</mo><mi>B</mi><mi>C</mi><mo stretchy="false">)</mo></mrow><annotation encoding="application/x-tex">A(BC)</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;">A(<span class="mord mathnormal" style="margin-right: 0.07153em;">BC) is:

<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mo stretchy="false">(</mo><mi>A</mi><mo stretchy="false">(</mo><mi>B</mi><mi>C</mi><mo stretchy="false">)</mo><msub><mo stretchy="false">)</mo><mrow><mi>i</mi><mi>l</mi></mrow></msub><mo>=</mo><msubsup><mo>∑</mo><mrow><mi>k</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></msubsup><msub><mi>A</mi><mrow><mi>i</mi><mi>k</mi></mrow></msub><mo stretchy="false">(</mo><mi>B</mi><mi>C</mi><msub><mo stretchy="false">)</mo><mrow><mi>k</mi><mi>l</mi></mrow></msub></mrow><annotation encoding="application/x-tex">(A(BC))_{il} = \sum_{k=1}^{n} A_{ik} (BC)_{kl}</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;">(A(<span class="mord mathnormal" style="margin-right: 0.07153em;">BC))<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">i<span class="mord mathnormal mtight" style="margin-right: 0.01968em;">l​<span class="vlist" style="height: 0.15em;"><span class="mspace" style="margin-right: 0.2778em;">=<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 1.104em; vertical-align: -0.2997em;"><span class="mop op-symbol small-op" style="position: relative; top: 0em;">∑<span class="vlist" style="height: 0.8043em;"><span style="top: -2.4003em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.03148em;">k=1<span style="top: -3.2029em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n​<span class="vlist" style="height: 0.2997em;"><span class="mspace" style="margin-right: 0.1667em;">A<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.03148em;">ik​<span class="vlist" style="height: 0.15em;">(<span class="mord mathnormal" style="margin-right: 0.07153em;">BC)<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.03148em;">k<span class="mord mathnormal mtight" style="margin-right: 0.01968em;">l​<span class="vlist" style="height: 0.15em;">
<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mo>=</mo><msubsup><mo>∑</mo><mrow><mi>k</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></msubsup><msub><mi>A</mi><mrow><mi>i</mi><mi>k</mi></mrow></msub><mrow><mo fence="true">(</mo><msubsup><mo>∑</mo><mrow><mi>j</mi><mo>=</mo><mn>1</mn></mrow><mi>p</mi></msubsup><msub><mi>B</mi><mrow><mi>k</mi><mi>j</mi></mrow></msub><msub><mi>C</mi><mrow><mi>j</mi><mi>l</mi></mrow></msub><mo fence="true">)</mo></mrow></mrow><annotation encoding="application/x-tex">= \sum_{k=1}^{n} A_{ik} \left( \sum_{j=1}^{p} B_{kj} C_{jl} \right)</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.3669em;">=<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 1.8em; vertical-align: -0.65em;"><span class="mop op-symbol small-op" style="position: relative; top: 0em;">∑<span class="vlist" style="height: 0.8043em;"><span style="top: -2.4003em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.03148em;">k=1<span style="top: -3.2029em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n​<span class="vlist" style="height: 0.2997em;"><span class="mspace" style="margin-right: 0.1667em;">A<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.03148em;">ik​<span class="vlist" style="height: 0.15em;"><span class="mspace" style="margin-right: 0.1667em;"><span class="mopen delimcenter" style="top: 0em;">(<span class="mop op-symbol small-op" style="position: relative; top: 0em;">∑<span class="vlist" style="height: 0.8043em;"><span style="top: -2.4003em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">j=1<span style="top: -3.2029em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">p​<span class="vlist" style="height: 0.4358em;"><span class="mspace" style="margin-right: 0.1667em;"><span class="mord mathnormal" style="margin-right: 0.05017em;">B<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: -0.0502em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">kj​<span class="vlist" style="height: 0.2861em;"><span class="mord mathnormal" style="margin-right: 0.07153em;">C<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: -0.0715em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">j<span class="mord mathnormal mtight" style="margin-right: 0.01968em;">l​<span class="vlist" style="height: 0.2861em;"><span class="mclose delimcenter" style="top: 0em;">)


- **Equality of Entries**:

By rearranging the order of summation and using the properties of sums, you can show that:

<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msubsup><mo>∑</mo><mrow><mi>j</mi><mo>=</mo><mn>1</mn></mrow><mi>p</mi></msubsup><mrow><mo fence="true">(</mo><msubsup><mo>∑</mo><mrow><mi>k</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></msubsup><msub><mi>A</mi><mrow><mi>i</mi><mi>k</mi></mrow></msub><msub><mi>B</mi><mrow><mi>k</mi><mi>j</mi></mrow></msub><mo fence="true">)</mo></mrow><msub><mi>C</mi><mrow><mi>j</mi><mi>l</mi></mrow></msub><mo>=</mo><msubsup><mo>∑</mo><mrow><mi>k</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></msubsup><msub><mi>A</mi><mrow><mi>i</mi><mi>k</mi></mrow></msub><mrow><mo fence="true">(</mo><msubsup><mo>∑</mo><mrow><mi>j</mi><mo>=</mo><mn>1</mn></mrow><mi>p</mi></msubsup><msub><mi>B</mi><mrow><mi>k</mi><mi>j</mi></mrow></msub><msub><mi>C</mi><mrow><mi>j</mi><mi>l</mi></mrow></msub><mo fence="true">)</mo></mrow></mrow><annotation encoding="application/x-tex">\sum_{j=1}^{p} \left( \sum_{k=1}^{n} A_{ik} B_{kj} \right) C_{jl} = \sum_{k=1}^{n} A_{ik} \left( \sum_{j=1}^{p} B_{kj} C_{jl} \right)</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1.2401em; vertical-align: -0.4358em;"><span class="mop op-symbol small-op" style="position: relative; top: 0em;">∑<span class="vlist" style="height: 0.8043em;"><span style="top: -2.4003em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">j=1<span style="top: -3.2029em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">p​<span class="vlist" style="height: 0.4358em;"><span class="mspace" style="margin-right: 0.1667em;"><span class="mopen delimcenter" style="top: 0em;">(<span class="mop op-symbol small-op" style="position: relative; top: 0em;">∑<span class="vlist" style="height: 0.8043em;"><span style="top: -2.4003em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.03148em;">k=1<span style="top: -3.2029em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n​<span class="vlist" style="height: 0.2997em;"><span class="mspace" style="margin-right: 0.1667em;">A<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.03148em;">ik​<span class="vlist" style="height: 0.15em;"><span class="mord mathnormal" style="margin-right: 0.05017em;">B<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: -0.0502em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">kj​<span class="vlist" style="height: 0.2861em;"><span class="mclose delimcenter" style="top: 0em;">)<span class="mspace" style="margin-right: 0.1667em;"><span class="mord mathnormal" style="margin-right: 0.07153em;">C<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: -0.0715em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">j<span class="mord mathnormal mtight" style="margin-right: 0.01968em;">l​<span class="vlist" style="height: 0.2861em;"><span class="mspace" style="margin-right: 0.2778em;">=<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 1.8em; vertical-align: -0.65em;"><span class="mop op-symbol small-op" style="position: relative; top: 0em;">∑<span class="vlist" style="height: 0.8043em;"><span style="top: -2.4003em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.03148em;">k=1<span style="top: -3.2029em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n​<span class="vlist" style="height: 0.2997em;"><span class="mspace" style="margin-right: 0.1667em;">A<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.03148em;">ik​<span class="vlist" style="height: 0.15em;"><span class="mspace" style="margin-right: 0.1667em;"><span class="mopen delimcenter" style="top: 0em;">(<span class="mop op-symbol small-op" style="position: relative; top: 0em;">∑<span class="vlist" style="height: 0.8043em;"><span style="top: -2.4003em; margin-left: 0em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">j=1<span style="top: -3.2029em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">p​<span class="vlist" style="height: 0.4358em;"><span class="mspace" style="margin-right: 0.1667em;"><span class="mord mathnormal" style="margin-right: 0.05017em;">B<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: -0.0502em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">kj​<span class="vlist" style="height: 0.2861em;"><span class="mord mathnormal" style="margin-right: 0.07153em;">C<span class="vlist" style="height: 0.3361em;"><span style="top: -2.55em; margin-left: -0.0715em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.05724em;">j<span class="mord mathnormal mtight" style="margin-right: 0.01968em;">l​<span class="vlist" style="height: 0.2861em;"><span class="mclose delimcenter" style="top: 0em;">)

This shows that the entries of the matrices <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mo stretchy="false">(</mo><mi>A</mi><mi>B</mi><mo stretchy="false">)</mo><mi>C</mi></mrow><annotation encoding="application/x-tex">(AB)C</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;">(A<span class="mord mathnormal" style="margin-right: 0.05017em;">B)<span class="mord mathnormal" style="margin-right: 0.07153em;">C and <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>A</mi><mo stretchy="false">(</mo><mi>B</mi><mi>C</mi><mo stretchy="false">)</mo></mrow><annotation encoding="application/x-tex">A(BC)</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;">A(<span class="mord mathnormal" style="margin-right: 0.07153em;">BC) are equal for all <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>i</mi></mrow><annotation encoding="application/x-tex">i</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6595em;">i and <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>l</mi></mrow><annotation encoding="application/x-tex">l</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6944em;"><span class="mord mathnormal" style="margin-right: 0.01968em;">l.


- **Conclusion**:

Since the entries of <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mo stretchy="false">(</mo><mi>A</mi><mi>B</mi><mo stretchy="false">)</mo><mi>C</mi></mrow><annotation encoding="application/x-tex">(AB)C</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;">(A<span class="mord mathnormal" style="margin-right: 0.05017em;">B)<span class="mord mathnormal" style="margin-right: 0.07153em;">C and <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>A</mi><mo stretchy="false">(</mo><mi>B</mi><mi>C</mi><mo stretchy="false">)</mo></mrow><annotation encoding="application/x-tex">A(BC)</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;">A(<span class="mord mathnormal" style="margin-right: 0.07153em;">BC) are equal for all rows and columns, it follows that the matrices themselves are equal, and matrix multiplication is associative:

<math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mo stretchy="false">(</mo><mi>A</mi><mo>×</mo><mi>B</mi><mo stretchy="false">)</mo><mo>×</mo><mi>C</mi><mo>=</mo><mi>A</mi><mo>×</mo><mo stretchy="false">(</mo><mi>B</mi><mo>×</mo><mi>C</mi><mo stretchy="false">)</mo></mrow><annotation encoding="application/x-tex">(A \times B) \times C = A \times (B \times C)</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 1em; vertical-align: -0.25em;">(A<span class="mspace" style="margin-right: 0.2222em;">×<span class="mspace" style="margin-right: 0.2222em;"><span class="strut" style="height: 1em; vertical-align: -0.25em;"><span class="mord mathnormal" style="margin-right: 0.05017em;">B)<span class="mspace" style="margin-right: 0.2222em;">×<span class="mspace" style="margin-right: 0.2222em;"><span class="strut" style="height: 0.6833em;"><span class="mord mathnormal" style="margin-right: 0.07153em;">C<span class="mspace" style="margin-right: 0.2778em;">=<span class="mspace" style="margin-right: 0.2778em;"><span class="strut" style="height: 0.7667em; vertical-align: -0.0833em;">A<span class="mspace" style="margin-right: 0.2222em;">×<span class="mspace" style="margin-right: 0.2222em;"><span class="strut" style="height: 1em; vertical-align: -0.25em;">(<span class="mord mathnormal" style="margin-right: 0.05017em;">B<span class="mspace" style="margin-right: 0.2222em;">×<span class="mspace" style="margin-right: 0.2222em;"><span class="strut" style="height: 1em; vertical-align: -0.25em;"><span class="mord mathnormal" style="margin-right: 0.07153em;">C)

This proof essentially breaks down matrix multiplication into its individual components and demonstrates that the associative property holds true based on the definitions and properties of matrix entries and summation.



------------------

**You:**

Any Linear Map Can Be Represented as a Matrix:

so when we say matrix represent linear map, when we construct matrix, we need to choose basis for both vector spaces, and matrix represent how any v (represented as linear combination of Bv) maps to w in W and the resulting w (of matrix multiplication on v) is the coefficient vector of Bw

------------------

**ChatGPT:**

Exactly! Your understanding is spot on. Let's break it down for clarity:


- **Basis Selection**:
   - Let
   V
   V
   V be the domain of the linear transformation with basis
   B
   V
   =
   {
   v
   1
   ,
   v
   2
   ,
   …
   ,
   v
   n
   }
   B_V = \{ v_1, v_2, \dots, v_n \}
   B
   V​
   =
   {
   v
   1​
   ,
   v
   2​
   ,
   …
   ,
   v
   n​
   }.
   - Let
   W
   W
   W be the codomain of the linear transformation with basis
   B
   W
   =
   {
   w
   1
   ,
   w
   2
   ,
   …
   ,
   w
   m
   }
   B_W = \{ w_1, w_2, \dots, w_m \}
   B
   W​
   =
   {
   w
   1​
   ,
   w
   2​
   ,
   …
   ,
   w
   m​
   }.
- **Matrix Construction**:
   - For each vector
   v
   i
   v_i
   v
   i​
   in the basis
   B
   V
   B_V
   B
   V​
   , apply the linear transformation to obtain
   T
   (
   v
   i
   )
   T(v_i)
   T(
   v
   i​
   ).
   - Express
   T
   (
   v
   i
   )
   T(v_i)
   T(
   v
   i​
   ) as a linear combination of the basis vectors in
   B
   W
   B_W
   B
   W​
   :
   T
   (
   v
   i
   )
   =
   a
   1
   i
   w
   1
   +
   a
   2
   i
   w
   2
   +
   ⋯
   +
   a
   m
   i
   w
   m
   T(v_i) = a_{1i} w_1 + a_{2i} w_2 + \dots + a_{mi} w_m
   T(
   v
   i​
   )
   =
   a
   1i​
   w
   1​
   +
   a
   2i​
   w
   2​
   +
   ⋯
   +
   a
   mi​
   w
   m​
   - The coefficients
   a
   1
   i
   ,
   a
   2
   i
   ,
   …
   ,
   a
   m
   i
   a_{1i}, a_{2i}, \dots, a_{mi}
   a
   1i​
   ,
   a
   2i​
   ,
   …
   ,
   a
   mi​
   form the
   i
   t
   h
   i^{th}
   i
   th column of the matrix representation of
   T
   T
   T.
- **Representation of a Vector**:
   - Any vector
   v
   v
   v in
   V
   V
   V can be expressed as a linear combination of the basis vectors in
   B
   V
   B_V
   B
   V​
   .
   - When you multiply the matrix of
   T
   T
   T by the coordinate/column vector of
   v
   v
   v with respect to
   B
   V
   B_V
   B
   V​
   , you get the coordinate/column vector of
   T
   (
   v
   )
   T(v)
   T(
   v) with respect to
   B
   W
   B_W
   B
   W​
   . This resulting vector is essentially the coefficients with which
   T
   (
   v
   )
   T(v)
   T(
   v) is expressed in terms of the basis
   B
   W
   B_W
   B
   W​
   .

So, the matrix representation of a linear map is a way to capture the action of that map on a vector space with respect to chosen bases. Given a vector in <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>V</mi></mrow><annotation encoding="application/x-tex">V</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;"><span class="mord mathnormal" style="margin-right: 0.22222em;">V (expressed in terms of <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msub><mi>B</mi><mi>V</mi></msub></mrow><annotation encoding="application/x-tex">B_V</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.8333em; vertical-align: -0.15em;"><span class="mord mathnormal" style="margin-right: 0.05017em;">B<span class="vlist" style="height: 0.3283em;"><span style="top: -2.55em; margin-left: -0.0502em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.22222em;">V​<span class="vlist" style="height: 0.15em;">), the matrix tells you how that vector is transformed into <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>W</mi></mrow><annotation encoding="application/x-tex">W</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6833em;"><span class="mord mathnormal" style="margin-right: 0.13889em;">W (expressed in terms of <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msub><mi>B</mi><mi>W</mi></msub></mrow><annotation encoding="application/x-tex">B_W</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.8333em; vertical-align: -0.15em;"><span class="mord mathnormal" style="margin-right: 0.05017em;">B<span class="vlist" style="height: 0.3283em;"><span style="top: -2.55em; margin-left: -0.0502em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;"><span class="mord mathnormal mtight" style="margin-right: 0.13889em;">W​<span class="vlist" style="height: 0.15em;">). The matrix serves as a bridge between these two representations.



------------------

**You:**

then it's rather abstract question, 
we are assuming there's a basis vector representation of any vector space, 
but how do we know if it's true

(because if we can't construct basis vector, we can't construct the matrix for the linear map)

for analogy, for "set", assuming any set can be constructed (meaningful) resulted in russel paradox, 

how do we know if basis vector representation is always possible? (it's not same as Existence of basis vector of finite dimension)

------------------

**ChatGPT:**

The statement that every vector space has a basis is a fundamental result in linear algebra, known as the **Basis Theorem**. The existence of a basis for any vector space is foundational, but you're right to point out that it's not trivial, especially when we move beyond finite-dimensional spaces.

The proof that every vector space has a basis uses the **Axiom of Choice** (or some variant of it, like Zorn's Lemma). The Axiom of Choice is one of the controversial (though widely accepted) axioms in set theory, in part because it leads to some non-intuitive results. Here's a sketch of how it works:

**Proof Sketch Using Zorn's Lemma**:


- Consider the set of all linearly independent subsets of a vector space
V
V
V. Partially order this set by inclusion.
- Take a chain (a totally ordered subset) in this set. This chain is a collection of linearly independent subsets of
V
V
V. Their union will also be a linearly independent set.
- By Zorn's Lemma, there exists a maximal element in this set, i.e., a maximal linearly independent subset of
V
V
V.
- This maximal linearly independent subset is a basis for
V
V
V. If it weren't, there'd be a vector in
V
V
V outside this set that's not a linear combination of the vectors in the set. But adding this vector to our subset would give a larger linearly independent set, contradicting the maximality of our chosen set.

The critical step here is Zorn's Lemma, which is equivalent to the Axiom of Choice.

However, you're absolutely right that the infinite case isn't as straightforward as the finite-dimensional case. For finite-dimensional vector spaces, the existence of a basis is more elementary and doesn't require the Axiom of Choice.

Lastly, while the Axiom of Choice can lead to non-intuitive results (like the Banach-Tarski paradox in measure theory), it doesn't result in outright contradictions like Russell's Paradox. That said, its use in proofs often signals that we're venturing into deeper and potentially more abstract territory.



------------------

**You:**

oh i'm not asking finite vs infinite,
i'm not asking if basis exists for finite or for inifinite

i'm focusing on finite vector space, and I know we can prove existence of basis in finite vector space,

i'm asking , "existence is not equal to constructing it", if we want to say every linear map is represented by matrix,
(and in the proof, we assumed that there's basis vector for both vector spaces, 
I'm thinking the proof did require more than just existence, it assumes basis vector can be represented (or constructed), because only then we can workon creating matrix representation. 

I think it's similar to set case, where we assume something (any set we can declare) exists is not always constructable, and it lead to the russel paradox,

so i was wondering, assuming this "basis" thing "can be constructed" might be not well founded as "set" case.

------------------

**ChatGPT:**

Ah, I see where you're coming from now. You're touching on a deep topic in the philosophy of mathematics: the difference between **existence** proofs and **constructive** proofs.

You're correct that many classical existence proofs, including the existence of a basis for a vector space (even finite-dimensional ones) using the Axiom of Choice, are non-constructive. They prove that something exists without necessarily giving a method to find or construct it.

For finite-dimensional vector spaces over the real numbers (or any field, really), we do have both existence and constructibility. Given a spanning set for a finite-dimensional vector space, we can use the Gram-Schmidt process, for instance, to construct an orthonormal basis. So, for finite-dimensional spaces, the bases are both provably existent and constructible.

However, as you correctly note, merely proving existence doesn't give us a way to explicitly construct or represent the thing in question. This difference between existence and constructibility is a recurring theme in many areas of mathematics.

In the context of linear algebra, for practical applications involving finite-dimensional vector spaces (like most of the ones in engineering, physics, computer science, etc.), the bases we work with are both existent and constructible. The "constructibility" concern is more pressing when we step into more abstract realms or specific mathematical scenarios where we leverage the full power of axiomatic systems like ZFC (Zermelo–Fraenkel set theory with the Axiom of Choice).

To draw a parallel to the set-theoretic concerns you mentioned: Yes, the Axiom of Choice has led to some "strange" results (like the Banach-Tarski Paradox), but it hasn't led to outright contradictions like Russell's Paradox did for naive set theory. The modern ZFC axiomatic system for set theory has been built in a way to avoid these contradictions.

In summary, for the practical applications of linear algebra in finite-dimensional spaces, the bases are both existent and constructible. Your concerns become more significant in more abstract mathematical settings or when considering the philosophical foundations of mathematics.



------------------

**You:**

ya, but I'm not asking the difference between constructive vs existence in general,
i was asking 
Do you see the hidden assumption (our proof used the construction as given), as I see in the proof, (because it assumes the existence of concrete basis for both vector spaces) 
And i think it's different from assuming existence of basis.

------------------

**ChatGPT:**

I see your point better now. The distinction you're highlighting is indeed nuanced and important.

When we say that every linear transformation between finite-dimensional vector spaces can be represented by a matrix, we're implicitly making a stronger claim than just the existence of a basis for each space. We're assuming:


- There exists a basis for each space (which we can prove).
- We have chosen or can choose (i.e., construct or specify) a particular basis for each space to define the matrix representation.

The matrix representation of a linear transformation is tied to specific bases for the domain and codomain. The act of constructing the matrix requires us to know these bases so that we can compute how each basis vector of the domain is mapped to a linear combination of the basis vectors of the codomain.

In practice, when working with finite-dimensional vector spaces, especially in applied contexts, the bases are often either given explicitly or are implicitly understood (e.g., the standard basis for <math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mi mathvariant="double-struck">R</mi><mi>n</mi></msup></mrow><annotation encoding="application/x-tex">\mathbb{R}^n</annotation></semantics></math><span class="katex-html" aria-hidden="true"><span class="strut" style="height: 0.6889em;">R<span class="vlist" style="height: 0.6644em;"><span style="top: -3.063em; margin-right: 0.05em;"><span class="pstrut" style="height: 2.7em;">n). However, from a foundational standpoint, you're right that our matrix representation proofs rely on the stronger assumption that we can explicitly construct or choose particular bases, not just that bases exist in the abstract.

In essence, the matrix representation of a linear transformation doesn't just depend on the abstract existence of bases but on our ability to specify particular bases for the domain and codomain. Your observation underscores the point that when moving from abstract existence proofs to more concrete representations and computations, additional assumptions or specifications are often needed.



------------------

