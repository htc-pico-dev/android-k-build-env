How to run:

```
docker build --tag android-k-build-env .
docker run --rm -it -v /<your-android-dir>:/var/android android-k-build-env:latest
```

ccache:

```
docker run \
	--rm -it \
	--env USE_CCACHE=1 \
	--env CCACHE_DIR=/var/.ccache \
	--env CCACHE_MAXSIZE=50G \
	-v /<your-android-dir>:/var/android \
	-v /<your-ccache-dir>:/var/.ccache \
	android-k-build-env:latest
```
