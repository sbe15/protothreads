# protothreads
Fork of Adam Dunkels Protothreads (https://dunkels.com/adam/pt/) with some functional updates.

## 1.4.1
* lc-switch.h: Use `__COUNTER__` instead of `__LINE__`.
  
  This allows you to group multiple PT statements into a single macro,
  which would previously fail as multiple `LC_SET` would occur on the
  same line, thus creating duplicate case labels.

* pt.h: Mark `PT_YIELD_FLAG` as potentially unused in PT_BEGIN.
  
  It seems that recent compilers report `PT_YIELD_FLAG` as 
  'set, but not used' if no PT_YIELD (or variants) are used.
