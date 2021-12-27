############################################################################################################################
## MAKE SOURCE FILE                                                                                                       ##
############################################################################################################################
 # Project    : Example Makefile Template
 # File Name  : Makefile
 # Author     : Dhanush.K (dhanushsandy98@gmail.com)
 # Date       : 19/11/2021
 # 
 # Revised on : 27/12/2021
 # Version    : V0.0.2
 # 
 # Brief      : Project make file, Please read carefully and build the project by following commands, 
 #              Build		: ~$ make (or) make	all
 #				Build & Run	: ~$ make run
 #				Clean		: ~$ make clean
 # 
 # Reference  : 
 # 
 ##
############################################################################################################################
 # Licence    : MIT
 # Copyright (c) 2021 Dhanush.K
 ##
############################################################################################################################

# Project Name
PROJECT_NAME = EXAMPLE_MAKE

# Application Name
PROGRAM = $(PROJECT_NAME)_APP

# Project Directory
PROJECT_ROOT = $(dir $(abspath $(lastword $(MAKEFILE_LIST))))

# Run time Auguments
RUN_ARUG +=

# Compiler Target Options
CC_C = gcc
CC_CPP = g++

# Project files
C_MAIN  += Main.c
C_FILES += 

# Load Library.
LDLIBS +=

# Linker Flags.
LDFLAGS += 

# Feature Test Macros Arguments,
# "-D_DEFAULT_SOURCE" Enables the Features from 2008 edition of POSIX
#		|-> Here we used for "usleep" function call.
# "-D_GNU_SOURCE" Everything is included: ISO C89, C99, POSEX.1, POSEX.2, BSD, SVID, X/Open, LFS and GNU Extention.
#		|-> Here we used for "pthread_setname_np" function call.
MARCO_ARUG += -D_DEFAULT_SOURCE
MARCO_ARUG += -D_GNU_SOURCE

# Build Path
BUILD_DIR = ./build

# Objects Directory
OBJ_DIR = $(BUILD_DIR)/obj

# Object Files
OBJECTS := $(addprefix $(OBJ_DIR)/default/, $(C_FILES:%.c=%.o))

# C-Standards
STD_VAR = c99

# Build Arguments
CFLAGS += -Wall				# Enable all Warnings
CFLAGS += -O3				# Optimization Level, -O3 optimize max.
CFLAGS += -std=$(STD_VAR)	# C-Standards

#-----------------------------------------------------------------------------------------------------------
# Makefile Targets
#-----------------------------------------------------------------------------------------------------------
# Main Build target
all: start $(PROGRAM)

# Startup Message
start:
	@echo "Builing $(PROGRAM)...\n"

# Default Build Traget
$(PROGRAM): $(C_MAIN) $(OBJECTS)
	$(CC_C) $(MARCO_ARUG) $(CFLAGS) -g $(C_MAIN) $(OBJECTS) -o $(BUILD_DIR)/$@ $(LDFLAGS) $(LDLIBS)
	@echo "\n$(CC_C) Build Finish.!\n"

$(OBJ_DIR)/default/%.o: %.c %.h
	@mkdir -p $(@D)
	$(CC_C) $(MARCO_ARUG) $(CFLAGS) -c $< -o $@ $(LDFLAGS) $(LDLIBS)

# Run the Application
run: $(APP)
	@echo Running the $(PROGRAM)
	$(BUILD_PATH)$(APP)_APP $(RUN_ARUG)

# Clean Build
clean:
	-rm -rf ./build/*
	@echo "Clean Finished.!"

.PHONY: clean run

############################################################################################################
## End of File												  ##
############################################################################################################
