vox-diskinfo
========

Este módulo para jxcore, nodejs y derivados, está basado en https://github.com/BenoitGauthier/diskinfo 
La característica que distingue este módulo es que tiene soporte para Android con jxcore, con el comando df.


Como usar
=====

    var d = require('vox-diskinfo');

    d.getDrives(function(err, aDrives) {
  
          for (var i = 0; i < aDrives.length; i++) {
                console.log('Drive ' + aDrives[i].filesystem);
                console.log('blocks ' + aDrives[i].blocks);
                console.log('used ' + aDrives[i].used);
                console.log('available ' + aDrives[i].available);
                console.log('capacity ' + aDrives[i].capacity);
                console.log('mounted ' + aDrives[i].mounted);
                console.log('-----------------------------------------');
          }
  
    });
