#
# Podfile
# mas-cli
#

platform :osx, '10.9'

target 'mas' do
  pod 'Commandant', '~> 0.15'
end

target 'MasKit' do
  # Building swift pods statically since executable doesn't have a bundle.
  # use_frameworks!
  use_modular_headers!

  pod 'Commandant', '~> 0.15'
  pod 'Result'

  target 'MasKitTests' do
    platform :osx, '10.11'
    inherit! :search_paths

    pod 'Quick'
    pod 'Nimble'
  end
end

# https://stackoverflow.com/questions/50922311/workspace-warning-target-pods-cannot-link-framework-foundation-framework/51052908
# post_install do |installer|
#     podsTargets = installer.pods_project.targets.find_all { |target| target.name.start_with?('Pods') }
#     podsTargets.each do |target|
#         target.frameworks_build_phase.clear
#     end
# end
