# utl_line_printer_horizontal_bar_charts
Line printer horizontal bar charts.  Keywords: sas sql join merge big data analytics macros oracle teradata mysql sas communities stackoverflow statistics artificial inteligence AI Python R Java Javascript WPS Matlab SPSS Scala Perl C C# Excel MS Access JSON graphics maps NLP natural language processing machine learning igraph DOSUBL DOW loop stackoverflow SAS community.
    Line printer horizontal bar (maybe an alternative to SG graphics)

    Line printer horizontal bar charts (looks much better when you zoom to 100% or print it

    https://goo.gl/WsDESq
    https://github.com/rogerjdeangelis/utl_line_printer_horizontal_bar_charts/blob/master/utl_line_printer_horizontal_bar_charts.pdf

    github project
    https://github.com/rogerjdeangelis/utl_line_printer_horizontal_bar_charts

    I find line printer plots sometimes superior to SG graphics.
    In addition you have a great graphics editor.


    INPUT
    =====

     WORK.HAVE total obs=102

       STATE    VAGINALMEDIAN     AGE

        AK         9681.28       -Adult
        AK         9883.28       Minor
        AL         4884.44       -Adult
        AL         5258.44       Minor
        AR         5524.18       -Adult
        AR         6020.18       Minor
        AZ         6806.76       -Adult
        AZ         7342.76       Minor
        CA         7001.03       -Adult
       ...

    PROCESS
    =======

        options  leftmargin=.5in rightmargin=.5in orientation=portrait nocenter;
        ods pdf file='d:/pdf/utl_line_printer_horizontal_bar_charts.pdf' style=printer;
        options ls=132;
        proc chart data=have;
           format VaginalMedian dollar9.;
           hbar state  /sumvar = VaginalMedian subgroup=age descending ;
        run;quit;
        ods pdf close;

    OUTPUT
    ======

                                                                                           Sum
    STATE                                                                     Median Costs of Vaginal Delivery

         |
    AK   |-------------------------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM       $21,565
    NJ   |-----------------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM                     $18,096
    NY   |----------------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM                       $17,357
    WI   |---------------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM                          $16,753
    MA   |--------------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM                           $16,408
    CT   |--------------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM                            $16,090
    ND   |-----------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM                                $15,173
    FL   |------------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM                                $15,093
    IL   |------------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMMMM                                 $15,045
    CA   |----------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMMMM                                   $14,414
    NV   |----------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMMMM                                   $14,353
    TX   |----------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMMM                                    $14,277
    WY   |----------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMMM                                    $14,200
    AZ   |---------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMMM                                     $14,150
    CO   |---------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMMM                                     $13,844
    OR   |---------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMM                                      $13,778
    GA   |---------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMM                                      $13,766
    PA   |--------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMM                                       $13,652
    TN   |---------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMM                                      $13,579
    DC   |--------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMM                                       $13,547
    WA   |--------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMMM                                       $13,415
    VA   |--------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMM                                        $13,337
    MD   |--------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMM                                        $13,287
    VT   |--------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMM                                        $13,238
    IN   |-------------------------MMMMMMMMMMMMMMMMMMMMMMMMMMM                                         $13,125
    NC   |--------------------------MMMMMMMMMMMMMMMMMMMMMMMMMM                                         $12,962
    SC   |-------------------------MMMMMMMMMMMMMMMMMMMMMMMMMM                                          $12,624
    SD   |------------------------MMMMMMMMMMMMMMMMMMMMMMMMMM                                           $12,605
    OK   |------------------------MMMMMMMMMMMMMMMMMMMMMMMMMM                                           $12,556
    MI   |------------------------MMMMMMMMMMMMMMMMMMMMMMMMMM                                           $12,537
    NH   |-------------------------MMMMMMMMMMMMMMMMMMMMMMMMM                                           $12,536
    MT   |------------------------MMMMMMMMMMMMMMMMMMMMMMMMMM                                           $12,534
    MN   |------------------------MMMMMMMMMMMMMMMMMMMMMMMMMM                                           $12,440
    DE   |------------------------MMMMMMMMMMMMMMMMMMMMMMMMMM                                           $12,386
    ME   |------------------------MMMMMMMMMMMMMMMMMMMMMMMMMM                                           $12,344
    NM   |-----------------------MMMMMMMMMMMMMMMMMMMMMMMMM                                             $12,164
    MO   |------------------------MMMMMMMMMMMMMMMMMMMMMMMMM                                            $12,098
    OH   |-----------------------MMMMMMMMMMMMMMMMMMMMMMMMM                                             $11,978
    ID   |-----------------------MMMMMMMMMMMMMMMMMMMMMMMMM                                             $11,972
    WV   |-----------------------MMMMMMMMMMMMMMMMMMMMMMMMM                                             $11,971
    IA   |-----------------------MMMMMMMMMMMMMMMMMMMMMMMMM                                             $11,808
    KY   |-----------------------MMMMMMMMMMMMMMMMMMMMMMMM                                              $11,699
    AR   |----------------------MMMMMMMMMMMMMMMMMMMMMMMM                                               $11,544
    MS   |-----------------------MMMMMMMMMMMMMMMMMMMMMMM                                               $11,516
    HI   |----------------------MMMMMMMMMMMMMMMMMMMMMMMM                                               $11,513
    KS   |----------------------MMMMMMMMMMMMMMMMMMMMMMMM                                               $11,490
    LA   |----------------------MMMMMMMMMMMMMMMMMMMMMMM                                                $11,257
    UT   |----------------------MMMMMMMMMMMMMMMMMMMMMMM                                                $11,193
    NE   |---------------------MMMMMMMMMMMMMMMMMMMMMM                                                  $10,725
    AL   |--------------------MMMMMMMMMMMMMMMMMMMMM                                                    $10,143
    RI   |--------------------MMMMMMMMMMMMMMMMMMMM                                                     $10,095
         |
         --------+-------+-------+-------+-------+-------+-------+-------+-------+-------+------
               $2,000  $4,000  $6,000  $8,000 $10,000 $12,000 $14,000 $16,000 $18,000 $20,000

                                     Median Cost of Vaginal Delivery

    Symbol AGE        Symbol AGE

       -   -Adult        M   MMinor

    *                _              _       _
     _ __ ___   __ _| | _____    __| | __ _| |_ __ _
    | '_ ` _ \ / _` | |/ / _ \  / _` |/ _` | __/ _` |
    | | | | | | (_| |   <  __/ | (_| | (_| | || (_| |
    |_| |_| |_|\__,_|_|\_\___|  \__,_|\__,_|\__\__,_|

    ;

    data have;
      length State $2;

      input State VaginalMedian;
      label VaginalMedian = "Median Cost of Vaginal Delivery";
      age="-Adult";
      output;
      age="+Minor";
      VaginalMedian=VaginalMedian + 100 + int(500*uniform(5732));
      output;
    cards4;
    AK 9681.28
    AL 4884.44
    AR 5524.18
    AZ 6806.76
    CA 7001.03
    CO 6648.17
    CT 7906.21
    DE 5978.86
    FL 7391.90
    GA 6693.32
    HI 5622.85
    IA 5647.90
    ID 5772.21
    IL 7447.68
    IN 6347.41
    KS 5566.41
    KY 5647.04
    LA 5409.55
    MA 7949.91
    MD 6508.44
    ME 5879.74
    MI 5978.05
    MN 6011.99
    MO 5904.83
    MS 5651.97
    MT 6101.17
    NC 6407.91
    ND 7294.10
    NE 5223.61
    NH 6207.80
    NJ 8755.88
    NM 5819.31
    NV 6947.47
    NY 8449.33
    OH 5705.76
    OK 6057.96
    OR 6725.62
    PA 6535.24
    RI 4987.38
    SC 6141.69
    SD 6121.19
    TN 6696.51
    TX 6923.48
    UT 5454.84
    VA 6493.98
    VT 6502.27
    WA 6408.83
    WI 8278.86
    WV 5717.18
    WY 7018.03
    DC 6613.82
    ;;;;;
    run;quit;

    *          _       _   _
     ___  ___ | |_   _| |_(_) ___  _ __
    / __|/ _ \| | | | | __| |/ _ \| '_ \
    \__ \ (_) | | |_| | |_| | (_) | | | |
    |___/\___/|_|\__,_|\__|_|\___/|_| |_|

    ;

    options  leftmargin=.5in rightmargin=.5in orientation=portrait nocenter;
    ods pdf file="d:/pdf/utl_line_printer_horizontal_bar_charts.pdf" style=printer;
    options ls=132;
    proc chart data=have;
       format VaginalMedian dollar9.;
       hbar state  /sumvar = VaginalMedian subgroup=age descending ;
    run;quit;
    ods pdf close;
    run;quit;

