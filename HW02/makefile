CC := gcc
std := c99

all: task2a task2b task5

# This time, we use automatic variables in place of filenames.
# $< refers to the names of any dependencies and $@ refers to the target
task2a: task2a.o output.o
	$(CC) $^ -o $@ -std=$(std)

task2b: task2b.o output.o
	$(CC) $^ -o $@ -std=$(std)

task5: task5.o output.o
	$(CC) $^ -o $@ -std=$(std)

# This generic target matches any file with the pattern BASENAME.o
# which is built from a dependency called BASENAME.c
%.o: %.c
	$(CC) -c $< -o $@ -std=$(std)

clean:
	@rm -f *.o task2a task2b task5

# shortcut for compiling and running task2a, intended for quicker use
run_task2a:
	@make -s task2a
	@./task2a

# shortcut for running task2b you have to use, same for task5:
# $ make run_task2b n="insert an integer here"
run_task2b:
	@make -s task2b
	@./task2b $(n)

run_task5:
	@make -s task5
	@./task5 $(n)
