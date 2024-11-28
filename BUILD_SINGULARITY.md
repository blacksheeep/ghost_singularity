# Singularity for ai-forever's ghost

## Build your own singularity container: 


    1. clone the repo
    2. run: ``` $ chmod +x ./download_models.sh && download_models.sh ```
    3. run: sudo sudo singularity build ghost_singularity.sif ghost_singularity.def


## Run the singularity container: 
```
$ singularity exec --nv \
    ghost.sif python inference.py \
    --batch_size 8 \
    --source_paths ./examples/images/beckham.jpg \
    --target_video ./examples/videos/dance.mp4 \
    --out_video_name ./output.mp4
```


