TARGET=Textures.xbt
XBMCTEX=/home/marcel/workspace/xbmc/tools/TexturePacker/TexturePacker

IMAGES := $(shell find . -name "*jpg")
IMAGES += $(shell find . -name "*png")
IMAGES += $(shell find . -name "*gif")

all: $(TARGET)

.PHONY: force

$(TARGET): $(XBMCTEX) $(IMAGES)
ifeq (x86_64-linux,arm)
	$(XBMCTEX) -use_none -input . -output $(TARGET)
else
	$(XBMCTEX) -input . -output $(TARGET)

endif
$(XBMCTEX): force
	$(MAKE) -C /home/marcel/workspace/xbmc/tools/TexturePacker

clean:
	rm -f $(TARGET)
distclean: clean

