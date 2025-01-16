# Emscripten

## Build

```
mkdir build
cd build
emcmake cmake ..
emmake make
```

## Link

```
em++ -O3 ../../imlib/libimlib.a ../../lisp/liblisp.a ../../net/libnet.a ../../sdlport/libsdlport.a *.o */*.o -o index.html -sUSE_SDL=2 -sUSE_SDL_MIXER=2 -sSDL2_MIXER_FORMATS='["mid","wav"]' -sASYNCIFY -sENVIRONMENT=web --preload-file ../../../../data/@data/ --preload-file dgguspat/ --preload-file timidity.cfg -sSTACK_SIZE=131072 --closure 1 -sEXPORTED_RUNTIME_METHODS=['allocate']
```
