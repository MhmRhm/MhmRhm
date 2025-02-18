```cpp
namespace life {
bool terminated = false;
template <typename Func, typename... Args>
  requires requires(Func func, Args &&...args) {
    { func(std::forward<Args>(args)...) } -> std::totally_ordered;
  }
void ageing(Func new_way, Args &&...args) {
  extern Func my_way;
  while (!terminated) {
    if (new_way(std::forward<Args>(args)...) >
        my_way(std::forward<Args>(args)...)) {
      my_way = new_way;
    }
  }
}
} // namespace life

/**
 * For tutorial visit:
 * https://mhmrhm.github.io/tutorials/
 * 
 * To connect visit:
 * https://www.linkedin.com/in/mhmrhm/
 */
```
