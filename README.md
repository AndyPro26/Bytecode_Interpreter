# Bytecode_Interpreter
This program implements a simple virtual machine (VM) utilizing a stack data structure to execute bytecode instructions. 
The VM supports basic arithmetic operations such as addition, subtraction, multiplication, and division. 
Additionally, it handles errors like division by zero and unknown opcodes.

# Instruction set
    OP_PUSHI: Pushes an immediate argument onto the stack.
    OP_ADD: Pops two values from the stack, adds them, and pushes the result onto the stack.
    OP_SUB: Pops two values from the stack, subtracts them, and pushes the result onto the stack.
    OP_DIV: Pops two values from the stack, divides them (handling division by zero), and pushes the result onto the stack.
    OP_MUL: Pops two values from the stack, multiplies them, and pushes the result onto the stack.
    OP_POP_RES: Pops the top of the stack and sets it as the execution result.
    OP_DONE: Stops the execution.

# Stack Implementation
    The stack is implemented as a fixed-size array (vm.stack) within the VM structure.
    The stack grows upwards, starting from the bottom (vm.stack) and moving towards higher memory addresses.
    The top of the stack is tracked using a pointer (vm.stack_top), which points to the next available space on the stack.
    Stack operations (vm_stack_push and vm_stack_pop) manipulate this pointer to push and pop values onto/from the stack.
