commit d47e011666084da68b23aecce57054100426fef3
Author: wjb <jaybob413@gmail.com>
Date:   Fri Nov 18 23:09:33 2011 -0500

    Temporary hack to avoid building libpreprocessing (needs webrtc) - rename Android.mk
    
    Change-Id: I5c193036d88dcb18b73a72d464f5e3f52a147c5b

diff --git a/media/libeffects/preprocessing/Android.mk b/media/libeffects/preprocessing/Android.mk
deleted file mode 100755
index 77d40b6..0000000
--- a/media/libeffects/preprocessing/Android.mk
+++ /dev/null
@@ -1,32 +0,0 @@
-LOCAL_PATH:= $(call my-dir)
-
-# audio preprocessing wrapper
-include $(CLEAR_VARS)
-
-LOCAL_MODULE:= libaudiopreprocessing
-LOCAL_MODULE_TAGS := optional
-LOCAL_MODULE_PATH := $(TARGET_OUT_SHARED_LIBRARIES)/soundfx
-
-LOCAL_SRC_FILES:= \
-    PreProcessing.cpp
-
-LOCAL_C_INCLUDES += \
-    external/webrtc/src \
-    external/webrtc/src/modules/interface \
-    external/webrtc/src/modules/audio_processing/main/interface \
-    system/media/audio_effects/include
-
-LOCAL_C_INCLUDES += $(call include-path-for, speex)
-
-LOCAL_SHARED_LIBRARIES := \
-    libwebrtc_audio_preprocessing \
-    libspeexresampler \
-    libutils
-
-ifeq ($(TARGET_SIMULATOR),true)
-LOCAL_LDLIBS += -ldl
-else
-LOCAL_SHARED_LIBRARIES += libdl
-endif
-
-include $(BUILD_SHARED_LIBRARY)
diff --git a/media/libeffects/preprocessing/Android.mk.bak b/media/libeffects/preprocessing/Android.mk.bak
new file mode 100755
index 0000000..77d40b6
--- /dev/null
+++ b/media/libeffects/preprocessing/Android.mk.bak
@@ -0,0 +1,32 @@
+LOCAL_PATH:= $(call my-dir)
+
+# audio preprocessing wrapper
+include $(CLEAR_VARS)
+
+LOCAL_MODULE:= libaudiopreprocessing
+LOCAL_MODULE_TAGS := optional
+LOCAL_MODULE_PATH := $(TARGET_OUT_SHARED_LIBRARIES)/soundfx
+
+LOCAL_SRC_FILES:= \
+    PreProcessing.cpp
+
+LOCAL_C_INCLUDES += \
+    external/webrtc/src \
+    external/webrtc/src/modules/interface \
+    external/webrtc/src/modules/audio_processing/main/interface \
+    system/media/audio_effects/include
+
+LOCAL_C_INCLUDES += $(call include-path-for, speex)
+
+LOCAL_SHARED_LIBRARIES := \
+    libwebrtc_audio_preprocessing \
+    libspeexresampler \
+    libutils
+
+ifeq ($(TARGET_SIMULATOR),true)
+LOCAL_LDLIBS += -ldl
+else
+LOCAL_SHARED_LIBRARIES += libdl
+endif
+
+include $(BUILD_SHARED_LIBRARY)
