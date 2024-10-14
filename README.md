## OHiFormer: Object-Wise Hierarchical Dependency-Based Transformer for Screen Summarization 

This is the official PyTorch implementation for the paper "OHiFormer: Object-Wise Hierarchical Dependency-Based Transformer for Screen Summarization".

## Abstract
Screen summarization aims to generate concise textual descriptions that communicate the crucial contents and functionalities of a mobile user interface (UI) screen. A UI screen consists of objects with a hierarchical structure that are tightly interconnected, and each object contains multimodal data such as images, texts, and bounding boxes. Considering these characteristics, previous works encoded the absolute position of objects at the view hierarchy to extract the semantic representation of the UI screen. However, the importance of the hierarchical dependency between objects in the UI structure was overlooked. In this study, we propose an object-wise hierarchical dependency-based Transformer named OHiFormer. OHiFormer considers the objects on the UI screen as tokens in natural language processing and leverages the Transformer to capture the mutual relationships between objects. Moreover, OHiFormer includes a modified self-attention mechanism using structural relative position encoding to represent the hierarchically connected UI. Experimental results demonstrate that OHiFormer outperforms benchmark models in the BLEU 1, BLEU 2, BLEU 3, BLEU 4, ROUGE-L, and CIDEr metrics by 3.63%, 2.1%, 0.12%, 1.8%, 2.38%, and 17.58%, respectively, on the Screen Summarization dataset. Furthermore, our proposed UI structural representation method achieves remarkable performance on complex UIs with numerous objects compared to other structural position encoding methods. Finally, a visualization of the selfattention heatmaps demonstrates how OHiFormer reflects the hierarchical dependencies between objects. By reflecting hierarchical dependencies hidden in the visual layout of the UI, OHiFormer not only improves the quality of summaries but also offers the potential for applications in mobile apps and systems containing numerous interactive objects.

## Architecture
Overview of OHiFormer. It uses the multimodal UI features, represented by the image, text, and bounding box embeddings, as input. The structural relative position encoding is injected into the object-wise hierarchical dependency-based multi-head attention module.
![image](https://github.com/user-attachments/assets/6e99365b-f946-4b54-8ad2-7de4be02647c)

## Main results
| Model         | Ref.point | BLEU1 | BLEU2 | BLEU3 | BLEU4 | ROUGE-L | CIDEr |
|---------------|-----------|-------|-------|-------|-------|---------|-------|
| Screen2Words  | Abs.      | 65.6  | 45.8  | 32.4  | **25.1**  | 48.6    | 61.3  |
| VUT           | Abs.      | 68.9  | 50.8  | 33.5  | 21.4  | 54.9    | 65.6  |
| **OHiFormer** | **Rel.**  | **72.53** | **52.9**  | **33.62** | 23.78 | **56.7** | **83.18** |
   
## Citation
```
@article{han2024ohiformer,
  title={OHiFormer: Object-Wise Hierarchical Dependency-Based Transformer for Screen Summarization},
  author={Han, Ye Ji and Lee, SoYeon and Kim, Jin Sob and Lee, Byung Hoon and Han, Sung Won},
  journal={IEEE Access},
  year={2024},
  publisher={IEEE}
}
```
