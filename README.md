
# Image Generation Metrics Notebook

This notebook trains and evaluates an image generation model (GAN) using PyTorch. It computes the following metrics:
- **Frechet Inception Distance (FID)**: Measures the similarity between the generated images and the dataset.
- **Intra-FID**: Computes FID for each class or subclass separately.
- **Inception Score**: Evaluates the diversity and quality of generated images.

## How to Download 

1. Clone the Repository
   ```
   git clone https://github.com/Battlehooks/ricebowl-cifar-100-gen.git
   cd ricebowl-cifar-100 gen
   ```
2. Install the prerequisites below

## Prerequisites

1. Install Python (version >= 3.8 is recommended).
2. Install Jupyter Notebook:
   ```
   pip install jupyter notebook
   ```

3. Install the required Python libraries:
   ```
   pip install torch torchvision torchmetrics tqdm pillow scipy numpy
   ```
   or
   ```
   pip install -r requirements.txt
   ```

## How to Use the Notebook

### 1. Clone or Download the Notebook
Save the notebook file to your desired directory.

### 2. Set Up the Environment
Ensure you have a GPU-enabled environment for optimal performance (CUDA is required).

### 3. Reproducibility: Set the SEED
The notebook uses a predefined SEED for reproducibility:
```python
SEED = 42
```
You can modify this value in the notebook.

### 4. Running the Notebook
1. Open the notebook:
   ```
   jupyter notebook Main.ipynb
   ```

2. Run all cells sequentially. Ensure that the CUDA environment is set up correctly if running on GPU.

3. The notebook will output the following metrics:
   - **FID**
   - **Intra-FID Mean and Std**
   - **Inception Score Mean and Std**

4. During training, images will be saved in the `generated_samples` directory.

### 5. Output
At the end of execution, you will see the computed metrics printed in the final cell, e.g.:
```
FID : 92.35295142621786 		 Intra-FID : 203.00923767768046 (std: 41.58789489848683) 		 Inception Score : 5.023540496826172 (std: 0.056270573288202286) 
Superclass 0 : 168.0937694440035
Superclass 1 : 143.0529514583625
Superclass 2 : 207.87133502221496
Superclass 3 : 112.85649723740383
Superclass 4 : 236.0155400814707
Superclass 5 : 195.81918057929246
Superclass 6 : 182.35370335596235
Superclass 7 : 260.99065905158744
Superclass 8 : 232.10020306014218
Superclass 9 : 190.30455263374557
Superclass 10 : 206.36457349167597
Superclass 11 : 305.6945781238964
Superclass 12 : 229.05193562461199
Superclass 13 : 171.4540269489463
Superclass 14 : 198.05857429943802
Superclass 15 : 201.41546623269753
Superclass 16 : 196.36619489670176
Superclass 17 : 254.2173988003457
Superclass 18 : 179.20203719899672
Superclass 19 : 188.90157601211308
```
