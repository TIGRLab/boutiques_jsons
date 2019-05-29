# boutiques_jsons
Our descriptor and invocation jsons for our pipelines. Ask Gabi if you have questions, feel free to fix Gabi's mistakes.

filenames with an `_in` suffix are the invocation/input jsons.

MRIQC: mriqc.json & mriqc_in.json

ciftify: fmriprep_ciftify_bosh.json  ciftify_in.json

freesurfer: freesurfer6_bidsapp.json 

fmriprep: fmriprep.json


The paths inside of the invocation jsons are relative to the singularity container. An example call to ciftify could look like this:

`bosh exec launch -v /directory/to/bind/as/bids:/bids -v /directory/to/bind/as/output:/ciftify_output -v /directory/to/bind/with/freesurfer/license:/license -x --workdir /directory/to/bind/as/workdir
fmriprep_ciftify_bosh.json ciftify_in.json --imagepath /archive/code/containers/FMRIPREP_CIFTIFY/tigrlab_fmriprep_ciftify_1.3.0.post2-2.3.1-2019-04-04-8ebe3500bebf.img`
