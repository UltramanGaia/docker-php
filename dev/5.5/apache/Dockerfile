FROM chialab/php:5.5-apache
LABEL maintainer="dev@chialab.io"

# Install XDebug.
RUN pecl install xdebug-2.5.5 \
    && echo "zend_extension=\"$(php-config --extension-dir)/xdebug.so\"\n\
xdebug.show_execption_trace = On\n\
xdebug.show_local_vars = On\n\
xdebug.remote_autostart = On\n\
xdebug.remote_enable = On\n\
xdebug.remote_connect_back = 1\n\
xdebug.collect_vars = On\n\
xdebug.collect_params = On\n\
xdebug.remote_handler = "dbgp"\n\
xdebug.idekey = PHPSTORM\n\
xdebug.remote_port = 9000\n\
xdebug.remote_host = 0.0.0.0\n\
" > $PHP_INI_DIR/conf.d/xdebug.ini
