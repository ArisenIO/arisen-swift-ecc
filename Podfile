using_local_pods = ENV['USE_LOCAL_PODS'] == 'true' || false

platform :ios, '11.0'

# ignore all warnings from all pods
inhibit_all_warnings!

if using_local_pods
  # Pull pods from sibling directories if using local pods
  target 'ArisenSwiftEcc' do
    use_frameworks!

    target 'ArisenSwiftEccTests' do
      inherit! :search_paths
      pod 'GRKOpenSSLFramework', '1.0.2.19'
      pod 'ArisenSwift', :path => '../arisen-swift'
    end

    pod 'GRKOpenSSLFramework', '1.0.2.19'
    pod 'ArisenSwift', :path => '../arisen-swift'
    pod 'SwiftLint'
  end
else
  # Pull pods from sources above if not using local pods
    target 'ArisenSwiftEcc' do
    use_frameworks!

    target 'ArisenSwiftEccTests' do
      inherit! :search_paths
      pod 'GRKOpenSSLFramework', '1.0.2.19'
      pod 'ArisenSwift', '~> 0.2.1'
    end

    pod 'GRKOpenSSLFramework', '1.0.2.19'
    pod 'ArisenSwift', '~> 0.2.1'
    pod 'SwiftLint'
  end
end
