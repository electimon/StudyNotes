# fluence是什么
# 使能/禁用Fluence(sw设置)
  1. adb命令
    ro.vendor.audio.sdk.fluencetype
    adb shell setprop ro.qc.sdk.audio.fluencetype none    #设置成单MIC
    adb shell setprop ro.qc.sdk.audio.fluencetype fluence #设置成双MIC
    adb shell setprop persist.audio.fluence.voicecall true
    adb shell setprop persist.audio.fluence.voicerec true
    adb shell setprop persist.audio.fluence.speaker true
  2. 代码修改
    /device/qcom/msmxxxx/system.prop
    rc.qc.sdk.audio.fluencetype= fluencepro   # select different fluence type
    persist.audio.fluence.voicecall=true      # select true/false for your selection
    persist.audio.fluence.voicerec =false     # select true/false for your selection
    persist.audio.fluence.speaker =true       # select true/false for your selection