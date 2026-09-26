# Neural Network on STM32

This project was created to test the ability and efficiency of running a neural network on an STM32 development kit.

The main goal was to upload a simple TensorFlow model to the STM32 kit and measure how long it takes to run the model.

## Project Steps

1. Create a simple TensorFlow model.
2. Download and prepare TensorFlow Lite Micro.
3. Adapt the TensorFlow Lite Micro library for the STM32 project.
4. Upload the model to the STM32 kit.
5. Run the model on the microcontroller.
6. Measure the model execution time.
7. Analyze the performance of the model on the hardware.

## TensorFlow Lite Micro Setup

TensorFlow Lite Micro was used to adapt and run the TensorFlow model on the microcontroller.

Clone the TensorFlow Lite Micro repository:

```bash
git clone https://github.com/tensorflow/tflite-micro.git
```

Generate the required project files for the STM32 Cortex-M4 target:

```bash
python3 tensorflow/lite/micro/tools/project_generation/create_tflm_tree.py \
-e hello_world \
-makefile_options="TARGET_ARCH=cortex-m4" \
/path/to/your/stm32/project
```

Replace `/path/to/your/stm32/project` with the path to the STM32 project.

## STM32 Project Configuration

The TensorFlow Lite Micro library then needs to be added to the STM32 project:

1. Configure the build settings.
2. Add the required header file paths.
3. Configure the preprocessor definitions.
4. Configure compilation optimization.
5. Configure the linker settings.

After configuring the project, compile and upload it to the STM32 microcontroller.

The final step is to run the TensorFlow Lite Micro model on the STM32 and measure its execution time to evaluate the performance of the neural network on the hardware.
