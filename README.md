# glTF Viewer

three.js와 드래그 앤 드롭 인터페이스를 사용하는 WebGL 기반 glTF 2.0 모델 뷰어입니다

## Web
https://sokcuri.github.io/three-gltf-viewer/

## FBX to glTF 변환
Facebook의 [FBX2glTF](https://github.com/facebookincubator/FBX2glTF) 프로그램을 이용해 FBX를 glTF로 변환할 수 있습니다.
glTF Viewer는 glTF의 바이너리 패커인 glb를 지원합니다. FBX2glTF 변환 시 -b 옵션을 주어 glb 파일로 변환하는 것이 좋습니다.
FBX2glTF는 [릴리즈 페이지](https://github.com/facebookincubator/FBX2glTF/releases)에서 다운로드 가능합니다.

```
FBX2glTF 2.0: Generate a glTF 2.0 representation of an FBX model.
Usage:
  FBX2glTF [OPTION...] [<FBX File>]

  -i, --input arg               The FBX model to convert.
  -o, --output arg              Where to generate the output, without suffix.
  -e, --embed                   Inline buffers as data:// URIs within
                                generated non-binary glTF.
  -b, --binary                  Output a single binary format .glb file.
      --long-indices arg        Whether to use 32-bit indices
                                (never|auto|always).
  -d, --draco                   Apply Draco mesh compression to geometries.
      --compute-normals arg     When to compute normals for vertices
                                (never|broken|missing|always).
      --flip-u                  Flip all U texture coordinates.
      --flip-v                  Flip all V texture coordinates (default
                                behaviour!)
      --no-flip-v               Suppress the default flipping of V texture
                                coordinates
      --pbr-metallic-roughness  Try to glean glTF 2.0 native PBR attributes
                                from the FBX.
      --khr-materials-unlit     Use KHR_materials_unlit extension to specify
                                Unlit shader.
      --blend-shape-normals     Include blend shape normals, if reported
                                present by the FBX SDK.
      --blend-shape-tangents    Include blend shape tangents, if reported
                                present by the FBX SDK.
  -k, --keep-attribute arg      Used repeatedly to build a limiting set of
                                vertex attributes to keep.
  -v, --verbose                 Enable verbose output.
  -h, --help                    Show this help.
  -V, --version                 Display the current program version.
```

## 리포지토리 한정 변경사항
glTF Viewer는 UI로 dat.gui 라이브러리르 사용하는데, 필드의 이름과 값 너비가 정해져 있어 Animation name 등을 제대로 확인할 수 없습니다. 이 리포지토리는 수정된 dat.gui를 사용해 이슈를 고칩니다.
* [sokcuri/dat.gui](https://github.com/sokcuri/dat.gui)

## Quickstart

### Web

```
npm install
npm run dev
```

### Build
```
npm run build
```

## Original
* Author : donmccurdy (https://github.com/donmccurdy/three-gltf-viewer)

## glTF 2.0 Resources

- [THREE.GLTFLoader](https://github.com/mrdoob/three.js/blob/dev/examples/js/loaders/GLTFLoader.js)
- [glTF 2.0 Specification](https://github.com/KhronosGroup/glTF/blob/master/specification/2.0/README.md)
- [glTF 2.0 Sample Models](https://github.com/KhronosGroup/glTF-Sample-Models/tree/master/2.0/)

## Known Issues

- [ ] Limited drag-and-drop support in Safari.
