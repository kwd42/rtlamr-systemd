# rtlamr-systemd
Uses systemd to autostart rtltcp and rtlamr at bootup.

/etc/systemd/system/rtltcp.service
/etc/systemd/system/rtlamr.service

  These systemd unit files will start rtl_tcp and then rtlamr at system
  startup.

/etc/default/rtlamr

  As of Sept 18, 2016 (commit: 9e258fdd9e231e2df02ccb3394572e7bf6454554),
  rtlamr can read options from environment variables. The rtlamr service 
  will read source this file for use by rtlamr.

  Update this file to customize rtlamr processing to your situation.

/etc/logrotate.d/rtlamr

  The service files will define what log and error files are written to.
  If the filenames are updated in the service files, make the assoicated
  updates here.
