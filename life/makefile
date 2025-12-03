CC = gcc
CFLAGS = -g -Wall -I$(INCLUDE_DIR)

SRC_DIR = src
BUILD_DIR = build
INCLUDE_DIR = include

#Serial version
SERIAL_SRC = $(SRC_DIR)/life.c $(SRC_DIR)/life_test.c

# OpenMP version uses both life.c and life_omp.c
OMP_SRC = $(SRC_DIR)/life.c $(SRC_DIR)/life_omp.c $(SRC_DIR)/life_test.c


TARGETS = life_serial life_omp speed_test

all: ${TARGETS}

speed_test:
	$(CC) $(CFLAGS) -fopenmp \
		src/life.c src/life_omp.c src/speed_test.c \
		-o build/speed_test

life_serial:
	$(CC) $(CFLAGS) $(SERIAL_SRC) -o $(BUILD_DIR)/$@

life_omp:
	$(CC) $(CFLAGS) -fopenmp $(OMP_SRC) -o $(BUILD_DIR)/$@

run: run_serial run_omp

run_serial: life_serial
	./$(BUILD_DIR)/life_serial

run_omp: life_omp
	./$(BUILD_DIR)/life_omp

run_speed:
	./build/speed_test
