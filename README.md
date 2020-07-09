# BlockDevice trait
```rust
pub trait BlockDevice {
    type Error;
    fn read(&self, buf: &mut [u8], address: u32, number_of_blocks: u32) -> Result<(), Self::Error>;
    fn write(&self, buf: &[u8], address: u32, number_of_blocks: u32) -> Result<(), Self::Error>;
}
```