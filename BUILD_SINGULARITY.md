# Singularity for ai-forever's ghost

## Build your own singularity container: 


    1. clone the repo
    2. run: ``` $ chmod +x ./download_models.sh && download_models.sh ```
    3. run: sudo singularity build ghost_singularity.sif ghost_singularity.def


## Run the singularity container: 
```
$ singularity run --nv \
    -B $PWD:/data \
    ghost_singularity.sif \
    --batch_size 8 \
    --source_paths /data/examples/images/beckham.jpg \
    --target_video /data/examples/videos/dance.mp4 \
    --out_video_name /data/output.mp4
```


