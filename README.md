# Pico XS Project Template
This sample project blinks an LED on the Pico board using [Pico XS](https://github.com/fischer36/pico_xs).

## Compilation 
```bash
# Add the ARM Cortex-M0+ compilation target required for the Pico
rustup target add thumbv6m-none-eabi

# Install elf2uf2-rs to convert ELF binaries to UF2 format
cargo install elf2uf2-rs --locked

# Compile
cargo build --release --target thumbv6m-none-eabi 

# Convert to UF2
elf2uf2-rs target/thumbv6m-none-eabi/release/sample-project sample-project.uf2   

# Flash by moving the UF2 file to the Pico USB drive
```
