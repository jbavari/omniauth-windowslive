# OmniAuth Windows Live

This gem contains the unofficial WindowsLive strategy for OmniAuth.

## Basic Usage

	use OmniAuth::Builder do
		provider "windowslive", ENV['WINDOWSLIVE_CLIENT_ID'], ENV['WINDOWSLIVE_SECRET'], :scope => 'wl.basic'
	end

## Supported Flows

for create app
# https://manage.dev.live.com/Applications/Index?wa=wsignin1.0 OR https://manage.dev.live.com/AddApplication.aspx?tou=1

## Ruby

Tested with the following Ruby versions:

- RUBY 1.9.3-p0
- - Ruby 2.0.0-p427
- 
The main changes for this fork is to add the following SSL fix to not verify - since the requests were failing due to SSL related issues
require 'openssl'
OpenSSL::SSL::VERIFY_PEER = OpenSSL::SSL::VERIFY_NONE
