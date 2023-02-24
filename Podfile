# Uncomment the next line to define a global platform for your project
platform :ios, '11.0'
plugin 'cocoapods-binary'
use_frameworks!(:linkage => :static)

target 'dsbridge' do
  
end

target 'dsbridgedemo' do
  pod 'AFNetworking',"3.0",:binary => true
  pod 'Masonry',:binary => true
  pod 'YYCategories',:binary => true
#  pod 'BlocksKit',:binary => true
#  pod 'YYModel',:binary => true
#  pod 'FTPopOverMenu',:binary => true
#  pod 'MBProgressHUD', '1.2.0' ,:binary => true
  pod 'LBXScan/LBXNative','~> 2.5',:binary => true
  pod 'SAMKeychain','1.5.3'
  pod 'MJRefresh'
  pod 'ReactiveObjC',:binary => true
  pod 'YYCache',:binary => true
  pod 'DZNEmptyDataSet', '~> 1.8.1',:binary => true
  pod 'INTULocationManager',:binary => true
  pod 'SSZipArchive','2.4.3',:binary=> true
  pod 'Aspects'
  pod 'DeviceUtil'

  pod 'ijkplayerssl'

  pod 'UMCommon', '~> 7.2.5'
  pod 'UMDevice'
  pod 'UMCCommonLog', :configurations => ['Debug']   # UMCCommonLog 友盟开发阶段调试
  pod 'PromisesObjC',:binary => true
 pod 'XLPagerTabStripOC',:git => 'https://github.com/pencilCool/XLPagerTabStrip',:commit=>'bafd2b8c0'#  :branch => 'obj-c'
#
  pod 'XLPagerTabStrip', '~> 9.0'

#  pod 'TYHWaterMark','0.1.1'

  pod 'CocoaLumberjack', '~> 3.2.1'#,:binary => true

  pod 'BaiduTraceKit-Lite','3.1.3'

  pod 'BMKLocationKit', '1.8.0'
  pod 'BaiduNaviKit', '6.0.0'# 集成Navi包
  pod 'BaiduNaviKit/Search', '6.0.0' # 集成地图Search包
  pod 'BaiduNaviKit/Utils', '6.0.0'# 集成地图Utils包
  pod 'BaiduNaviKit/TTS', '6.0.0' # 集成地图Utils包

end

# fix xcode14 bug
# https://stackoverflow.com/questions/72561696/xcode-14-needs-selected-development-team-for-pod-bundles
post_install do |installer|
  installer.generated_projects.each do |project|
    project.targets.each do |target|
        target.build_configurations.each do |config|
            config.build_settings['CODE_SIGNING_ALLOWED'] = 'NO'
         end
    end
  end
end
