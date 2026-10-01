**
- Containers: enroot

## Links

- 
## Connection

- partition with percentages
- explicit parallelism
- 
- `ssh login.ai.lrz.de -l ra38xuj2`
- Storage
	- DSS (requires projects)
	- User dir: `/dss/dsshome1/0D/ra38xuj2`
- `squeue -u $USER`
	- See current jobs


## CMA



### Fairness Datasets

Custom enroot https://doku.lrz.de/10-creating-and-reusing-a-custom-enroot-container-image-10746637.html

```bash
# First alloc, then go inside
salloc -p lrz-v100x2 --gres=gpu:1

srun --pty bash 
# Get image
unlink ./image-no-cuda.sqsh
enroot import -o image-no-cuda.sqsh docker://ghcr.io#jansim/fairness-datasets-2:latest
```

what's available?
```
sinfo
```

```
sbatch ds-2.sbatch

sbatch ds-2__continue.sbatch
```


```bash
srun --pty --container-mounts=./output:/app/output,./cache:/app/cache --container-image=/dss/dsshome1/0D/ra38xuj2/ds-2/image-no-cuda.sqsh uv run -m multiversum --mode full
```

```bash
srun --pty --container-mounts=./output:/app/output --container-mounts=./cache:/app/cache --container-image=/dss/dsshome1/0D/ra38xuj2/ds-2/image-no-cuda.sqsh bash
```

```bash
srun --pty --container-mounts=./test:/app/ --container-image=/dss/dsshome1/0D/ra38xuj2/ds-2/image-no-cuda.sqsh uv run -m multiversum --mode full
```

Can only do one mount!

```bash
srun --pty --container-mounts=./output:/app/output --container-image=/dss/dsshome1/0D/ra38xuj2/ds-2/image-no-cuda.sqsh uv run -m multiversum --mode full
```

comma seems to work
```bash
srun --pty --container-mounts=./output:/app/output,./cache:/app/cache --container-image=/dss/dsshome1/0D/ra38xuj2/ds-2/image-no-cuda.sqsh uv run -m multiversum --mode full
```


batch script

```bash
sbatch ds-2.sbatch
```

```
#!/bin/bash
#SBATCH -p lrz-v100x2 
#SBATCH -t 10:00:00
#SBATCH --gres=gpu:1
#SBATCH -o std_out.out
#SBATCH -e std_err.err
#SBATCH --container-mounts=./output:/app/output,./cache:/app/cache
#SBATCH --container-image=/dss/dsshome1/0D/ra38xuj2/ds-2/image-no-cuda.sqsh

uv run -m multiversum --mode full
```



```bash
squeue -u ra38xuj2
```