# Lung CT Segmentation

## Dependencies

- Check the required python packages in `requirements.txt`.

## Datasets

- [**EXACT09**](http://image.diku.dk/exact/)


The file structure should be like this

```
/data/Airway/EXACT09
    /Training
        /CASE01
            /1093782
            /1093783
            ...
        /CASE02
        ...
    /Testing
        /CASE21
        ...
```

- [**LIDC-IDRI**](https://wiki.cancerimagingarchive.net/display/Public/LIDC-IDRI)

The file structure should be like this

```
/data/Airway/LIDC-IDRI
    /LIDC-IDRI-0001
        /1.3.6.1.4.1.14519.5.2.1.6279.6001.298806137288633453246975630178
            /1.3.6.1.4.1.14519.5.2.1.6279.6001.179049373636438705059720603192
                /1-001.dcm
                /1-002.dcm
                ...
    /LIDC-IDRI-0002
    ...
```

## Run the code

- **[Dataset preparation]**

    - Download the two datasets: EXACT09 and LIDC-IDRI.

    - Run ```dataset_preprocess_EXACT09.ipynb``` and ```dataset_preprocess_LIDC-IDRI.ipynb``` to preprocess the images.

    - Run ```Pre_crop_images.ipynb``` to pre-crop the images to be samll cubes.

    - Run ```Get_dataset_info.ipynb``` to generate dataset info which are pkl files.

- **[Training]** Run ```train.py``` to start training. You can change the hyperparameters. Model parameters are saved in ```checkpoint```.

- **[Inference]** Run ```NaviAirway_pipeline.ipynb```.