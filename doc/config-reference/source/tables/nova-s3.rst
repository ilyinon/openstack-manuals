..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _nova-s3:

.. list-table:: Description of S3 configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[DEFAULT]**
     -
   * - ``buckets_path`` = ``$state_path/buckets``
     - (StrOpt) Path to S3 buckets
   * - ``image_decryption_dir`` = ``/tmp``
     - (StrOpt) Parent directory for tempdir used for image decryption
   * - ``s3_access_key`` = ``notchecked``
     - (StrOpt) Access key to use for S3 server for images
   * - ``s3_affix_tenant`` = ``False``
     - (BoolOpt) Whether to affix the tenant id to the access key when downloading from S3
   * - ``s3_host`` = ``$my_ip``
     - (StrOpt) Hostname or IP for OpenStack to use when accessing the S3 api
   * - ``s3_listen`` = ``0.0.0.0``
     - (StrOpt) IP address for S3 API to listen
   * - ``s3_listen_port`` = ``3333``
     - (IntOpt) Port for S3 API to listen
   * - ``s3_port`` = ``3333``
     - (IntOpt) Port used when accessing the S3 api
   * - ``s3_secret_key`` = ``notchecked``
     - (StrOpt) Secret key to use for S3 server for images
   * - ``s3_use_ssl`` = ``False``
     - (BoolOpt) Whether to use SSL when talking to S3