############################################################################################################################
## MAKE SOURCE FILE                                                                                                       ##
############################################################################################################################
 # Project    : Example Makefile Template
 # File Name  : Makefile
 # Author     : Dhanush.K (dhanushsandy98@gmail.com)
 # Date       : 19/11/2021
 # 
 # Revised on : 11/11/2021
 # Version    : V0.0.1
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

# Application Name
APP = EXAMPLE

# Target files
TARGETS = \

# Run time Auguments
RUN_ARUG = \

# Macro Configuration Arguments
MARCO_ARUG = \
-D \
_DEFAULT_SOURCE

# Additinal Library Arguments
LIB_ARUG = \

# Compiler Options
CC_C = gcc

# Build Path
BUILD_PATH = ./build/

# Build Arguments
CFLAGS = -Wall -g -std=$(STD_VAR)
STD_VAR = c99

# Make commands
all: clean $(APP)

# Build Application
$(APP):
	$(CC_C) $(MARCO_ARUG) $(CFLAGS) $(TARGETS) -o $(BUILD_PATH)$(APP)_APP $(LIB_ARUG)

# Run the Application
run: $(APP)
	$(BUILD_PATH)$(APP)_APP

# Clean Build
clean:
	rm -rf $(BUILD_PATH)*

############################################################################################################
##											End of File                                                   ##
############################################################################################################