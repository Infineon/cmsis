# CMSIS Repository

### Overview
This repository is based on  https://github.com/ARM-software/CMSIS_5/tree/5.8.0.

CMSIS DSP is sourced from https://github.com/ARM-software/CMSIS-DSP

This repository has CMSIS Core headers, CMSIS DSP and CMSIS NN source. It can be used by application or middleware to link CMSIS Core headers. It can also be used to build CMSIS DSP or NN based applications.

### Enabling CMSIS NN and DSP
CMSIS NN and DSP source are not enabled by default. The applications which require CMSIS NN or CMSIS DSP need to update Makefile to add these in the components list:

COMPONENTS += CMSIS_NN CMSIS_DSP

For CM55 with Helium extension, below mentioned define also need to be set in application Makefile
ifeq ($(MTB_RECIPE__CORE),CM55)
DEFINES += ARM_MATH_AUTOVECTORIZE
endif