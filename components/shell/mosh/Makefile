#
# CDDL HEADER START
#
# The contents of this file are subject to the terms of the
# Common Development and Distribution License (the "License").
# You may not use this file except in compliance with the License.
#
# You can obtain a copy of the license at usr/src/OPENSOLARIS.LICENSE
# or http://www.illumos.org/license/CDDL.
# See the License for the specific language governing permissions
# and limitations under the License.
#
# When distributing Covered Code, include this CDDL HEADER in each
# file and include the License file at usr/src/OPENSOLARIS.LICENSE.
# If applicable, add the following below this CDDL HEADER, with the
# fields enclosed by brackets "[]" replaced with your own identifying
# information: Portions Copyright [yyyy] [name of copyright owner]
#
# CDDL HEADER END
#
# Copyright (c) 2015, Predrag Zecevic. All rights reserved.
#
include ../../../make-rules/shared-macros.mk

COMPONENT_NAME=		mosh
COMPONENT_VERSION=	1.3.0
COMPONENT_FMRI=	service/network/mosh
COMPONENT_CLASSIFICATION=System/Security
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_PROJECT_URL=	https://mosh.mit.edu/
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_HASH=	sha256:320e12f461e55d71566597976bd9440ba6c5265fa68fbf614c6f1c8401f93376
COMPONENT_ARCHIVE_URL=	https://mosh.mit.edu/$(COMPONENT_ARCHIVE)
COMPONENT_LICENSE=      GPLv3+
COMPONENT_LICENSE_FILE=	$(COMPONENT_NAME).license 
COMPONENT_SUMMARY=	Mosh (mobile shell) - Remote terminal application that allows roaming, supports intermittent connectivity, and provides intelligent local echo and line editing of user keystrokes (replacement for SSH).

include $(WS_MAKE_RULES)/prep.mk
include $(WS_MAKE_RULES)/configure.mk
include $(WS_MAKE_RULES)/ips.mk

CONFIGURE_OPTIONS+=	--sysconfdir=/etc
CONFIGURE_OPTIONS+=	--enable-examples
CONFIGURE_OPTIONS+=	--enable-completion

build: $(BUILD_32)

install: $(INSTALL_32)

test: $(NO_TESTS)

REQUIRED_PACKAGES += utility/bash-completion 
REQUIRED_PACKAGES += library/c++/protobuf
REQUIRED_PACKAGES += library/ncurses
REQUIRED_PACKAGES += library/security/openssl
REQUIRED_PACKAGES += library/zlib
REQUIRED_PACKAGES += SUNWcs
REQUIRED_PACKAGES += system/library
REQUIRED_PACKAGES += system/library/g++-4-runtime
REQUIRED_PACKAGES += system/library/gcc-4-runtime
REQUIRED_PACKAGES += system/library/math
