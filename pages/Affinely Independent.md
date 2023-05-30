- The set $$\{v_1, \cdots, v_n\}$$ is **linearly independent** for any $$c_1, \cdots, c_n$$ not all $$0$$
	- $$\sum_{i=1}^nc_iv_i = 0\iff \forall i\in[n], c_i = 0$$
- It is called **affinely independent** if they are linearly independent and also
	- $$\sum_{i=1}^nc_i = 1$$
- <img src="https://mermaid.ink/img/IGdhbnR0CiAgICB0aXRsZSBBIEdhbnR0IERpYWdyYW0KICAgIGRhdGVGb3JtYXQgIFlZWVktTU0tREQKICAgIHNlY3Rpb24gU2VjdGlvbgogICAgQSB0YXNrICAgICAgICAgICA6YTEsIDIwMTQtMDEtMDEsIDMwZAogICAgQW5vdGhlciB0YXNrICAgICA6YWZ0ZXIgYTEgICwgMjBkCiAgICBzZWN0aW9uIEFub3RoZXIKICAgIFRhc2sgaW4gc2VjICAgICAgOjIwMTQtMDEtMTIgICwgMTJkCiAgICBhbm90aGVyIHRhc2sgICAgICA6IDI0ZAo" />
  {{renderer :mermaid_fbzrdgnz}}
	- ```mermaid
	  gantt
	      title A Gantt Diagram
	      dateFormat  YYYY-MM-DD
	      section Section
	      A task           :a1, 2014-01-01, 30d
	      Another task     :after a1  , 20d
	      section Another
	      Task in sec      :2014-01-12  , 12d
	      another task      : 24d
	  ```