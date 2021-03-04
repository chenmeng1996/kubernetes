## 项目结构
```text
├── api
│   ├── apitesting
│   │   ├── codec.go
│   │   ├── fuzzer
│   │   │   ├── fuzzer.go
│   │   │   ├── valuefuzz.go
│   │   │   └── valuefuzz_test.go
│   │   ├── naming
│   │   │   └── naming.go
│   │   └── roundtrip
│   │       ├── compatibility.go
│   │       └── roundtrip.go
│   ├── equality
│   │   └── semantic.go
│   ├── errors
│   │   ├── OWNERS
│   │   ├── doc.go
│   │   ├── errors.go
│   │   └── errors_test.go
│   ├── meta
│   │   ├── OWNERS
│   │   ├── conditions.go
│   │   ├── conditions_test.go
│   │   ├── doc.go
│   │   ├── errors.go
│   │   ├── firsthit_restmapper.go
│   │   ├── help.go
│   │   ├── interfaces.go
│   │   ├── lazy.go
│   │   ├── meta.go
│   │   ├── meta_test.go
│   │   ├── multirestmapper.go
│   │   ├── multirestmapper_test.go
│   │   ├── priority.go
│   │   ├── priority_test.go
│   │   ├── restmapper.go
│   │   ├── restmapper_test.go
│   │   ├── table
│   │   │   └── table.go
│   │   └── testrestmapper
│   │       └── test_restmapper.go
│   ├── resource 提供Quantity表示资源量
│   │   ├── ...
│   └── validation
│       ├── doc.go
│       ├── generic.go
│       ├── objectmeta.go
│       ├── objectmeta_test.go
│       └── path
│           ├── name.go
│           └── name_test.go
├── apis
│   ├── meta
│   │   ├── fuzzer
│   │   │   └── fuzzer.go
│   │   ├── internalversion
│   │   │   ├── doc.go
│   │   │   ├── register.go
│   │   │   ├── scheme
│   │   │   │   ├── doc.go
│   │   │   │   ├── register.go
│   │   │   │   ├── register_test.go
│   │   │   │   └── roundtrip_test.go
│   │   │   ├── types.go
│   │   │   ├── validation
│   │   │   │   ├── validation.go
│   │   │   │   └── validation_test.go
│   │   │   ├── zz_generated.conversion.go
│   │   │   └── zz_generated.deepcopy.go
│   │   ├── v1
│   │   │   ├── controller_ref.go
│   │   │   ├── controller_ref_test.go
│   │   │   ├── conversion.go
│   │   │   ├── conversion_test.go
│   │   │   ├── deepcopy.go
│   │   │   ├── doc.go
│   │   │   ├── duration.go
│   │   │   ├── duration_test.go
│   │   │   ├── generated.pb.go
│   │   │   ├── generated.proto
│   │   │   ├── group_version.go
│   │   │   ├── group_version_test.go
│   │   │   ├── helpers.go
│   │   │   ├── helpers_test.go
│   │   │   ├── labels.go
│   │   │   ├── labels_test.go
│   │   │   ├── meta.go
│   │   │   ├── micro_time.go
│   │   │   ├── micro_time_fuzz.go
│   │   │   ├── micro_time_proto.go
│   │   │   ├── micro_time_test.go
│   │   │   ├── options_test.go
│   │   │   ├── register.go
│   │   │   ├── time.go
│   │   │   ├── time_fuzz.go
│   │   │   ├── time_proto.go
│   │   │   ├── time_test.go
│   │   │   ├── types.go
│   │   │   ├── types_swagger_doc_generated.go
│   │   │   ├── types_test.go
│   │   │   ├── unstructured
│   │   │   │   ├── helpers.go
│   │   │   │   ├── helpers_test.go
│   │   │   │   ├── unstructured.go
│   │   │   │   ├── unstructured_conversion_test.go
│   │   │   │   ├── unstructured_list.go
│   │   │   │   ├── unstructured_list_test.go
│   │   │   │   ├── unstructured_test.go
│   │   │   │   ├── unstructuredscheme
│   │   │   │   │   └── scheme.go
│   │   │   │   └── zz_generated.deepcopy.go
│   │   │   ├── validation
│   │   │   │   ├── validation.go
│   │   │   │   └── validation_test.go
│   │   │   ├── watch.go
│   │   │   ├── zz_generated.conversion.go
│   │   │   ├── zz_generated.deepcopy.go
│   │   │   └── zz_generated.defaults.go
│   │   └── v1beta1
│   │       ├── conversion.go
│   │       ├── deepcopy.go
│   │       ├── doc.go
│   │       ├── generated.pb.go
│   │       ├── generated.proto
│   │       ├── register.go
│   │       ├── types.go
│   │       ├── types_swagger_doc_generated.go
│   │       ├── validation
│   │       │   └── validation.go
│   │       ├── zz_generated.deepcopy.go
│   │       └── zz_generated.defaults.go
│   └── testapigroup
│       ├── doc.go
│       ├── fuzzer
│       │   └── fuzzer.go
│       ├── install
│       │   ├── install.go
│       │   └── roundtrip_test.go
│       ├── register.go
│       ├── types.go
│       ├── v1
│       │   ├── conversion.go
│       │   ├── defaults.go
│       │   ├── doc.go
│       │   ├── generated.pb.go
│       │   ├── generated.proto
│       │   ├── register.go
│       │   ├── types.go
│       │   ├── zz_generated.conversion.go
│       │   ├── zz_generated.deepcopy.go
│       │   └── zz_generated.defaults.go
│       └── zz_generated.deepcopy.go
├── conversion 提供对象版本控制
│   ├── ...
├── fields 简单的字段体系，可以匹配selectors指定的字段
│   ├── ...
├── labels 简单的标签体系，可以匹配selectors指定的标签
│   ├── ...
├── runtime
│   ├── codec.go 编解码
│   ├── codec_check.go
│   ├── conversion.go 转换
│   ├── converter.go interface和map之间的转换
│   ├── embedded.go 编解码相关
│   ├── extension.go
│   ├── interfaces.go 各种接口
│   ├── register.go TypeMeta的方法
│   ├── schema Group，Version，Kind定义
│   │   ├── ...
│   ├── scheme.go Schema定义，用来管理GVK和go struct之间的映射
│   ├── scheme_builder.go 用来管理Schema
│   ├── serializer 序列化相关（json,protobuf,yaml）
│   │   ├── ...
│   ├── types.go 定义了每个k8s对象都需要用的TypeMeta，表示GVK
├── selection 定义selecotr筛选的动作
│   └── operator.go
├── types 一些简单的定义
│   ├── doc.go
│   ├── namespacedname.go
│   ├── nodename.go
│   ├── patch.go 定义修改对象的几种方式（jsonPatch,mergePatch等）
│   └── uid.go
├── util
│   ├── cache
│   │   ├── expiring.go
│   │   ├── expiring_test.go
│   │   ├── lruexpirecache.go
│   │   └── lruexpirecache_test.go
│   ├── clock
│   │   ├── clock.go
│   │   └── clock_test.go
│   ├── diff
│   │   ├── diff.go
│   │   └── diff_test.go
│   ├── duration
│   │   ├── duration.go
│   │   └── duration_test.go
│   ├── errors
│   │   ├── doc.go
│   │   ├── errors.go
│   │   └── errors_test.go
│   ├── framer
│   │   ├── framer.go
│   │   └── framer_test.go
│   ├── httpstream
│   │   ├── doc.go
│   │   ├── httpstream.go
│   │   ├── httpstream_test.go
│   │   └── spdy
│   │       ├── connection.go
│   │       ├── connection_test.go
│   │       ├── roundtripper.go
│   │       ├── roundtripper_test.go
│   │       ├── upgrade.go
│   │       └── upgrade_test.go
│   ├── intstr
│   │   ├── generated.pb.go
│   │   ├── generated.proto
│   │   ├── instr_fuzz.go
│   │   ├── intstr.go
│   │   └── intstr_test.go
│   ├── json
│   │   ├── json.go
│   │   └── json_test.go
│   ├── jsonmergepatch
│   │   ├── patch.go
│   │   └── patch_test.go
│   ├── mergepatch
│   │   ├── OWNERS
│   │   ├── errors.go
│   │   ├── util.go
│   │   └── util_test.go
│   ├── naming
│   │   ├── from_stack.go
│   │   └── from_stack_test.go
│   ├── net
│   │   ├── http.go
│   │   ├── http_test.go
│   │   ├── interface.go
│   │   ├── interface_test.go
│   │   ├── port_range.go
│   │   ├── port_range_test.go
│   │   ├── port_split.go
│   │   ├── port_split_test.go
│   │   ├── util.go
│   │   └── util_test.go
│   ├── proxy
│   │   ├── dial.go
│   │   ├── dial_test.go
│   │   ├── doc.go
│   │   ├── transport.go
│   │   ├── transport_test.go
│   │   ├── upgradeaware.go
│   │   └── upgradeaware_test.go
│   ├── rand
│   │   ├── rand.go
│   │   └── rand_test.go
│   ├── remotecommand
│   │   └── constants.go
│   ├── runtime
│   │   ├── runtime.go
│   │   └── runtime_test.go
│   ├── sets
│   │   ├── byte.go
│   │   ├── doc.go
│   │   ├── empty.go
│   │   ├── int.go
│   │   ├── int32.go
│   │   ├── int64.go
│   │   ├── set_test.go
│   │   ├── string.go
│   │   └── types
│   │       └── types.go
│   ├── strategicpatch
│   │   ├── errors.go
│   │   ├── meta.go
│   │   ├── patch.go
│   │   ├── patch_test.go
│   │   ├── testdata
│   │   │   ├── swagger-merge-item.json
│   │   │   └── swagger-precision-item.json
│   │   ├── testing
│   │   │   └── openapi.go
│   │   └── types.go
│   ├── uuid
│   │   └── uuid.go
│   ├── validation
│   │   ├── field
│   │   │   ├── errors.go
│   │   │   ├── errors_test.go
│   │   │   ├── path.go
│   │   │   └── path_test.go
│   │   ├── validation.go
│   │   └── validation_test.go
│   ├── version
│   │   ├── doc.go
│   │   ├── version.go
│   │   └── version_test.go
│   ├── wait
│   │   ├── doc.go
│   │   ├── wait.go
│   │   └── wait_test.go
│   ├── waitgroup
│   │   ├── doc.go
│   │   ├── waitgroup.go
│   │   └── waitgroup_test.go
│   └── yaml
│       ├── decoder.go
│       └── decoder_test.go
├── version
│   ├── doc.go
│   ├── helpers.go
│   ├── helpers_test.go
│   └── types.go
└── watch 监听对象发生的事件
    ├── ...
```