<pre>
{
  "timestamp" : "2017-05-10T04:00:14.856Z",
  "clusters" : [ {
    "name" : "gorden2",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "612368384"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "612368384"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "4679270400"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "787"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-0-114.us-west-1.compute.internal"
        }, {
          "name" : "hive_metastore_database_name",
          "value" : "hive"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "123456"
        }, {
          "name" : "hive_metastore_database_user",
          "value" : "root"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-9a335f1a0448726ae6b78b10d0145c33",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "0e65674d-2c39-4dfc-aa65-6e33cc99a740"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-9b559241407dc4715cffc86463bb3ff6",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "d0c95a8a-c7b5-4f9a-bacb-e87e3ba1bfe2"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-b3d2790c92070f4d31a16d2ca98365bc",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0333d8a545b73caaf"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-c6937c848b6c3662a85731252f78ef51",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0139c3c1161dedf0a"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-b3d2790c92070f4d31a16d2ca98365bc",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "i-0333d8a545b73caaf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d9y6hjs3s5tlz2n03dmbb56tn"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-b3d2790c92070f4d31a16d2ca98365bc",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-0333d8a545b73caaf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bvtqtr0zh8bfe3z4fcvfedilr"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "612368384"
          } ]
        } ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-a9b571298433b6d815c981b4034022f9",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "bf1475e6-7d99-4e6f-9664-64b8871cc015"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cp5bcyfj9c82o1zenxc3an43n"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-b3d2790c92070f4d31a16d2ca98365bc",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0333d8a545b73caaf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "97pvjiv01p8y0igl8vr0z45n8"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-c6937c848b6c3662a85731252f78ef51",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0139c3c1161dedf0a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8j61ca2t81s27emvvfcpbuos8"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-0-114.us-west-1.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "123456"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "database_user",
          "value" : "root"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-c6937c848b6c3662a85731252f78ef51"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-b3d2790c92070f4d31a16d2ca98365bc",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-0333d8a545b73caaf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4yntmqmag1xp3l7i113avkldq"
          }, {
            "name" : "secret_key",
            "value" : "uLRQrz3ZNnFds585zayEIDq7pB9zIH"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-0-114.us-west-1.compute.internal"
          }, {
            "name" : "oozie_database_name",
            "value" : "ooz"
          }, {
            "name" : "oozie_database_password",
            "value" : "123456"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "root"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "612368384"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-b3d2790c92070f4d31a16d2ca98365bc",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-0333d8a545b73caaf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5lmxm45hyek4wshhnagxtwqlf"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "7"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
          } ]
        }, {
          "roleType" : "JOBHISTORY",
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "612368384"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1600"
          }, {
            "name" : "rm_io_weight",
            "value" : "800"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "3"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "1024"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "resource_manager_java_heapsize",
            "value" : "612368384"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "5250"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "80"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "AMlST6WxGSjKQ3yG0VajFdiNjsZiBI"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-GATEWAY-9a335f1a0448726ae6b78b10d0145c33",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "0e65674d-2c39-4dfc-aa65-6e33cc99a740"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-GATEWAY-9b559241407dc4715cffc86463bb3ff6",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "d0c95a8a-c7b5-4f9a-bacb-e87e3ba1bfe2"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-GATEWAY-a9b571298433b6d815c981b4034022f9",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "bf1475e6-7d99-4e6f-9664-64b8871cc015"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-GATEWAY-b3d2790c92070f4d31a16d2ca98365bc",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0333d8a545b73caaf"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-GATEWAY-c6937c848b6c3662a85731252f78ef51",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0139c3c1161dedf0a"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-JOBHISTORY-b3d2790c92070f4d31a16d2ca98365bc",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "i-0333d8a545b73caaf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "52mj4hoy2626xwtk932825ndc"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-9a335f1a0448726ae6b78b10d0145c33",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "0e65674d-2c39-4dfc-aa65-6e33cc99a740"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "57sibwns4czujil6ga7nvajz5"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-9b559241407dc4715cffc86463bb3ff6",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "d0c95a8a-c7b5-4f9a-bacb-e87e3ba1bfe2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ez9uhu452vmvzznyycckzq3kn"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-a9b571298433b6d815c981b4034022f9",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "bf1475e6-7d99-4e6f-9664-64b8871cc015"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8nmwxfltpzpwy1ff8x4g5pigx"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-b3d2790c92070f4d31a16d2ca98365bc",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0333d8a545b73caaf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3iezgec8ixb42g7kzj445q8p8"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-c6937c848b6c3662a85731252f78ef51",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0139c3c1161dedf0a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5dw3vh85z7fhkkqovr5hdmdyd"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-b3d2790c92070f4d31a16d2ca98365bc",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-0333d8a545b73caaf"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "110"
          }, {
            "name" : "role_jceks_password",
            "value" : "7m6bvyaz88ejv2z5bxjdb3ne"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "BALANCER",
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "612368384"
          } ]
        }, {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3170683699"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "400"
          }, {
            "name" : "rm_io_weight",
            "value" : "200"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "612368384"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "612368384"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "RqAsTYUAUOpj2v99ZESB9wA1vNn7kh"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "EnWWER9H9z2WELZqYBe7GJQ4cTp8yL"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "UZJnELCGY6swCfYFQQ5AY26IxpnoR1"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "20"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-b3d2790c92070f4d31a16d2ca98365bc",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "i-0333d8a545b73caaf"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-9a335f1a0448726ae6b78b10d0145c33",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "0e65674d-2c39-4dfc-aa65-6e33cc99a740"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "21kf5wfspa1vtdh1jhzwz21j"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-9b559241407dc4715cffc86463bb3ff6",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "d0c95a8a-c7b5-4f9a-bacb-e87e3ba1bfe2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e2xry5swufudtsp60ms486ywk"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-a9b571298433b6d815c981b4034022f9",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "bf1475e6-7d99-4e6f-9664-64b8871cc015"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "169gulxxgbyu17nucexdw0ge8"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-b3d2790c92070f4d31a16d2ca98365bc",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0333d8a545b73caaf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "atgtfhtgwbunvdj3gj5qxj9jr"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-c6937c848b6c3662a85731252f78ef51",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0139c3c1161dedf0a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c2j43vxhq0tt6lbbjbp9mfp3b"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-b3d2790c92070f4d31a16d2ca98365bc",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-0333d8a545b73caaf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d06j4autxv5gh3nlnc53ggnzh"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-c6937c848b6c3662a85731252f78ef51",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-0139c3c1161dedf0a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "728un38ot6onj64iegqbpcdt1"
          } ]
        }
      }, {
        "name" : "hdfs-GATEWAY-9a335f1a0448726ae6b78b10d0145c33",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "0e65674d-2c39-4dfc-aa65-6e33cc99a740"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-GATEWAY-9b559241407dc4715cffc86463bb3ff6",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "d0c95a8a-c7b5-4f9a-bacb-e87e3ba1bfe2"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-GATEWAY-a9b571298433b6d815c981b4034022f9",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "bf1475e6-7d99-4e6f-9664-64b8871cc015"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-GATEWAY-b3d2790c92070f4d31a16d2ca98365bc",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0333d8a545b73caaf"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-GATEWAY-c6937c848b6c3662a85731252f78ef51",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0139c3c1161dedf0a"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-HTTPFS-c6937c848b6c3662a85731252f78ef51",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "i-0139c3c1161dedf0a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4usk8ihigc86kcq04j94p8ekw"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-a9b571298433b6d815c981b4034022f9",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "bf1475e6-7d99-4e6f-9664-64b8871cc015"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6xd9cm6ihq905i5uec28of9oy"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-b3d2790c92070f4d31a16d2ca98365bc",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0333d8a545b73caaf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "a4m33swib8mvjpmf4l9cy7amr"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-c6937c848b6c3662a85731252f78ef51",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0139c3c1161dedf0a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c8tistp7srn710jjoc56xlplq"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-b3d2790c92070f4d31a16d2ca98365bc",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-0333d8a545b73caaf"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "112"
          }, {
            "name" : "role_jceks_password",
            "value" : "7fq0ag5jlnx504y6rvu8p7xih"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-c6937c848b6c3662a85731252f78ef51",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-0139c3c1161dedf0a"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "141"
          }, {
            "name" : "role_jceks_password",
            "value" : "as07g0qc8gb75bl8rp6r294a3"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "i-0333d8a545b73caaf",
    "ipAddress" : "172.31.0.114",
    "hostname" : "ip-172-31-0-114.us-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0139c3c1161dedf0a",
    "ipAddress" : "172.31.0.228",
    "hostname" : "ip-172-31-0-228.us-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "d0c95a8a-c7b5-4f9a-bacb-e87e3ba1bfe2",
    "ipAddress" : "172.31.10.129",
    "hostname" : "ip-172-31-10-129.us-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "0e65674d-2c39-4dfc-aa65-6e33cc99a740",
    "ipAddress" : "172.31.14.172",
    "hostname" : "ip-172-31-14-172.us-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "bf1475e6-7d99-4e6f-9664-64b8871cc015",
    "ipAddress" : "172.31.9.243",
    "hostname" : "ip-172-31-9-243.us-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-b3d2790c92070f4d31a16d2ca98365bc",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "d512bed882c8f766dc1c626dc7a8d24b65013ee1d71fe6bddf4edcdca5ff3eed",
    "pwSalt" : 6020485237471313590,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-b3d2790c92070f4d31a16d2ca98365bc",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "4cdd259f22717d65d5ed58308ca59974af2f5219a8b9ba037665a74f7d6444ff",
    "pwSalt" : -5772266252141707600,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-b3d2790c92070f4d31a16d2ca98365bc",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "f288238062471165c61b634ab51ce04cb414fe94af8a314d41f1b82daca26cd1",
    "pwSalt" : -1816970319787774446,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-b3d2790c92070f4d31a16d2ca98365bc",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "d81f9b42818762f0537d9509ea990f2bb8b527ac3ba01651e73adfcea50fa6f1",
    "pwSalt" : -249703025552458804,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "466b5088c4c2f78a8e8353e90be65de8a5db803ae5868bcef916e2ab35850aa0",
    "pwSalt" : 4308980328676419551,
    "pwLogin" : true
  }, {
    "name" : "gorden2",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "50010c0223bf2592f84f7f2eda945f692b750448cda91dd20e27c34c32d389af",
    "pwSalt" : -253198701206385666,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "d921526a58d358552176a1ee10507d7da82d3da8ed07267e7cbd4d914de3331c",
    "pwSalt" : -3408268529797637170,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.9.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170330-1814",
    "gitHash" : "822da28bff818f57fc1bfc3eafe3a550300ef1b0",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "612368384"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "612368384"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "805306368"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-0-114.us-west-1.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "123456"
        }, {
          "name" : "headlamp_database_user",
          "value" : "root"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "612368384"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "612368384"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "805306368"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-b3d2790c92070f4d31a16d2ca98365bc",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-0333d8a545b73caaf"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "3ehhhwslkijy2svst66hhda9e"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-b3d2790c92070f4d31a16d2ca98365bc",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-0333d8a545b73caaf"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "c56yx2xzxjbi4hkee5p9gg3dv"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-b3d2790c92070f4d31a16d2ca98365bc",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-0333d8a545b73caaf"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "e1izouc06f7puw4rcpyqmyj7o"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-b3d2790c92070f4d31a16d2ca98365bc",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-0333d8a545b73caaf"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "242suhskac6859kgjrr47r3mv"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-b3d2790c92070f4d31a16d2ca98365bc",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-0333d8a545b73caaf"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "28utvht8cuws14yxl5cuobjng"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/24/2012 12:10"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}
</pre>