# DMA Controller (Verilog)

This project implements a simplified DMA controller in Verilog based on the block diagram shown below. The controller supports 8 independent streams, each configurable to use one of 8 channels, with FIFO buffering and arbitration between streams.

## 📊 Block Diagram

![DMA Block Diagram](doc/dma_block_diagram.png)

## 📁 Directory Structure

dma_controller_project/
├── src/
│ ├── dma_controller.v
│ ├── dma_stream.v
│ ├── dma_fifo.v
│ ├── dma_channel_selector.v
│ ├── dma_arbiter.v
│ └── ahb_interface.v
├── README.md
└── doc/
└── dma_block_diagram.png


## 🔧 Features

- 8 DMA Streams
- Each stream can be assigned one of 8 channels
- FIFO buffering for each stream
- Round-robin/priority-based arbitration
- AHB Master for memory & peripheral access
- AHB Slave for programming/configuration

## 🔌 Ports Overview

| Module            | Description                                  |
|-------------------|----------------------------------------------|
| `dma_controller`  | Top-level integrating all submodules         |
| `dma_stream`      | Represents an individual stream              |
| `dma_fifo`        | FIFO buffer for data                         |
| `dma_arbiter`     | Manages access priority among streams        |
| `dma_channel_selector` | Maps stream-to-channel requests         |
| `ahb_interface`   | Interface stubs for memory/peripheral access |

## 🛠️ Future Enhancements

- Burst mode support
- Interrupt generation
- Priority-based arbitration with programmable priorities
- Error handling and status reporting

## 📜 License

Open source under MIT License.

