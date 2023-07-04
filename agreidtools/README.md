# AG-ReID Person Re-Identification Toolkit Instructions

The following steps will guide you through the process of setting up the AG-ReID person re-identification toolkit:

1. Begin by extracting the downloaded data into the ``data`` folder.

2. Then, you can initialize the dataloader by executing the reader script. The command for this is:
```bash
python AG-ReIDReader.py --data_path /your/reid_data_root/path
```
   Replace `/your/reid_data_root/path` with the actual path to your re-identification data root directory.

The expected directory structure in `/your/reid_data_root/path` should be as follows:

```
└───[reid_data_root]
    ├───bounding_box_train
        ├───P0001T04041A0C0F31.jpg
        ├───P0001T04041A0C0F61.jpg
        └───...
    ├───bounding_box_test_all_c0
        ├───P0000T02140A0C0F31.jpg
        ├───P0000T02140A0C0F61.jpg
        └───...
    ├───bounding_box_test_all_c3
        ├───P0000T02140A0C3F691.jpg
        ├───P0000T02140A0C3F721.jpg
        └───...
    ├───query_all_c0
        ├───P0000T02140A0C0F91.jpg
        ├───P0000T02140A0C0F121.jpg
        └───...
    ├───query_all_c3
        ├───P0000T02140A0C3F751.jpg
        ├───P0000T02140A0C3F901.jpg
        └───...
    └───qut_attribute_v4_88_attributes.mat
```

Remember, the `reid_data_root` directory should contain separate sub-directories for training and testing bounding boxes, and for queries from different cameras.