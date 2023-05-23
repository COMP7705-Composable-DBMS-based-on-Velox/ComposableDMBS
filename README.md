# ComposableDMBS

## Calcite

References:

https://www.youtube.com/watch?v=meI0W12f_nw

https://github.com/zabetak/calcite-tutorial

https://liebing.org.cn/collections/calcite/

https://frankma.me/posts/papers/apache-calcite/

Refactor calcite part in [calcite-tpch](./calcite-tpch.zip)

Sql and Physical Plans are in [query_plan](./query_plan)

## Velox

### Jsoncpp

```bash
brew install jsoncpp
```

Add following content in velox/velox/exec/tests/CMakeLists.txt

```
INCLUDE_DIRECTORIES(/usr/local/Cellar/jsoncpp/1.9.5/include)
LINK_DIRECTORIES(/usr/local/Cellar/jsoncpp/1.9.5/lib)
file(GLOB LIBRARIES "/usr/local/Cellar/jsoncpp/1.9.5/lib/*.dylib")
message("LIBRARIES = ${LIBRARIES}")

TARGET_LINK_LIBRARIES(velox_in_10_min_demo ${LIBRARIES})
```

Then can #include "json/..."

后续libhdfs3也可以试试这种方式链接静态库

