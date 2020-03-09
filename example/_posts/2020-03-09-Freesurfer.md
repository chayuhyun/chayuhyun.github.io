# Freesurfer

# 사이트 정리

## Freesurfer

[FreeSurfer](https://surfer.nmr.mgh.harvard.edu/)

### **fswiki**

[FreeSurferWiki - Free Surfer Wiki](https://surfer.nmr.mgh.harvard.edu/fswiki)

**Freesurfer Support**

[FreeSurferSupport - Free Surfer Wiki](https://surfer.nmr.mgh.harvard.edu/fswiki/FreeSurferSupport)

**Tutorials**

[Tutorials - Free Surfer Wiki](https://surfer.nmr.mgh.harvard.edu/fswiki/Tutorials)

**FsTutorial**

[FsTutorial - Free Surfer Wiki](https://surfer.nmr.mgh.harvard.edu/fswiki/FsTutorial)

- **Anatomical ROI analysis**

    [FsTutorial/AnatomicalROIV6.0 - Free Surfer Wiki](https://surfer.nmr.mgh.harvard.edu/fswiki/FsTutorial/AnatomicalROIV6.0)

**Pipeline overview**

[FreeSurferAnalysisPipelineOverview - Free Surfer Wiki](https://surfer.nmr.mgh.harvard.edu/fswiki/FreeSurferAnalysisPipelineOverview)

**Freesurfer Workflows**

[FreeSurferWorkFlows - Free Surfer Wiki](https://surfer.nmr.mgh.harvard.edu/fswiki/FreeSurferWorkFlows)

**WorkFlows**

[WorkFlows](https://surfer.nmr.mgh.harvard.edu/fswiki/WorkFlows)

### Protocol

[Neuroimaging Protocols](https://bookdown.org/u0243256/brainiac/)

### Protocol 2

[University of Calgary ARC Manual](https://bookdown.org/u0243256/arc/)

### Class by Camacho

[FreeSurfer Class - M. Catalina Camacho](https://www.catcamacho.net/freesurfer-class)

# Freesurfer 설치하기

---

[DownloadAndInstall - Free Surfer Wiki](https://surfer.nmr.mgh.harvard.edu/fswiki/DownloadAndInstall)

[MacOsInstall - Free Surfer Wiki](https://surfer.nmr.mgh.harvard.edu/fswiki/MacOsInstall)

[MatlabRuntime - Free Surfer Wiki](https://surfer.nmr.mgh.harvard.edu/fswiki/MatlabRuntime)

[FreeSurfer를 이용한 Hippocampal Segmentation 방법](https://donghwa-kim.github.io/hippocampal-segmentation.html)

[UpdateFreeview - Free Surfer Wiki](https://surfer.nmr.mgh.harvard.edu/fswiki/UpdateFreeview)

[20.02.02] stable v6.0.0 설치

[20.02.02] 라이센스 신청 #46138 ([https://surfer.nmr.mgh.harvard.edu/registration.html](https://surfer.nmr.mgh.harvard.edu/registration.html))

- Licence

    [chayu@snu.ac.kr](mailto:chayu@snu.ac.kr)

[20.02.03] Terminal 설치

    export FREESURFER_HOME=/Applications/freesurfer
    source $FREESURFER_HOME/SetUpFreeSurfer.sh

    # Matlab runtime
    # https://surfer.nmr.mgh.harvard.edu/fswiki/MatlabRuntime
    export FREESURFER_HOME=/Applications/freesurfer
    cd $FREESURFER_HOME
    sudo curl "https://surfer.nmr.mgh.harvard.edu/fswiki/MatlabRuntime?action=AttachFile&do=get&target=runtime2012bMAC.tar.gz" -o "runtime.tar.gz"
    sudo tar xvf runtime.tar.gz
    source $FREESURFER_HOME/SetUpFreeSurfer.sh
    sudo chmod -R a+w $FREESURFER_HOME

    # 돌려보기
    cp $FREESURFER_HOME/subjects/sample-001.mgz .
    mri_convert sample-001.mgz sample-001.nii.gz
    mkdir sample-001/
    export SUBJECTS_DIR=sample-001/
    recon-all -s bert -all

    freeview -v \
        mri/T1.mgz \
        mri/wm.mgz \
        mri/brainmask.mgz \
        mri/aseg.mgz:colormap=lut:opacity=0.2 \
        -f \

# R ggseg

[LCBC-UiO/ggseg](https://github.com/LCBC-UiO/ggseg)

[Plotting brain atlases in ggplot](https://lcbc-uio.github.io/ggseg/articles/ggseg.html)

[Dr. Mowinckel's](https://drmowinckels.io/blog/introducing-the-ggseg-r-package-for-brain-segmentations/)