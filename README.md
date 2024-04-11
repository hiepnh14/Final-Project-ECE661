# Final-Project-ECE661
This is a repository for our final project in ECE 661

## Instruction on how to utilize Apple arm GPU for pytorch
### Requirements:
- Mac computers with Apple silicon or AMD GPUs
- macOS 12.3 or later
- Python 3.7 or later
- Xcode command-line tools: xcode-select --install
- Either have Pip/Pip3 or Conda installed
### Install:
- Anaconda:
```bash
    conda install pytorch torchvision torchaudio -c pytorch-nightly
```
- Pip3:
```bash
    pip3 install --pre torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/nightly/cpu
```

### Verification:
Run this script:
```python
    import torch
    if torch.backends.mps.is_available():
        mps_device = torch.device("mps")
        x = torch.ones(1, device=mps_device)
        print (x)
    else:
        print ("MPS device not found.")
```

Expected output:
```
    tensor([1.], device='mps:0')
```

- Install all requirements in requirements.txt
```bash
    pip3 install -r requirements.txt
```