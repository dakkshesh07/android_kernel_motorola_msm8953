#dtb-$(CONFIG_ARCH_QCOM)	+= apq8016-sbc.dtb msm8916-mtp.dtb
#dtb-$(CONFIG_ARCH_QCOM)	+= msm8996-mtp.dtb
#dtb-$(CONFIG_ARCH_QCOM)	+= apq8096-db820c.dtb

# Add 1k of padding to the DTBs to allow for environment variables
# to be runtime added by the bootloader (i.e. /chosen properties)
DTC_FLAGS += -p 1024

ifeq ($(CONFIG_BUILD_ARM64_DT_OVERLAY),y)
$(error Motorola DTBs currently don't support overlayed mode)
endif

ifeq ($(CONFIG_POTTER_DTB),y)
dtb-$(CONFIG_ARCH_MSM8953) += msm8953-potter-p0a.dtb \
	msm8953-potter-p1a.dtb \
	msm8953-potter-p1b.dtb \
	msm8953-potter-p2a.dtb \
	msm8953-potter-p2a2.dtb \
	msm8953-potter-p2b.dtb \
	msm8953-potter-p3a.dtb
endif

always		:= $(dtb-y)
subdir-y	:= $(dts-dirs)
clean-files	:= *.dtb
