#define source files

ALEXAPI_SRCS =	capture.py \
		config.py \
		constants.py \
		exceptions.py \
		__init__.py \
		tunein.py

alexapidir = $(pythondir)/alexapi
alexapi_PYTHON = ${ALEXAPI_SRCS};

ALEXAPI_DEVICE_PLATFORM_SRCS =	device_platforms/baseplatform.py \
				device_platforms/hyperionplatform.py \
				device_platforms/raspberrypiplatform.py \
				device_platforms/chipplatform.py \
				device_platforms/__init__.py \
				device_platforms/rpilikeplatform.py \
				device_platforms/desktopplatform.py \
				device_platforms/magicmirrorplatform.py \
				device_platforms/serialplatform.py \
				device_platforms/dummyplatform.py \
				device_platforms/orangepiplatform.py

alexapideviceplatformdir = $(pythondir)/alexapi/device_platforms
alexapideviceplatform_PYTHON = ${ALEXAPI_DEVICE_PLATFORM_SRCS};

ALEXAPI_PLAYBACK_HANDLERS_SRCS =	playback_handlers/basehandler.py \
					playback_handlers/__init__.py \
					playback_handlers/soxhandler.py \
					playback_handlers/vlchandler.py

alexapiplaybackhandlersdir = $(pythondir)/alexapi/playback_handlers
alexapiplaybackhandlers_PYTHON = ${ALEXAPI_PLAYBACK_HANDLERS_SRCS};

ALEXAPI_TRIGGERS_SRCS = triggers/basetrigger.py \
			triggers/__init__.py \
			triggers/platformtrigger.py \
			triggers/pocketsphinxtrigger.py

alexapitriggersdir = $(pythondir)/alexapi/triggers
alexapitriggers_PYTHON = ${ALEXAPI_TRIGGERS_SRCS};
