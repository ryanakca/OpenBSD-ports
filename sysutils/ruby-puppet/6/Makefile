PORTROACH=		limit:^6

VERSION=		6.28.0
REVISION=		3

RUN_DEPENDS+=		converters/ruby-multi_json,${MODRUBY_FLAVOR}>=1.10,<2 \
			databases/ruby-hiera3,${MODRUBY_FLAVOR} \
			devel/ruby-gettext-setup,${MODRUBY_FLAVOR}>=0.28,<1 \
			devel/ruby-locale,${MODRUBY_FLAVOR}>=2.1,<3 \
			devel/ruby-rgen,${MODRUBY_FLAVOR} \
			devel/ruby-concurrent-ruby,${MODRUBY_FLAVOR} \
			devel/ruby-puppet-resource_api,${MODRUBY_FLAVOR} \
			devel/ruby-semantic_puppet,${MODRUBY_FLAVOR} \
			sysutils/ruby-facter,${MODRUBY_FLAVOR} \
			www/ruby-httpclient,${MODRUBY_FLAVOR}

pre-configure:
	${SUBST_CMD} ${WRKDIST}/lib/puppet/provider/package/gem.rb \
		${WRKDIST}/lib/puppet/provider/package/pip.rb \
		${WRKDIST}/lib/puppet/provider/package/pip3.rb \
		${WRKDIST}/lib/puppet/provider/package/gem.rb \
		${WRKSRC}/lib/puppet/reference/configuration.rb \
		${WRKSRC}/lib/puppet/util/run_mode.rb \
		${WRKSRC}/lib/puppet/defaults.rb

.include <bsd.port.mk>
