cmake_minimum_required (VERSION 2.6)
project (Tutorial)
# バージョン番号
set (Tutorial_VERSION_MAJOR 1)
set (Tutorial_VERSION_MINOR 0)

# CMake の設定をソースコードに渡すための
# ヘッダファイルの構成
configure_file (
	  "${PROJECT_SOURCE_DIR}/TutorialConfig.h.in"
	    "${PROJECT_BINARY_DIR}/TutorialConfig.h"
	      )

      # TutorialConfig.h を検出できるように，
      # インクルードファイルの探索パスにバイナリツリーを追加
      include_directories("${PROJECT_BINARY_DIR}")

      # 実行ファイルを追加
      add_executable(Tutorial tutorial.cpp)
