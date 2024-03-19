This is a raw protobuf to JSON parser written in C, compiled to wasm. It can be used to parse binary protobuf, when you do not have access to the source SDL.

If you want to read about how I compiled protoc & libs (included in this repo) check out [this](build_protobuf_wasm). You shouldn't need to actually build this, since it's included, and it's in cross-platform wasm.

```
# build the wasm-portion of the lib
npm run build
```