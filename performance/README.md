# Performance Optimization

CPython Extensions
- Ising model simulation is my favorite showcase for this: https://jakevdp.github.io/blog/2017/12/11/live-coding-cython-ising-model/
- rule of thumb: profile first, optimize later (also item 70 in "Effective Python" by Brett Slatkin)
- only worth it for tight loops with numeric computation

C++ Bindings
- pybind11 is my go-to for wrapping C++ code: https://pybind11.readthedocs.io/
- useful when you need existing C++ libraries or extreme performance

General tips:
- numpy vectorization (good old basic)
- numba JIT compilation is the sweet spot between effort and speedup
- profile with `line_profiler`