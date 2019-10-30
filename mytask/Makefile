CC = g++
CFLAGS = -g -lstdc++ -lopencv_core -lopvencv_highgui -lopencv_videoio -lopencv_imgcodecs

OPENCV = `pkg-config --cflags opencv` `pkg-config --libs opencv`
LIBS = $(OPENCV)

TOP_DIR = $(PWD)
BIN_DIR = $(TOP_DIR)/bin
SRC_DIR = $(TOP_DIR)/src
SUB_DIR = src \

#TARGET = $(BIN_DIR)/change_blackpart $(BIN_DIR)/image_resizing $(BIN_DIR)/image_rotation $(BIN_DIR)/edge_detection $(BIN_DIR)/orientation_analysis $(BIN_DIR)/hog $(BIN_DIR)/corner_detectiion $(BIN_DIR)/webcam_corner $(BIN_DIR)/webam_match $(BIN_DIR)/face_detection $(BIN_DIR)/save_face $(BIN_DIR)/face_lock $(BIN_DIR)/face_lbp

TARGET = $(BIN_DIR)/sift

export CC CFLAGS OPENCV LIBS TOP_DIR BIN_DIR SRC_DIR SUB_DIR TARGET

all: CHECKDIR $(SUB_DIR)

CHECKDIR:
	mkdir -p $(SUB_DIR) $(BIN_DIR)

$(SUB_DIR):ECHO
	make all -c $@

ECHO:
	@echo $(SUB_DIR)
	@echo begin compile

clean:
	rm -fr $(BIN_DIR)
	rm -fr img_folder/*.bmp

