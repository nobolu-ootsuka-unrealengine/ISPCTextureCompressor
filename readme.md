
＃高速ISPCテクスチャコンプレッサ

BC6H、BC7、ETC1、ASTCおよびBC1 / BC3の最先端のテクスチャ圧縮。

[ISPCコンパイラ]（https://ispc.github.io/）を使用します。

[Fast ISPC Texture Compressor]（https://software.intel.com/en-us/articles/fast-ispc-texture-compressor-update）の記事を参照してください。
Intel Developer Zone。

サポートされている圧縮形式：

* BC6H（FP16 HDR入力）
* BC7
* ASTC（LDR、最大8x8のブロックサイズ）
* ETC1
* BC1、BC3（別名DXT1、DXT5）


##ビルド手順

* Windows：
*後でVisual Studio 2012を使用して、ソリューションまたはプロジェクトファイルをビルドします。
*このレポにはISPCバージョン1.8.2が含まれています。

* Mac OS X：
* Xcodeプロジェクトファイルは、コンプレッサーにのみ含まれています。例ではありません。
* ISPCコンパイラバージョン[1.8.2 build]（https://sf.net/projects/ispcmirror）を入手し、コンパイラ実行ファイルを `ISPC Texture Compressor / ispc_osx`に置く必要があります。
* Xcode 7.3でテストされた `ISPC Texture Compressor / ispc_texcomp.xcodeproj`を使用してください。
* OS Xの最小配備バージョンを10.9に設定しました。
* dylibのインストール名は `@executable_path /../Frameworks/ $（EXECUTABLE_PATH）`に設定されています

* Linux：
*メイクファイルは、コンプレッサー自体にのみ含まれています。例ではありません。
* ISPCコンパイラバージョン[1.8.2 build]（https://sf.net/projects/ispcmirror）を入手し、コンパイラ実行ファイルを `ISPC Texture Compressor / ispc_linux`に置く必要があります。
* `Make -f Makefile.linux`を` ISPC Texture Compressor`フォルダから実行します。




ーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーー翻訳おわり　原文下
ーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーー



# Fast ISPC Texture Compressor

State of the art texture compression for BC6H, BC7, ETC1, ASTC and BC1/BC3.

Uses [ISPC compiler](https://ispc.github.io/).

See [Fast ISPC Texture Compressor](https://software.intel.com/en-us/articles/fast-ispc-texture-compressor-update) post on
Intel Developer Zone.

Supported compression formats:

* BC6H (FP16 HDR input)
* BC7
* ASTC (LDR, block sizes up to 8x8)
* ETC1
* BC1, BC3 (aka DXT1, DXT5)


## Build Instructions

* Windows:
	* Use Visual Studio 2012 on later, build solution or project files.
	* ISPC version 1.8.2 is included in this repo.

* Mac OS X:
	* Xcode project file included only for compressor itself, not for the examples.
	* You'll need to get ISPC compiler version [1.8.2 build](https://sf.net/projects/ispcmirror) and put the compiler executable into `ISPC Texture Compressor/ispc_osx`.
	* Use `ISPC Texture Compressor/ispc_texcomp.xcodeproj`, tested with Xcode 7.3.
	* Minimum OS X deployment version set to 10.9.
	* dylib install name is set to `@executable_path/../Frameworks/$(EXECUTABLE_PATH)`

* Linux:
	* Makefile included only for compressor itself, not for the examples.
	* You'll need to get ISPC compiler version [1.8.2 build](https://sf.net/projects/ispcmirror) and put the compiler executable into `ISPC Texture Compressor/ispc_linux`.
	* `make -f Makefile.linux` from `ISPC Texture Compressor` folder.
