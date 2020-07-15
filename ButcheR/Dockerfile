FROM hdsu/r_tensorflow2

LABEL maintainer="Andres Quintero andres.quintero@bioquant.uni-heidelberg.de"


RUN R -e "devtools::install_github( 'hdsu-bioquant/ButcheR' )"
    
RUN R -e "BiocManager::install('DESeq2', update = FALSE)"
RUN R -e "BiocManager::install('gage', update = FALSE)"
RUN R -e "install.packages('DT')"


RUN useradd -ms /bin/bash hdsu

COPY --chown=hdsu /ButcheR/data /home/hdsu/Corces_NMF/data
COPY --chown=hdsu /ButcheR/src /home/hdsu/Corces_NMF/src
COPY --chown=hdsu /ButcheR/db /home/hdsu/Corces_NMF/db

COPY --chown=hdsu /ButcheR/user-settings /home/hdsu/.rstudio/monitored/user-settings/user-settings
COPY --chown=hdsu /ButcheR/Rprofile /home/hdsu/.Rprofile
COPY /ButcheR/user-settings /home/rstudio/.rstudio/monitored/user-settings/user-settings
COPY /ButcheR/Rprofile /home/rstudio/.Rprofile

# COPY --chown=hdsu data /home/hdsu/Corces_NMF/data
# COPY --chown=hdsu src /home/hdsu/Corces_NMF/src
# COPY --chown=hdsu db /home/hdsu/Corces_NMF/db
# COPY --chown=hdsu user-settings /home/hdsu/.rstudio/monitored/user-settings/user-settings
# COPY --chown=hdsu .Rprofile /home/hdsu/.Rprofile
# COPY .Rprofile /home/rstudio/.Rprofile
# COPY user-settings /home/rstudio/.rstudio/monitored/user-settings/user-settings


