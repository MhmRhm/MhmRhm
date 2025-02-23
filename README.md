```cpp
namespace life {                                                   // For tutorials visit:
bool terminated = false;                                           // https://mhmrhm.github.io/tutorials/
template <typename Func, typename... Args>                         //
  requires requires(Func func, Args &&...args) {                   // For the cheatsheet see:
    { func(std::forward<Args>(args)...) } -> std::totally_ordered; // https://github.com/MhmRhm/DotBashHistory
  }                                                                //
void ageing(Func new_way, Args &&...args) {                        // To connect with me:
  extern Func my_way;                                              // https://www.linkedin.com/in/mhmrhm/
  while (!terminated) {                                            //
    if (my_way(args...) < new_way(args...)) {                      // To message me:
      my_way = new_way;                                            // https://t.me/rahimi_mhmmd
    }                                                              //
  }                                                                // I'm Mohammad, a C/C++ developer from Iran,
}                                                                  // currently based in Kuala Lumpur. I enjoy
} // namespace life                                                // programming and playing pool.
```
