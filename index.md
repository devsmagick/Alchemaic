<!doctype html><html xmlns=http://www.w3.org/1999/xhtml xml:lang=en-US lang=en-us prefix="og: http://ogp.me/ns#">
<head>
<meta charset=utf-8>
<title>Signing commits with GPG | GitLab</title>
<meta property=og:title content="Signing commits with GPG | GitLab">
<meta name=description property=og:description content="Documentation for GitLab Community Edition, GitLab Enterprise Edition, Omnibus GitLab, and GitLab Runner.">
<meta name=viewport content="width=device-width,initial-scale=1,user-scalable=no">
<meta name=docsearch:language content=en>
<meta name=docsearch:version content=main>
<meta http-equiv=content-security-policy content="default-src 'self' https:; script-src 'self' 'unsafe-inline' 'unsafe-eval' https:; style-src 'self' 'unsafe-inline' https:; object-src 'none'; base-uri 'self'; connect-src 'self' https:; frame-src 'self' https:; img-src 'self' https: data:; manifest-src 'self'; media-src 'self'; worker-src 'none';">
<link rel=stylesheet href=https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css integrity=sha384-JcKb8q3iqJ61gNV9KGb8thSsNjpSL0n8PARn9HuZOnIxN0hoP+VmmDGMN5t9UJ0Z crossorigin=anonymous>
<link rel=stylesheet href=/assets/stylesheets/stylesheet-v112.css>
<link rel=stylesheet href=/assets/stylesheets/highlight-v8.css>
<link rel=stylesheet href=/assets/stylesheets/footer-v10.css>
<link rel=stylesheet href=/assets/stylesheets/toc-v20.css>
<link rel=stylesheet href=/assets/stylesheets/help-v6.css>
<link rel=stylesheet href=https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css>
<link rel=stylesheet href=https://cdn.jsdelivr.net/npm/docsearch.js@2/dist/cdn/docsearch.min.css>
<script id=Cookiebot src=https://consent.cookiebot.com/uc.js data-cbid=36a06ac5-ddb4-4f91-8337-067ad19ad8d5></script>
<script src=/assets/javascripts/google_tagmanager-v1.js></script>
<meta name=google-site-verification content=6eFQOFLxYAer08ROqc3I-SAi44F9NmvH7PrUUBR3oCI>
<meta name=google-site-verification content=xAUTWp3CDg-tU1LVVwsM9OrVhLR7L3SmiyKzkOuPNos>
<meta name=google-site-verification content=F0zzwaMpiyWFcPQ1Lqu18qN3EnuQsqFXbySl_29yvHs>
<meta name=google-site-verification content=nwo1bVaU0t9TZxZyM-aOI6-CofaH9GRL-uBPbdREWgc>
<meta name=google-site-verification content=rWoHrtHEmIX0t28oOb1ZEDMYZb_EZA6rr6ZOl5otEPI>
<meta name=google-site-verification content=fSxr8-uslxcuFL0N-oECp3Tm0RPNEGX97wbdayKOEL8>
<script async src=https://cdn.jsdelivr.net/npm/eligrey-classlist-js-polyfill@1.2.20180112/classList.min.js integrity="sha256-idm3p7jl0XwymUpIccg6WI96tQmoDR/5DWEsnPnxYU4=" crossorigin=anonymous></script>
<script async src=/assets/javascripts/closest-polyfill-v.js></script>
<meta name=generator content="Nanoc 4.12.1">
<link href=/opensearch.xml rel=search title="Search through GitLab Docs" type=application/opensearchdescription+xml>
<link rel=apple-touch-icon sizes=180x180 href=/assets/images/apple-touch-icon.png>
<link rel=manifest href=/assets/manifests/site.webmanifest>
<meta name=msapplication-config content=/assets/manifests/browserconfig.xml>
<meta name=msapplication-TileColor content=#FC6D26>
<meta name=theme-color content=#FC6D26>
<link rel=canonical href=https://docs.gitlab.com/ee/user/project/repository/gpg_signed_commits/>
<meta property=og:url content=https://docs.gitlab.com/ee/user/project/repository/gpg_signed_commits/>
</head>
<body class=gl-docs itemscope itemtype=http://schema.org/WebPage data-spy=scroll data-target=#doc-nav data-offset=90>
<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-WZCXKT5" height=0 width=0 style=display:none;visibility:hidden></iframe></noscript>
<nav class="navbar navbar-expand-md navbar-dark fixed-top py-lg-0">
<a class="navbar-brand d-flex align-items-center justify-content-center" href=/>
<img src=/assets/images/gitlab-logo.svg alt="GitLab documentation home" class=logo>
<span class="d-none d-lg-block px-2">GitLab</span> <strong class="pl-2 pl-lg-0 pt-0">Docs</strong>
</a>
<button class=navbar-toggler type=button data-toggle=collapse data-target=#navbarSupportedContent aria-controls=navbarSupportedContent aria-expanded=false aria-label="Toggle navigation">
<span class=navbar-toggler-icon></span>
</button>
<div class="collapse navbar-collapse" id=navbarSupportedContent>
<ul class="navbar-nav mr-auto mb-0">
<li class="nav-item active">
<form class="form-inline my-2 my-lg-0" id=search-form action=/search/>
<span class="fa fa-search form-control-feedback position-absolute ml-3 text-muted"></span>
<input class="form-control mr-sm-2 docsearch border-0" name=query type=search placeholder="Search the docs..." aria-label=Search>
<input type=submit style=visibility:hidden;position:absolute>
</form>
</ul>
<ul class="navbar-nav mb-0">
<li class="nav-item p-2 dropdown">
<button class="btn dropdown-toggle text-white" type=button id=navbarDropdown data-toggle=dropdown aria-haspopup=true aria-expanded=false>
GitLab.com (14.0-pre)
</button>
<div class=dropdown-menu aria-labelledby=navbarDropdown>
<a class=dropdown-item class=active href=/ee/user/project/repository/gpg_signed_commits/index.html class=versions-tooltip>GitLab.com (14.0-pre)
<i class="fa fa-question-circle-o" aria-hidden=true data-toggle=tooltip data-placement=bottom title="Latest pre-release version of GitLab, with features available or about to become available on GitLab.com. For self-managed GitLab installations, select your version number as listed at your GitLab instance's /help URL."></i>
</a>
<div class=dropdown-divider></div>
<a class=dropdown-item href=/13.12/ee/user/project/repository/gpg_signed_commits/index.html>
13.12
</a>
<a class=dropdown-item href=/13.11/ee/user/project/repository/gpg_signed_commits/index.html>
13.11
</a>
<a class=dropdown-item href=/13.10/ee/user/project/repository/gpg_signed_commits/index.html>
13.10
</a>
<div class=dropdown-divider></div>
<a class=dropdown-item href=/12.10/ee/user/project/repository/gpg_signed_commits/index.html>
12.10
</a>
<a class=dropdown-item href=/11.11/ee/user/project/repository/gpg_signed_commits/index.html>
11.11
</a>
<div class=dropdown-divider></div>
<a class=dropdown-item href=/archives/>Archives</a>
</div>
<li class="nav-item p-2">
<a class="btn btn-danger btn-cta text-white" href=https://about.gitlab.com/free-trial/ target=_blank rel="noopener noreferrer" role=button>
Get free trial
</a>
</ul>
</div>
</nav>
<section class="container-fluid pt-5">
<div class=row>
<div class="col-0 col-lg-2 pl-0">
<div class="nav-wrapper active">
<aside id=global-nav class=global-nav>
<nav class=global-nav-content>
<div class=global-nav-section>
<span class="global-nav-block-top nav-link">
<a class="global-nav-link level-0" href=/ee/README.html>
GitLab Docs
</a>
<div class="section-title  collapsed" data-toggle=collapse aria-expanded=false data-target=#sec_246dee77-b5f1-4a77-954a-a8951192b770></div>
</span>
</div>
<div class=global-nav-section>
<span class="global-nav-block-top nav-link">
<a class="global-nav-link level-0 has-collapse" href=/ee/subscriptions/>
Choose a subscription
</a>
<div class="section-title collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#sec_f6ff2811-a356-4765-a23a-52f08a2c5308></div>
</span>
<div class=collapse id=sec_f6ff2811-a356-4765-a23a-52f08a2c5308>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/subscriptions/gitlab_com/>
GitLab.com subscriptions
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_a34e4753-5caa-4625-b902-851beb344955></div>
</span>
<div class=collapse id=cat_a34e4753-5caa-4625-b902-851beb344955>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/usage_quotas.html>
Storage usage quota
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_800240e8-82ff-4d76-95c1-2909e55cc449></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/subscriptions/self_managed/>
Self-managed subscriptions
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_206b557a-ae3b-4206-9e4c-5c82906f720b></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/user/admin_area/license.html>
Activate Enterprise Edition
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_5c32166f-e092-4bd9-aa12-305377cfc5c7></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/subscriptions/bronze_starter.html>
Features available to Starter and Bronze subscribers
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_61ddd8d6-93cf-48fb-ba3b-486dd2592e86></div>
</span>
</div>
</div>
<div class=global-nav-section>
<span class="global-nav-block-top nav-link">
<a class="global-nav-link level-0 has-collapse" href=/ee/install/>
Install GitLab
</a>
<div class="section-title collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#sec_2118b8fc-0379-46ef-aadd-cd8fd94626e2></div>
</span>
<div class=collapse id=sec_2118b8fc-0379-46ef-aadd-cd8fd94626e2>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/install/requirements.html>
Requirements
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_84699003-244b-4044-909e-12ccbe6c93d9></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/install/>
Installation methods
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_25d5eb85-d291-42ab-b84e-43425e38cda3></div>
</span>
<div class=collapse id=cat_25d5eb85-d291-42ab-b84e-43425e38cda3>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/omnibus/README.html>
Linux packages (Omnibus)
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_84a2b528-3759-4d6a-8a94-f582d9b2a5d7></div>
</span>
<div class=collapse id=doc_84a2b528-3759-4d6a-8a94-f582d9b2a5d7>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/omnibus/architecture/README.html>
Architecture
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_28fa3671-97c0-46b2-8c1a-f0b8f4ff04fb></div>
</span>
<div class=collapse id=doc_28fa3671-97c0-46b2-8c1a-f0b8f4ff04fb>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/package-information/omnibus_packages.html>
Omnibus packages and images
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/package-information/README.html>
Package information
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/package-information/defaults.html>
Package defaults
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/package-information/licensing.html>
Package licensing
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/package-information/signed_packages.html>
Package signatures
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/omnibus/installation/>
Installation
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_3911f71c-49b0-4dc6-9c1f-eb4805a49590></div>
</span>
<div class=collapse id=doc_3911f71c-49b0-4dc6-9c1f-eb4805a49590>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/architecture/registry/README.html>
Container Registry
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/package-information/deprecation_policy.html>
Deprecation policy
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/package-information/deprecated_os.html>
Deprecated OSes
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/docker/README.html>
Docker images
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/manual_install.html>
Manual installation
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/jihu_edition.html>
Install JiHu Edition
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/omnibus/settings/README.html>
Configure
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_7cb9d104-3f43-46dc-8d68-9136dd984ffe></div>
</span>
<div class=collapse id=doc_7cb9d104-3f43-46dc-8d68-9136dd984ffe>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/settings/environment-variables.html>
Custom environment variables
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/settings/backups.html>
Backups
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/settings/database.html>
Database
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/gitlab-mattermost/README.html>
GitLab Mattermost
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/settings/grafana.html>
Grafana
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/roles/README.html>
High availability roles
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/administration/auth/ldap/>
LDAP
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/settings/logs.html>
Logs
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/settings/nginx.html>
NGINX
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/settings/praefect.html>
Gitaly Cluster
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/settings/prometheus.html>
Prometheus
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/settings/puma.html>
Puma
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/settings/rpi.html>
Raspberry Pi
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/settings/redis.html>
Redis
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/settings/smtp.html>
SMTP
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/settings/ssl.html>
SSL
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/settings/dns.html>
DNS
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/settings/unicorn.html>
Unicorn
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/settings/image_scaling.html>
Image scaling
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/settings/memory_constrained_envs.html>
Memory-constrained environments
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/omnibus/release/README.html>
Release process
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_a02e9153-5d97-4dfa-802b-a097d7576584></div>
</span>
<div class=collapse id=doc_a02e9153-5d97-4dfa-802b-a097d7576584>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/release/openshift.html>
OpenShift release process
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/omnibus/update/README.html>
Update
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_0c6b1d54-1b6e-425e-b7ba-1a62ce2e65fd></div>
</span>
<div class=collapse id=doc_0c6b1d54-1b6e-425e-b7ba-1a62ce2e65fd>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/update/convert_to_omnibus.html>
Convert to Omnibus
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/update/package_signatures.html>
Package signatures
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/update/gitlab_13_changes.html>
GitLab 13 changes
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/update/gitlab_12_changes.html>
GitLab 12 changes
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/update/gitlab_11_changes.html>
GitLab 11 changes
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/omnibus/update/gitlab_10_changes.html>
GitLab 10 changes
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3" href=/omnibus/maintenance/README.html>
Maintain
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_53932738-de2e-452e-b0ee-dda0aa5e029c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/omnibus/common_installation_problems/README.html>
Troubleshoot
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a369f071-cce3-4f7a-aa08-8bec17cefabd></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/charts/>
Kubernetes
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_e2036ae7-11a7-4542-b090-669e8c38a5e3></div>
</span>
<div class=collapse id=doc_e2036ae7-11a7-4542-b090-669e8c38a5e3>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/charts/installation/>
Install
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_28f4a980-bda7-4a6d-ae72-e356f42aee1f></div>
</span>
<div class=collapse id=doc_28f4a980-bda7-4a6d-ae72-e356f42aee1f>
<span class=nav-link>
<a class="global-nav-link level-4" href=/charts/installation/tools.html>
Required tools
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/charts/installation/cloud/>
Cloud cluster preparation
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/charts/installation/deployment.html>
Deploy
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/charts/installation/upgrade.html>
Upgrade
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/charts/backup-restore/>
Backup and Restore
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/charts/installation/migration/>
Migrate from Omnibus
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/charts/installation/version_mappings.html>
Version mappings
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/charts/charts/>
Configure
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_ecc27a19-2f1b-47de-a4b2-f40a8592536f></div>
</span>
<div class=collapse id=doc_ecc27a19-2f1b-47de-a4b2-f40a8592536f>
<span class=nav-link>
<a class="global-nav-link level-4" href=/charts/charts/globals.html>
Globals
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/charts/charts/gitlab/>
GitLab sub-charts
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/charts/charts/minio/>
Minio chart
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/charts/charts/nginx/>
Nginx chart
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/charts/installation/deployment.html#redis>
Redis chart
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/charts/installation/deployment.html#redis>
Redis HA chart
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/charts/charts/registry/>
Registry chart
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/charts/advanced/>
Advanced
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3" href=/charts/troubleshooting/>
Troubleshoot
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_dc07e1ca-b988-4742-bb20-cec9ef47300c></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/install/docker.html>
Docker
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d3d4d080-f453-4d5c-af91-cbc7c0b2dd8b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/install/installation.html>
From source
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9a416d4c-d889-4174-a0e8-48be10743ceb></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/install/#install-gitlab-on-cloud-providers>
Cloud providers guides
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_9d2dadc7-54bb-4bd5-8013-eb6bcef390d5></div>
</span>
<div class=collapse id=cat_9d2dadc7-54bb-4bd5-8013-eb6bcef390d5>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/install/azure/>
Azure
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d6186269-b07f-45a1-a722-053a4f58cd0d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/install/google_cloud_platform/>
Google Cloud Platform (GCP)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_601015b7-eb6a-40a6-97de-9bae3d1bc5b6></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/install/aws/>
Amazon Web Services (AWS)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_086ab9ef-372c-4905-90a1-8d1bd506cbd8></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/administration/reference_architectures/>
Reference Architectures
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_78594472-f23f-4310-b5a7-59d642c7c38e></div>
</span>
<div class=collapse id=cat_78594472-f23f-4310-b5a7-59d642c7c38e>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/reference_architectures/1k_users.html>
Up to 1,000 users
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_41b2402f-983c-42f2-af8d-631793e89a2d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/reference_architectures/2k_users.html>
Up to 2,000 users
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0ae360db-b2fb-4c77-aa69-9f6f07e6c146></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/reference_architectures/3k_users.html>
Up to 3,000 users
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ca10d479-6e65-45f4-8344-8d58a3577f8d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/reference_architectures/5k_users.html>
Up to 5,000 users
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0d72b7ef-5d39-4564-b5fc-1a0a1099b25c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/reference_architectures/10k_users.html>
Up to 10,000 users
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d1bce2af-3b10-4c7e-a097-4be766f93092></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/reference_architectures/25k_users.html>
Up to 25,000 users
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6a98e5b0-ad5f-428e-bb86-63e10447eb36></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/reference_architectures/50k_users.html>
Up to 50,000 users
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9e536dd9-7f1e-4673-a65c-a248c7f5cd47></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/reference_architectures/troubleshooting.html>
Troubleshooting
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7a24091b-6695-4112-a887-cb19f3edddab></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/install/next_steps.html>
Steps after installing
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_67706309-5aa1-4397-8540-d69041c29137></div>
</span>
</div>
</div>
<div class=global-nav-section>
<span class="global-nav-block-top nav-link">
<a class="global-nav-link level-0 has-collapse" href=/ee/integration/>
Integrate applications
</a>
<div class="section-title collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#sec_94ec7bce-f589-4a0c-9cce-dc345b77dbbc></div>
</span>
<div class=collapse id=sec_94ec7bce-f589-4a0c-9cce-dc345b77dbbc>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/integration/akismet.html>
Akismet
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_e812a224-24a4-4735-84c0-b38305cf1eff></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/integration/elasticsearch.html>
Elasticsearch
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_fec9d876-2cf3-483f-9b5c-7e43c057465f></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/integration/gitpod.html>
Gitpod
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_1a5c72c4-edc1-4e1c-a649-d79c6db3bfe4></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/integration/jira/>
Jira integrations
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_6772ef56-ec52-4d1b-86b4-8ed5fb1bd7ae></div>
</span>
<div class=collapse id=cat_6772ef56-ec52-4d1b-86b4-8ed5fb1bd7ae>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/jira/connect-app.html>
GitLab for Jira app
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9d3301a8-7e77-4efe-a3b2-d5bfec6d4df1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/jira/dvcs.html>
Jira DVCS connector
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7f6bb84a-7928-498f-b4b4-c15b1f4433fc></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/jira/development_panel.html>
Jira Development Panel
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6159d617-f97d-4628-b3e0-20c7ac893563></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/jira/jira_server_configuration.html>
Create Jira Server user
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9005575c-2a52-4b3c-ba94-164a3648d4f1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/jira/jira_cloud_configuration.html>
Create Jira Cloud API token
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_21149444-b46d-42aa-9880-bb867af25b4b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/jira/issues.html>
Jira integration issue management
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_fd14448e-796c-4464-bea3-38523b424d87></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/integration/kroki.html>
Kroki diagrams
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_bf7a8d06-d33d-49ed-bd55-5a1ad5f7320e></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/integration/plantuml.html>
PlantUML
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_29c4a26b-855f-420e-8d08-0dfb1a9d16b8></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/user/admin_area/settings/project_integration_management.html>
Project integration management
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_f2b9750e-f409-4ad1-b457-28ddc090a79e></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/user/project/integrations/>
Project integrations
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_7bceace8-28d9-4465-b261-10a2c6b386d6></div>
</span>
<div class=collapse id=cat_7bceace8-28d9-4465-b261-10a2c6b386d6>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/overview.html>
Overview
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f09e437b-e21e-4139-8f96-8e66f035e306></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/asana.html>
Asana
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_15f08cc7-71a8-4769-89d5-1b4990d4979f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/bamboo.html>
Bamboo CI
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_89da6ef6-77f5-4ae7-bb0c-29194f14e479></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/discord_notifications.html>
Discord
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_38e7949b-9edc-465a-8e63-12fc8e3bdf19></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/emails_on_push.html>
Emails on push
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_62988538-bcbc-4684-ac34-2681eb65b226></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/github.html>
GitHub
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7b4bfecf-27de-4b90-b175-9f2661b75794></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/hangouts_chat.html>
Google Chat
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a8d64df7-1f2b-447d-8d69-0451cd889f9c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/irker.html>
Irker
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_fb61a0b4-7304-4da3-bdb1-a4e75f4ec88d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/jenkins.html>
Jenkins
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_56993362-9bfc-45a7-80d2-56da566e053b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/jenkins_deprecated.html>
Jenkins (deprecated)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b27b7e68-df79-4f9f-a532-2b0b4c5fa50f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/mattermost.html>
Mattermost notifications
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a0596199-bf74-4c68-b8fd-592b49b0b7ca></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/mattermost_slash_commands.html>
Mattermost slash commands
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_bc706fdf-cdfe-443f-a1f4-97136169c130></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/microsoft_teams.html>
Microsoft Teams
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_91adbc93-32a3-4066-bae5-6b26d895ac86></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/mock_ci.html>
Mock CI
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3c827eae-f4e1-49cd-9f5c-be337ed995ee></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/prometheus.html>
Prometheus
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_dd6b38ae-f766-4d71-8eab-6775e8d6249e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/servicenow.html>
ServiceNow
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c097bd0b-fe7c-49cf-9543-aa128b52a6f0></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/services_templates.html>
Service templates
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9249040c-8025-4692-bb2f-342b61f547f0></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/shibboleth.html>
Shibboleth
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9839d1cb-84c5-4600-ab05-26567e0f2fa3></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/slack.html>
Slack notifications
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a4a67bd5-9ff9-499a-8481-aa476efbea7c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/slack_slash_commands.html>
Slack slash commands
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_daa88f67-dbc4-45f9-aeb4-c4faaaabe41b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/gitlab_slack_application.html>
Slack application
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4c9fb156-dca1-4650-ad37-352d30e9585d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/unify_circuit.html>
Unify Circuit
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d41ea024-00fa-43ad-8958-6bafafbeef9c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/webex_teams.html>
Webex Teams
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b3783f30-2e79-4b7b-b0af-de9a6ca4e622></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/webhooks.html>
Webhooks
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d0fd751e-a2a5-41e5-ad7a-4a4eece5576c></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/integration/external-issue-tracker.html>
External issue tracker
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_95e57a76-2ab3-4353-9b58-0102e0a48dbe></div>
</span>
<div class=collapse id=cat_95e57a76-2ab3-4353-9b58-0102e0a48dbe>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/bugzilla.html>
Bugzilla
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_fb1a6fd6-0a70-41df-8412-902d30af40ab></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/custom_issue_tracker.html>
Custom issue tracker
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d40f9757-2d1a-48d3-8bed-128aa6840e28></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/ewm.html>
IBM Engineering Workflow Management
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_97b1a882-35e3-41fb-bcf5-1ebc9bc746f8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/redmine.html>
Redmine
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_310be643-af88-4032-a50f-4f85fb3dfaf7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/integrations/youtrack.html>
YouTrack
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_261bf717-4d2f-44bc-92b7-93610ec658b9></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/integration/gmail_action_buttons_for_gitlab.html>
Gmail actions buttons
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_8bdf7b6d-2548-4551-8a39-6516738965dd></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/integration/recaptcha.html>
reCAPTCHA
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_e8202ac2-b96c-4f16-af72-79ffb8c74133></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/integration/security_partners/>
Security partners
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_51ff96b3-0ebc-4e2a-8c91-c4ecdf8b42a2></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/integration/sourcegraph.html>
Sourcegraph
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_6f0d41ba-c61d-44ed-8948-7aa8a29fcd0f></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/integration/trello_power_up.html>
Trello
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_54b76d8d-1da0-4e09-a60b-fab7b6790bf7></div>
</span>
</div>
</div>
<div class=global-nav-section>
<span class="global-nav-block-top nav-link">
<a class="global-nav-link level-0 has-collapse" href=/ee/administration/>
Administer self-managed
</a>
<div class="section-title collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#sec_ced51963-89a2-4e26-b2e8-91c5dc28fc1c></div>
</span>
<div class=collapse id=sec_ced51963-89a2-4e26-b2e8-91c5dc28fc1c>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/administration/auth/README.html>
Authentication and authorization
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_ce5e14d2-4840-4e2e-9294-8972203f1027></div>
</span>
<div class=collapse id=cat_ce5e14d2-4840-4e2e-9294-8972203f1027>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/auth/crowd.html>
Atlassian Crowd
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5c274372-28fe-418a-947a-92efb09309f7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/auth/atlassian.html>
Atlassian
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_fdabce6a-af1f-4414-8110-6f034a901c22></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/auth0.html>
Auth0
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3ce3f021-b163-4d79-9e61-3cf0eb8d8b41></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/auth/authentiq.html>
Authentiq
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_772b718d-5a21-4fb4-8d05-1a45e27dbaee></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/auth/cognito.html>
AWS Cognito
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f6bdda63-443a-438c-a7dc-c2be4573f3d8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/azure.html>
Azure
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_debe3adf-0ae7-455a-9c24-12b4715a15fc></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/bitbucket.html>
Bitbucket Cloud
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ae942c81-1624-4a05-b9a3-c7f63c9df403></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/cas.html>
CAS
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_edd3296d-b66e-4ac1-9b7b-ba34eb597080></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/facebook.html>
Facebook
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_cbf2d305-2e2d-47c4-971d-7846ee4b20ab></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/oauth2_generic.html>
Generic OAuth2
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d9252521-f56c-4607-b994-188350f23fe2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/github.html>
GitHub
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_fdcbb798-e8ec-4941-8534-86081331988c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/gitlab.html>
GitLab.com
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5402573d-0c27-4a05-a050-bb7376ce6e1b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/google.html>
Google
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_2eef5b2f-35dc-48be-b496-d192228e6d1d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/auth/jwt.html>
JWT
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_dc10413c-4cf5-47bd-b8f9-16b3068c62e0></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/kerberos.html>
Kerberos
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1e5d053f-cc6b-403a-8864-7d329ccd2090></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/auth/ldap/>
LDAP
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d84146fd-1b71-4cbd-aadc-bb87715ceca2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/auth/ldap/google_secure_ldap.html>
LDAP (Google Secure)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_85c7c28a-7b70-445c-9d80-a5805327aa91></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/auth/ldap/ldap-troubleshooting.html>
LDAP Troubleshooting
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_68dbe23f-b1ca-4268-8a13-d35cc0b7d259></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/oauth_provider.html>
OAuth service provider
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_54760687-4d58-4d0a-97e8-ff61b1b5f9c3></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/auth/okta.html>
Okta
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6b6417b4-e98a-4950-97d7-ab0902b6cbdf></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/omniauth.html>
OmniAuth
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_85f21f81-6092-4bb2-ae56-d98db58c09e4></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/auth/oidc.html>
OpenID Connect OmniAuth
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_69f3eeba-d15b-40d9-baab-5a312839304e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/openid_connect_provider.html>
OpenID Connect identity
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1d98d097-219c-4598-838c-e9bc64155d92></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/salesforce.html>
Salesforce
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a3d165c7-d287-4134-9288-3e2b1af42bc2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/saml.html>
SAML
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5d5f2d81-2d0f-4211-9358-bb50df95ce52></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/auth/smartcard.html>
Smartcard
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e7199f91-1326-4da0-93e1-2905984f115b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/twitter.html>
Twitter
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3e78356e-c3e6-4d94-ad8c-406afaec8d4e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/integration/vault.html>
Vault
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e290a1fc-a56d-4a10-a88d-b21fba60fde5></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/user/admin_area/>
Configuration and Admin Area
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_46038155-c639-44e2-8cd2-cb320986e8ff></div>
</span>
<div class=collapse id=cat_46038155-c639-44e2-8cd2-cb320986e8ff>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/settings/>
Admin Area settings
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c01fb222-4b38-4655-8efc-e5a233e0b35c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/settings/account_and_limit_settings.html>
Account and limit settings
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_86b7a1c4-3240-4bee-b998-e150e49a31b4></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/appearance.html>
Appearance
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4433b840-7abe-43e8-95df-791b1cfbfd3f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/topics/authentication/>
Authentication
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f9b58bfb-694c-45e4-af32-e717282f1654></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/monitoring/background_migrations.html>
Batched background migrations
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4af28477-3b50-4cae-8233-5c7b7de0fa1c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/settings/continuous_integration.html>
CI/CD
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a18904f7-8c63-456d-bb88-f19cd932b143></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/custom_project_templates.html>
Custom instance-level project templates
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0de6e398-1f02-4cd9-b04f-e9d5fb7f3b73></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/diff_limits.html>
Diff limits
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1fe486ab-7a14-4379-a266-a20007867dc2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/settings/email.html>
Email
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f4422437-d8ff-436b-9dd0-1bc27460876f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/external_pipeline_validation.html>
External pipeline validation
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_73ec46f4-ac81-4807-9b01-9d4e95bba138></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/feature_flags.html>
Enable features with feature flags
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6c1088b7-ff9b-4f08-9db5-4242bfc7c349></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/feature_flags.html>
Available GitLab feature flags
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_750318f5-de6a-46f5-83e4-201e98714a97></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/settings/floc.html>
Federated Learning of Cohorts (FLoC)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0dc472ca-3729-4a47-b9d8-4f4285589f34></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/geo_nodes.html>
Geo nodes
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f0aca673-e2a7-433b-8331-7714f275737d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/lfs/>
Git LFS administration
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5878fb57-e757-43f5-a325-567a277e4682></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/pages/>
GitLab Pages
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ada7afea-cd87-4f5f-b0f9-7bfd88e7e478></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/monitoring/health_check.html>
Health Check
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ff68f5e1-9a59-4cfc-ac93-a31bfa73eef1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/incoming_email.html>
Incoming email
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_abc54cc0-851c-4ea8-a7c1-f6bcf78753d3></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/settings/instance_template_repository.html>
Instance template repository
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_62974a57-ebaf-4b8a-9202-96c3644b8d34></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/job_artifacts.html>
Job artifacts
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5d83a68a-f05b-44e5-aa56-01c5ae2b59b3></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/job_logs.html>
Job logs
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_608537b2-1d59-40d3-8fd5-d17a84da4a88></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/labels.html>
Labels
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ccc70731-8d68-4b9f-baf0-f6bbf73820e9></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/logs.html>
Log system
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_900426c6-cbff-4fbb-ac4f-807e47fdaf14></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/maintenance_mode/>
Maintenance Mode
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b75841a1-9b06-45d0-9d76-cb95e14a9f12></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/merge_requests_approvals.html>
Merge request approvals
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0e7b05c2-72a1-4b9b-88ed-41c96f05e8ba></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/settings/package_registry_rate_limits.html>
Package Registry rate limits
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_912ffa3b-cf31-460b-ac69-daa7e0503825></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/settings/push_event_activities_limit.html>
Push event activities limit
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ebe74c44-a32a-48f7-b95a-29bdf78c0fb3></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/settings/rate_limit_on_issues_creation.html>
Rate limits on issue creation
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_97858435-8590-445f-bb1c-4ff914539e99></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/settings/rate_limit_on_notes_creation.html>
Rate limits on note creation
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_475930f4-3e8b-4d1f-adc6-79945818e0e0></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/reply_by_email.html>
Reply by email
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_99c50f61-1009-4621-ad1b-0e4bb90624ac></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/repository_checks.html>
Repository checks
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_73ec0204-d593-48a7-b81f-3705f7cbd5c8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/settings/sign_in_restrictions.html>
Sign-in restrictions
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_06835aed-a817-4879-9a05-36f3f9ff3197></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/settings/sign_up_restrictions.html>
Sign-up restrictions
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b172bae1-32c5-42f5-8780-fe6b73454f45></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/system_hooks/system_hooks.html>
System Hooks
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_857e369f-fdfc-4d12-8cf8-a7f07ffd9d70></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/timezone.html>
Timezone
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0f189a52-d5a7-465d-9375-535da390b1e4></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/uploads.html>
Uploads
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d155ecc2-e90a-4672-8974-185d613bcbf1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/user_cohorts.html>
User Cohorts
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_60ccc54a-6b29-4337-acbc-73fed7de950e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/settings/visibility_and_access_controls.html>
Visibility and access controls
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_82c059e6-997d-4004-80f7-50523897ada6></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/security/README.html>
Security
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_41cc2d44-c248-46fd-8886-a8ece0077572></div>
</span>
<div class=collapse id=cat_41cc2d44-c248-46fd-8886-a8ece0077572>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/security/password_storage.html>
Password storage
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7e126541-1aed-4e62-b896-1b4144f64c75></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/security/password_length_limits.html>
Custom password length limits
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c4eccce5-9c2d-4f14-a496-6fc5a97abf76></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/security/passwords_for_integrated_authentication_methods.html>
Generated passwords and integrated authentication
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_45a7dc5e-d448-4c38-b1f2-bbac177874bb></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/credentials_inventory.html>
Credentials inventory
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ff17000e-daa5-46fa-87ee-57323a32731d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/security/ssh_keys_restrictions.html>
Limits on SSH keys
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c650fc71-13d5-4bbe-b304-92d4a2edf8a2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/security/rate_limits.html>
Rate limits
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_494454da-7a08-4c4a-b90f-fe84df2a3f3a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/security/webhooks.html>
Webhooks
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_81ec734a-a84f-49c7-b55b-7933098c181b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/security/information_exclusivity.html>
Information exclusivity
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_dbea56bd-5271-4a40-b8f5-a6286ea699b8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/security/reset_user_password.html>
Reset user password
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9f62271a-5cf7-44e3-b4a0-4ae890b72dea></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/security/unlock_user.html>
Unlock a user
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_dd6a8691-3cfc-4084-99da-469a18dc8313></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/profile/unknown_sign_in_notification.html>
Unknown sign-ins, email notification
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4deee8cc-6546-4e73-bd39-76cb27b31084></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/approving_users.html>
Users pending approval
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b234ff4f-1b7f-435a-8ff1-c8b37f062305></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/security/user_file_uploads.html>
User file uploads
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c7f80927-167b-4a9a-81d3-c7999f2d164d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/security/crime_vulnerability.html>
Manage the CRIME vulnerability
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_8315f805-67ff-4dd9-80d9-bec4868231a3></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/security/two_factor_authentication.html>
Enforce two-factor authentication (2FA)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b8623f9b-42e7-42df-ad87-d057f309320c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/security/user_email_confirmation.html>
User email confirmation
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_770d8407-d719-492a-a35e-e85e59cd8272></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=https://docs.gitlab.com/runner/security/ target=_blank>
Security of running jobs
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e63558a3-2aaf-4036-be52-497af50858de></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/security/asset_proxy.html>
Proxying assets
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f95e4171-c793-4cff-b50c-a695cb2a4bd9></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/security/cicd_environment_variables.html>
CI/CD variables
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d95aab1f-c06f-4d3c-8b83-36262e5d304f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/security/token_overview.html>
Token overview
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b966b857-93fa-4c30-b8b9-7ffc175b1650></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/user/admin_area/review_abuse_reports.html>
Review abuse reports
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_237372bd-71e0-4df1-aeff-26d2c8b6b728></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/user/profile/account/create_accounts.html>
Create users
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_028dfe81-e1b8-4353-b3d0-c02daac40035></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/user/admin_area/analytics/>
Analytics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_d9e237e8-fede-45fd-bff1-11fbd4ecd4cc></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/audit_events.html>
Audit events
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_462be1b8-579d-48c5-864d-8a40d8011a69></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/audit_reports.html>
Audit reports
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_c39a5431-0949-4e8e-87a5-7d8053b304f7></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/user/admin_area/broadcast_messages.html>
Broadcast messages
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_8ec7764a-5f06-465b-b876-07738233411e></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/consul.html>
Consul
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_3c8df3a1-ee70-4212-ba3b-4e1c69f09000></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/compliance.html>
Compliance features
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_ca6b653a-e8a0-4886-8336-492975566928></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/tools/email.html>
Email from GitLab
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_29fc50bf-b64e-4206-accf-6bb2aab03648></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/file_hooks.html>
File hooks
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_749ff2bd-8d8b-465f-bfc6-2fd983fad2e5></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/git_protocol.html>
Git protocol v2
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_a5b6e74a-7029-48d9-9698-fc7737ba9bfb></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/user_settings.html>
Global user settings
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_3d23c11e-cce9-4259-a477-195d6ce9a053></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/instance_review.html>
Instance Review
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_e6eaf106-eefc-497b-8aa6-ed036d7a4268></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/invalidate_markdown_cache.html>
Invalidate Markdown cache
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_cb5794bf-13c6-4e88-98af-5f9213aa403c></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/issue_closing_pattern.html>
Issue closing pattern
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_af78d47d-747c-4824-8742-d708d5d3442a></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/merge_request_diffs.html>
Merge request diffs storage
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_b59ddf9d-8d40-4cd2-b021-2f002ef999a7></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/user/admin_area/moderate_users.html>
Moderate users
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_e4ee17fa-8d10-4c29-82a1-41081fc4bcfc></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/administration/postgresql/>
PostgreSQL
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_1b76557e-c59d-4f19-bc34-9ccba8c301dc></div>
</span>
<div class=collapse id=cat_1b76557e-c59d-4f19-bc34-9ccba8c301dc>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/postgresql/pgbouncer.html>
PgBouncer
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c89e8711-e712-4ba6-aa65-d7213f7bcee2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/postgresql/replication_and_failover.html>
Replication and failover
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_44d9f5be-36c5-481f-8060-ffd1ec1743fd></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/postgresql/external.html>
External database service
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_dd0eb03a-c7c3-4de7-86f9-edee0d1ef69b></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/load_balancer.html>
Load balancer
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_15db7ff5-2a25-4759-9bd5-adeabf8326ac></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/nfs.html>
NFS
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_5294319c-bc03-4be1-b9d5-f23a466e3058></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/redis/>
Redis
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_c047c05f-757f-41e1-86b9-b1ae5fe3effe></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/sidekiq.html>
Sidekiq
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_d627859d-7aae-4eef-9b9f-e776ce86fb7b></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/snippets/>
Snippets
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_4f370f62-649d-46f9-a488-7d8165e32f1f></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/clusters/kas.html>
Kubernetes Agent Server
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_da33706f-94e2-4186-93c3-c2a23e6e161e></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/administration/repository_storage_paths.html>
Repository storage
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_85fef7c1-7922-4edb-b93d-a6e1b0bc3613></div>
</span>
<div class=collapse id=cat_85fef7c1-7922-4edb-b93d-a6e1b0bc3613>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/repository_storage_types.html>
Repository storage types
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_27b361b4-58cd-47c6-9639-a1154faf0d74></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/administration/gitaly/>
Gitaly and Gitaly Cluster
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_9eeff24e-8816-4ea2-b776-6703d916683d></div>
</span>
<div class=collapse id=doc_9eeff24e-8816-4ea2-b776-6703d916683d>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/administration/gitaly/configure_gitaly.html>
Configure Gitaly
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_323ae5f3-2eee-4dab-a061-df9eed61a5fd></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/administration/gitaly/praefect.html>
Configure Gitaly Cluster
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_24bc7cfb-767f-4f65-aa42-b532b473b818></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/gitaly/reference.html>
Gitaly reference
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1cdbf681-f831-41f3-8e6a-d3ee479948a0></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/settings/gitaly_timeouts.html>
Gitaly timeouts
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_bc66fc74-42bf-4bf2-a147-19561bdaba49></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/administration/monitoring/>
Metrics
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_5bad4cc9-214d-4725-b854-8fc9188147fb></div>
</span>
<div class=collapse id=cat_5bad4cc9-214d-4725-b854-8fc9188147fb>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/monitoring/performance/gitlab_configuration.html>
Configure GitLab
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_bc6ebbd4-aded-42d4-8b2a-5c4d28a69b92></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/monitoring/performance/grafana_configuration.html>
Configure Grafana
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_28e3f775-f849-4d9d-b2cb-2be68e13edd0></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/monitoring/github_imports.html>
GitHub imports
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_48ebe480-a596-4d86-b64d-e18ff0a65d48></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/monitoring/prometheus/gitlab_exporter.html>
GitLab exporter
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_88c7bc08-b030-495a-b35a-5a0463c94ff6></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/monitoring/prometheus/gitlab_metrics.html>
GitLab Prometheus metrics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_343a6a1c-904c-4a9e-9721-062aebee39d5></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/monitoring/gitlab_self_monitoring_project/>
GitLab self monitoring project
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_80a5419f-b964-4440-9c76-cce58721ce8e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/monitoring/ip_whitelist.html>
IP allowlist endpoints
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4b2341df-73de-48a0-85ed-43ee44be60a7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/monitoring/prometheus/node_exporter.html>
Node exporter
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7a69f155-dced-4407-945f-693be660ad26></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/monitoring/prometheus/pgbouncer_exporter.html>
PGBouncer exporter
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_df6d275b-fb9b-4107-971a-6679ddf9dbbf></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/monitoring/prometheus/postgres_exporter.html>
PostgreSQL server exporter
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a78a4164-116b-44be-8292-6c5af510c276></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/monitoring/prometheus/>
Prometheus
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0e3941b6-e56e-4d04-81ba-d3558ce04102></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/monitoring/performance/performance_bar.html>
Performance bar
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_16904510-b6b0-495e-9aef-03bcbc19fad7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/monitoring/performance/>
Performance monitoring
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d0a747f3-a12a-44b2-a7d8-65a443fd854f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/monitoring/prometheus/redis_exporter.html>
Redis exporter
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d8a94e78-7495-4862-94e8-2bf4729959d5></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/monitoring/prometheus/registry_exporter.html>
Registry exporter
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5055af52-aa15-4100-8361-10aca9b79f80></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/monitoring/performance/request_profiling.html>
Request profiling
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_465bc38b-cdcc-4bba-8653-941550838a1d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/settings/usage_statistics.html>
Usage statistics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c0c1d5b0-8c08-4a3e-9c90-e786b77e5d3a></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/object_storage.html>
Object storage
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_ba47f364-bfaf-4700-a434-fa1da672fa6e></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/administration/operations/>
Operations
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_e712d0d9-82b4-4f1a-98ab-63e89a55c0f6></div>
</span>
<div class=collapse id=cat_e712d0d9-82b4-4f1a-98ab-63e89a55c0f6>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/operations/cleaning_up_redis_sessions.html>
Clean up Redis sessions
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ace1782b-44b3-41fd-ab96-afd5f92d8340></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/operations/fast_ssh_key_lookup.html>
Fast SSH key lookup
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9eea6bc8-894d-40b9-8309-205119a7bc56></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/operations/filesystem_benchmarking.html>
Filesystem benchmarking
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a7fee607-2b59-4b5d-8e68-7da64a2d1bf1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/operations/moving_repositories.html>
Move repositories
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_00911114-5f07-4ac4-999a-e9eacd16718e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/operations/extra_sidekiq_processes.html>
Multiple Sidekiq processes
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e57e906e-5fe9-4cb7-b8eb-9cde8ea2da9e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/operations/rails_console.html>
Rails console
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5b30b800-230f-4ba4-8f48-d349bd5dbb60></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/operations/sidekiq_memory_killer.html>
Sidekiq MemoryKiller
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_03793ff3-d18c-4182-97af-a4b993fb1faf></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/operations/puma.html>
Switch to Puma
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0cf29ec3-19d3-4da1-8541-615e8917de91></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/operations/ssh_certificates.html>
Use SSH certificates
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_98f0edd3-effd-4922-9991-16af27802e1a></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/administration/packages/>
Packages
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_8ab407a9-313d-4bf6-8d3f-0803b3d4103e></div>
</span>
<div class=collapse id=cat_8ab407a9-313d-4bf6-8d3f-0803b3d4103e>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/packages/container_registry.html>
Container Registry
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_47cb9221-fdce-4ef9-87a1-adf07ec159e7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/packages/dependency_proxy.html>
Dependency Proxy
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ff096006-ca8e-4fe8-ad9a-5309bf8fbbcc></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/administration/geo/>
Geo
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_00e4f6e3-a768-4e1f-aa43-338d8807803c></div>
</span>
<div class=collapse id=cat_00e4f6e3-a768-4e1f-aa43-338d8807803c>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/setup/>
Setting up Geo
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4a641db4-1cd1-4c7f-8e5a-d74f18eb3fa4></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/setup/database.html>
Database replication
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_877f5d7d-9deb-4556-b20e-1481b3886a5e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/setup/external_database.html>
External PostgreSQL instances
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_524f89f5-c2a4-4068-b050-c44de7f3db3b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/replication/configuration.html>
Configuration
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_01c0385a-cf7c-41b3-8699-bca8b5d80157></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/replication/usage.html>
Using a Geo site
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_889228d7-7b4e-487c-9485-b9e7c0ec837a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/replication/updating_the_geo_nodes.html>
Updating Geo nodes
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_2a9b9c68-4539-4d29-995f-6993a6ce4970></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/replication/version_specific_updates.html>
Version-specific updates
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_89cbaad7-f6bb-4ba0-89b3-3bdfa41b4621></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/replication/object_storage.html>
Using object storage
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_864d524c-3072-4d00-87a5-6f28bed08bd8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/replication/docker_registry.html>
Using Docker Registry
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_2a91a62a-f107-4fa9-8c83-ab5b91ffc428></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/replication/multiple_servers.html>
Geo for multiple servers
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4e8af1bd-88b8-4149-8595-e3335f654438></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/replication/security_review.html>
Geo security review
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_21515c3e-2d44-4a40-959e-bccd369e2586></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/replication/location_aware_git_url.html>
Location-aware Git remote URLs
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_8446b8ab-ce9c-4fce-a8d6-42685ae7b708></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/replication/tuning.html>
Tuning Geo
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_10013a56-d2bf-4210-801c-d4673b65aea8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/replication/disable_geo.html>
Disable Geo
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_dea50322-4e1c-4e39-b23f-bb52481c8998></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/replication/remove_geo_site.html>
Removing a Geo site
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_79c5905f-47f4-499f-a04b-01b218e55d3b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/replication/datatypes.html>
Supported data types
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_252abbfc-b922-499a-88c6-083baed86458></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/replication/faq.html>
Frequently asked questions
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_274ea017-1ce5-4e2f-a988-1dcb77532723></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/replication/troubleshooting.html>
Troubleshooting
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3ec0dbbe-1c16-41fc-902b-2d7bdeaf5581></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/replication/geo_validation_tests.html>
Validation tests
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4ef99ab3-3154-42f5-9854-e1486d8bfb4d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/glossary.html>
Geo Glossary
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5c76fe6f-1583-45ea-9be3-5a7d91ea3532></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/administration/geo/disaster_recovery/>
Disaster recovery (Geo)
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_08803678-1bba-4eb1-ba2c-92161f1422d6></div>
</span>
<div class=collapse id=cat_08803678-1bba-4eb1-ba2c-92161f1422d6>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/disaster_recovery/planned_failover.html>
Planned failover
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_da6051fa-0c44-4374-b89f-a848578b6dd5></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/disaster_recovery/bring_primary_back.html>
Bring primary back
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_519b62e0-1eb5-42f9-b021-84851408b7b1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/geo/disaster_recovery/background_verification.html>
Automatic background verification
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_2671cafd-a734-48a3-91fd-d6de8287756f></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/raketasks/>
Rake tasks
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_9b24bfcc-6644-4c0e-b1df-94f173b37275></div>
</span>
<div class=collapse id=cat_9b24bfcc-6644-4c0e-b1df-94f173b37275>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/raketasks/backup_restore.html>
Backup and restore
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f75ec3c5-c4fe-44b7-b341-dd5e0d8b2509></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/raketasks/cleanup.html>
Clean up
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6b49e222-3d1a-48bb-b3ff-0208f4d569df></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/raketasks/features.html>
Enable namespaces
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_dec2099d-2bf9-4b1c-8cc8-1f8426e0c4b4></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/raketasks/maintenance.html>
General maintenance
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d2788bc0-fc6e-415a-9f5c-eee5441f269a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/raketasks/geo.html>
Geo tasks
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c0055dff-86d6-4a86-b65b-db2af296ae8b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/raketasks/github_import.html>
GitHub import
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_98c1d249-3989-4a06-9206-1d72105a6a2f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/raketasks/import.html>
Import repositories
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c9887ec0-55b4-4345-9af6-e7ebffa7fa1f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/raketasks/check.html>
Integrity check
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c6c36257-65b3-4a3d-b05f-af6da12632db></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/raketasks/ldap.html>
LDAP maintenance
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_45d30aca-7740-4ba4-a7ee-72d5d1ec5fe7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/raketasks/list_repos.html>
List repositories
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_913d9e43-0500-4bcc-ba0d-6d635b559a2e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/raketasks/migrate_snippets.html>
Migrate snippets
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d51d4184-2fda-4c5d-8154-b203412769e9></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/raketasks/praefect.html>
Praefect tasks
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1daf00ff-69f8-45f7-af0c-97091c9bc9e2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/raketasks/project_import_export.html>
Project import and export
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b2628a8e-1fb4-48b2-83bc-561e5968ba08></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/raketasks/storage.html>
Repository storage
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5988ce0e-6591-4ce8-b3eb-335f8e883cae></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/raketasks/generate_sample_prometheus_data.html>
Sample Prometheus data
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_dbe18f70-8295-4789-a117-ea16d09e0925></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/raketasks/uploads/migrate.html>
Uploads migration
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f2241e3c-bcba-4762-861d-44f64aea2a8c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/raketasks/uploads/sanitize.html>
Uploads sanitization
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ddae9e72-7d87-4644-b422-ba088c424449></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/raketasks/user_management.html>
User management
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6dee064f-5a68-4f10-9fff-c31ad04a79c5></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/raketasks/web_hooks.html>
Webhooks administration
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_394f6804-5fe7-4cb6-90d0-84b94b5a1653></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/raketasks/x509_signatures.html>
X509 signatures
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_51a18cf3-e26f-44e1-b826-f3054394ef13></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/server_hooks.html>
Server hooks
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_020f618c-ec4f-48d9-8bbf-4bdb92052a0f></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/static_objects_external_storage.html>
Static objects external storage
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_3a7d59b0-6b63-4fe5-852c-c93576c01005></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/terraform_state.html>
Terraform state
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_5fc27dbd-4a6c-469a-bba6-0bbec6b5d06a></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/update/>
Update
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_dc49220a-9d12-43d2-8693-e5c84ff92520></div>
</span>
<div class=collapse id=cat_dc49220a-9d12-43d2-8693-e5c84ff92520>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/policy/maintenance.html>
Releases and maintenance
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7e2cfe28-9a1a-411f-8acf-2740b551b78f></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/whats-new.html>
What's new
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_1a1d3f9b-d164-47ea-b34d-394676b614e5></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/integration/terminal.html>
Web terminals
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_253e7eaf-011e-47a5-864c-6d821cffc79d></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/administration/wikis/>
Wikis
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_100c5eeb-e8eb-4786-b2f7-2877db2f5f17></div>
</span>
</div>
</div>
<div class=global-nav-section>
<span class="global-nav-block-top nav-link">
<a class="global-nav-link level-0 has-collapse" href=/ee/topics/use_gitlab.html>
Use GitLab
</a>
<div class="section-title collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#sec_7964142a-f2b6-4573-8f61-e2bcda42039d></div>
</span>
<div class=collapse id=sec_7964142a-f2b6-4573-8f61-e2bcda42039d>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/topics/set_up_organization.html>
Set up your organization
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_65c0fe7e-c169-4121-b7e9-304657b5791a></div>
</span>
<div class=collapse id=cat_65c0fe7e-c169-4121-b7e9-304657b5791a>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/members/>
Members
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_653a12b6-d7f7-47aa-90aa-945e9a2017be></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/user/group/>
Groups
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_547091b1-5975-4ba5-bcfb-72ee7f2c5aa0></div>
</span>
<div class=collapse id=doc_547091b1-5975-4ba5-bcfb-72ee7f2c5aa0>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/group/custom_project_templates.html>
Custom group-level project templates
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ac0963f4-59a4-4d77-a26d-3d0482b9925d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/group/settings/import_export.html>
Group Import/Export
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7f882e0a-5d9a-4ac3-843b-f509a9aa9e1c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/group/import/>
Migrating groups
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9e7e3790-3a11-464f-99a4-0324eaa70734></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/user/group/saml_sso/>
SAML SSO for GitLab.com groups
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_a9ad5b95-ab37-4ced-a9f3-685e5e0cc51b></div>
</span>
<div class=collapse id=doc_a9ad5b95-ab37-4ced-a9f3-685e5e0cc51b>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/group/saml_sso/group_managed_accounts.html>
Group Managed Accounts (Closed Beta)
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/group/saml_sso/scim_setup.html>
SCIM provisioning
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/administration/troubleshooting/group_saml_scim.html>
Troubleshooting Group SAML and SCIM
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/group/subgroups/>
Subgroups
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b7925910-c432-4789-bdbd-3df3b5534419></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/user/profile/>
User account options
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_e585877d-f3c8-4281-88aa-d3e66c5d38b2></div>
</span>
<div class=collapse id=doc_e585877d-f3c8-4281-88aa-d3e66c5d38b2>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/profile/active_sessions.html>
Active sessions
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e61426b0-7c0c-4a8e-bea9-9689c77bf48e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/permissions.html>
Permissions
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_def3599a-2efb-4e47-aed4-949d008c513a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/profile/personal_access_tokens.html>
Personal access tokens
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9e444897-3f7f-4a1c-bb7d-568102ab3c3d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/profile/preferences.html>
Profile preferences
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9337407b-1f5c-4ffa-9ff2-e6d725bf87ef></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/profile/notifications.html>
Notification emails
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7af2ebf3-b4a9-48e0-991e-6bf0a5d69442></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/profile/account/two_factor_authentication.html>
Two-factor authentication
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5d0e4f06-3dd0-4986-87b4-4a5e81acf312></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/report_abuse.html>
Report abuse
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_17f238b0-2d73-4a28-be89-f8dc34998d14></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/profile/account/delete_account.html>
Delete account
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_51c50d5f-9fd2-4b43-bdec-8d7882901786></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/ssh/README.html>
SSH keys
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6300f3a2-e57c-44ec-a152-e8a368b0c2d9></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/gitlab_com/>
GitLab.com settings
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_797bd750-4a47-48c9-8140-dfaa54af2bcf></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/user/project/>
Organize work with projects
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_679633eb-9dc2-4794-ab4f-5bd0b0ba1721></div>
</span>
<div class=collapse id=cat_679633eb-9dc2-4794-ab4f-5bd0b0ba1721>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/working_with_projects.html>
Manage projects
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c25db57c-9d29-4633-8aa5-d7ebd47ae576></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/public_access/public_access.html>
Public access
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6abd442f-0697-42b6-8f21-17224079caa7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/settings/>
Project settings
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3fc4c3b9-7056-4821-82af-68f7810dc621></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/settings/project_access_tokens.html>
Project access tokens
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c69989c6-a64e-419f-8b04-35506042ae43></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/members/share_project_with_groups.html>
Share projects
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ed914905-6f02-4d6b-81b7-2e7c92040d9c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/reserved_names.html>
Reserved project and group names
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9ec03897-6970-43b4-84cd-cfd4b9c3ea1b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/user/search/>
Search
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_a62eeafe-ae34-48af-a509-2ae1658fbe47></div>
</span>
<div class=collapse id=doc_a62eeafe-ae34-48af-a509-2ae1658fbe47>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/search/advanced_search.html>
Advanced Search
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_46b99d47-674e-4626-a083-cd61f9cf2881></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/badges.html>
Badges
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_92ae10d3-eeca-4a75-843f-30c9de35788b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/code_intelligence.html>
Code intelligence
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_fe84f743-0e58-4d12-ac8f-895c239e366b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/user/compliance/>
Compliance
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_9ffec8f9-9e65-4745-a9bf-e609ebe8008a></div>
</span>
<div class=collapse id=doc_9ffec8f9-9e65-4745-a9bf-e609ebe8008a>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/compliance/license_compliance/>
License Compliance
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a154adcc-e24b-4e69-a5d0-940606fc46f4></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/compliance/compliance_dashboard/>
Compliance Dashboard
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_88abd5d1-b480-4576-8b80-5b71a25c86d0></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/description_templates.html>
Description templates
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d2f8be33-0d88-459a-a727-ea54135ce0a0></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/deploy_keys/>
Deploy keys
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a5c9b7ba-6cdf-48ba-8dc4-e33b72d9ebcc></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/deploy_tokens/>
Deploy tokens
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_14d52a45-1471-4dde-a00c-fc225be7b0b3></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/repository/file_finder.html>
File finder
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c6074162-d0fd-44f9-babc-e788b008840a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/user/project/pages/>
GitLab Pages
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_ce164324-d065-45ee-966a-00f9bb818384></div>
</span>
<div class=collapse id=doc_ce164324-d065-45ee-966a-00f9bb818384>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/pages/getting_started/pages_from_scratch.html>
Create from scratch
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6366cdd1-bb78-44bc-adfe-ee8378fc6237></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/pages/getting_started/pages_ci_cd_template.html>
Create using a CI/CD template
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_dd0ef8d1-ab15-4239-ab37-8514715e9296></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/pages/getting_started/pages_forked_sample_project.html>
Create using a forked sample project
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5153fe00-2d1e-4bc5-abb3-e00b4043c20e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/pages/getting_started/pages_new_project_template.html>
Create using a project template
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b62738ff-ea41-4caf-a540-2852fdd4be28></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/pages/getting_started_part_one.html>
Default domains, URLs, and baseurls
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_8a8544b2-6bf5-4414-89d7-fee138e7b085></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/pages/custom_domains_ssl_tls_certification/>
Custom domains and SSL/TLS certificates
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_8a924fbd-2536-45a5-b1cc-4b02024fc42f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/pages/custom_domains_ssl_tls_certification/dns_concepts.html>
DNS concepts
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_28368b12-0c3c-42f2-a710-28487a2658b1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/pages/custom_domains_ssl_tls_certification/ssl_tls_concepts.html>
SSL/TLS concepts
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0291a8b0-9283-4fae-8337-174c5fa5ccad></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/pages/custom_domains_ssl_tls_certification/lets_encrypt_integration.html>
Let's Encrypt integration
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_561f6621-59b4-4268-a49f-5bcbdd089fd7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/pages/pages_access_control.html>
Access control
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_dbe6a9e5-4692-41ad-bd02-25b86c811d7b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/pages/redirects.html>
Redirects
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_276b6b95-8ed6-4f44-8823-e4fd29c451ce></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/pages/introduction.html>
Exploring GitLab Pages
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_bc10e4f7-a929-46ad-91f4-2bea507d65e5></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/user/project/import/>
Migrating projects
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_4dad106e-2b06-4d16-acd6-2f1d0a53831e></div>
</span>
<div class=collapse id=doc_4dad106e-2b06-4d16-acd6-2f1d0a53831e>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/import/bitbucket.html>
Bitbucket Cloud
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_bf414d36-ce16-431f-a849-dee1205f4ac0></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/import/bitbucket_server.html>
Bitbucket Server
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_754c6838-e9e5-48ea-8a4e-a6bc9bdef793></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/import/clearcase.html>
ClearCase
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_78ae1dad-1dba-410a-ab2c-f2a11c6013b8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/import/cvs.html>
CVS
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3102f5f8-2401-454d-8b2e-39eb368972b1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/import/fogbugz.html>
FogBugz
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_310b2b48-f83d-4172-9831-3d2a3983049b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/import/github.html>
GitHub
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e72f1299-79d5-401a-82fd-bbd1ba73ecbc></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/import/gitlab_com.html>
GitLab.com
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e15e4a75-6d4f-45ea-b199-27c9df9fc239></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/import/gitea.html>
Gitea
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5bb723c5-d91e-400d-85c2-6b29734b7e9f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/import/jira.html>
Jira
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0dfc0b3e-e33a-4b79-9c5e-e26f0acc49bf></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/import/perforce.html>
Perforce Helix
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c26de8b1-6367-43a9-93d2-20a14dfb8479></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/import/phabricator.html>
Phabricator
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_cb3ae382-241a-4b95-b2b8-b0cbc457a1cf></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/import/manifest.html>
Repo by manifest file
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_794ca93d-44f6-48d4-bad5-24c92722b750></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/import/repo_by_url.html>
Repo by URL
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b0c10af5-952f-4b8a-907c-0995e2dab7cf></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/import/svn.html>
SVN
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0d105904-ae6b-4ecf-a643-e08c0884d576></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/import/tfvc.html>
TFVC
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f59add05-15fb-4900-a738-0c942353c9a2></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/settings/import_export.html>
Project import/export
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ffb53fb8-44dc-4ac6-a987-e282ebf11fa4></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/settings/import_export_rate_limits.html>
Project/Group import/export rate limits
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_38ca8310-0dc9-4b33-897a-70c7b44a5ff5></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/topics/plan_and_track.html>
Plan and track work
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_ac5c957a-bc83-4c2b-80a0-aed0aad25be6></div>
</span>
<div class=collapse id=cat_ac5c957a-bc83-4c2b-80a0-aed0aad25be6>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/user/group/epics/>
Epics
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_73e9a7d0-1772-4b70-996f-86ef48f31035></div>
</span>
<div class=collapse id=doc_73e9a7d0-1772-4b70-996f-86ef48f31035>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/group/epics/manage_epics.html>
Manage epics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_428e38ac-ef88-45d1-84da-550f5cc23c29></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/group/epics/epic_boards.html>
Epic Boards
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ddf57135-db50-4132-b913-53e4bcb833c6></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/user/project/issues/>
Issues
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_d3fa2a9d-5ce6-41df-b352-63ba607c7688></div>
</span>
<div class=collapse id=doc_d3fa2a9d-5ce6-41df-b352-63ba607c7688>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/issues/issue_data_and_actions.html>
Manage issues
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4b65d71c-8eff-4d56-9c1c-0577b6ef0688></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/award_emojis.html>
Award emoji
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b68ebb35-8a09-4c62-8fa1-7d54ec6bd5d8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/issues/confidential_issues.html>
Confidential issues
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_015bcaa6-f8ae-484a-9319-d79ae400cdf8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/issues/crosslinking_issues.html>
Crosslinking issues
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9d54322b-a631-432d-bbc4-8e9194c0df9c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/issues/csv_export.html>
CSV export
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_bcd65d45-5abb-4671-b044-34383d642234></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/issues/csv_import.html>
CSV import
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_cde6163d-f056-432d-9552-089ae63fb0f2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/issues/design_management.html>
Design management
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_846e3b23-3640-4e72-83dc-af3700d96328></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/issues/due_dates.html>
Due dates
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_8765da94-73a0-4f1d-9581-51f44c6b168a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/issue_board.html>
Issue Boards
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_071b0481-2ed5-4b68-91ea-2c203ca3f0fe></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/issues/managing_issues.html>
Managing issues
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_800da498-4702-4c70-b447-e68c531c4e10></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/issues/multiple_assignees_for_issues.html>
Multiple assignees
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e44245bc-9dbf-49e7-94fe-1240069c161e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/issues/related_issues.html>
Linked issues
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_dd108a12-56f1-403e-b22d-4b2dca64dba0></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/service_desk.html>
Service Desk
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1ce3bbd0-9372-4c9b-8e45-fcbadedc6a44></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/issues/sorting_issue_lists.html>
Sorting and ordering issue lists
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7503be06-41e0-4b33-a673-37f255095ee8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/issues/issue_weight.html>
Weight
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_335d32ed-ca48-4c7c-8625-04bf5d01d6a8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/issues/associate_zoom_meeting.html>
Zoom meetings in issues
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d8028856-384c-4c92-81b7-da459d11d01b></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/labels.html>
Labels
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_60d48a2b-aeb7-4350-8cac-69008c0fdd4a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/discussions/>
Discussions
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_66fe080c-ad0d-4c54-a87d-9a5faa4db9bc></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/group/iterations/>
Iterations
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b8d7da24-f98e-4bb4-bcb8-32ff1186cb67></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/user/project/milestones/>
Milestones
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_2bd2d216-7f67-4a28-b9df-a20af9aeb29b></div>
</span>
<div class=collapse id=doc_2bd2d216-7f67-4a28-b9df-a20af9aeb29b>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/milestones/burndown_and_burnup_charts.html>
Burndown and burnup charts
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_fc0bd1e9-9106-4372-a2b5-f5c5516d9c50></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/requirements/>
Requirements
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_8a18d897-209f-439a-9edc-e53731fbf930></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/group/roadmap/>
Roadmaps
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_09803ef8-b634-4848-a745-2ef0c44fb54d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/time_tracking.html>
Time tracking
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6406b63d-fb13-4f0e-9f67-b7f842b7c32d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/wiki/>
Wikis
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0f520f68-36bc-45e1-87ca-61d1e269ec96></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/shortcuts.html>
Keyboard shortcuts
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e188add1-883f-43f6-8982-8c75c456eced></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/user/project/quick_actions.html>
Quick actions
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_bc476d67-93aa-4764-b912-7f9c884c0313></div>
</span>
<div class=collapse id=doc_bc476d67-93aa-4764-b912-7f9c884c0313>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/autocomplete_characters.html>
Autocomplete characters
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_554f248d-c985-4b43-866a-234eeb0b0e8c></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/user/markdown.html>
Markdown
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_3180902a-d70e-4c18-b6d2-a13432b4cdc3></div>
</span>
<div class=collapse id=doc_3180902a-d70e-4c18-b6d2-a13432b4cdc3>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/asciidoc.html>
AsciiDoc
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f6931d21-6d84-43a2-a47a-d4e67c392d39></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/todos.html>
To-Do lists
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f92325ba-51ad-448a-9cc1-564fbc92f049></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/topics/git/>
Using Git
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_67a02563-b15d-46a5-946d-bc199d8de032></div>
</span>
<div class=collapse id=doc_67a02563-b15d-46a5-946d-bc199d8de032>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/gitlab-basics/start-using-git.html>
Get started
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_730c7a09-0045-4a09-9f0f-72fb47a67571></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/topics/git/how_to_install_git/>
Installing Git
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_87b8d9c3-9854-4c75-a606-0bd0b5011f7f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/gitlab-basics/create-branch.html>
Create branch
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_8f462273-ed62-4a91-ac1d-7f356d6b3d4e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/gitlab-basics/feature_branch_workflow.html>
Feature branch workflow
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d5e506b6-cecc-4bb8-90e3-2b3be75fdf04></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/topics/git/feature_branch_development.html>
Feature branch development
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_88f0c19a-d5f5-46a4-9866-8e750ba4dfbe></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/topics/gitlab_flow.html>
GitLab Flow
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_fb8f63fe-2543-4012-b11a-93ab18840cc7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/gitlab-basics/add-file.html>
Add file to repository
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_62ce4fd0-3bf4-48ba-81a5-7ae0308390cf></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/gitlab-basics/command-line-commands.html>
File editing
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_2e2f6457-c6f5-4646-a5bc-607c76776a80></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/topics/git/partial_clone.html>
Partial clone
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_be6e7237-2484-4314-bf47-8ce885a48396></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/topics/git/git_rebase.html>
Rebase, force-push, merge conflicts
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_119a731c-f294-4b0b-8524-69a0f0f26dd2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/topics/git/tags.html>
Tags
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0c769cae-7ee2-483f-a370-b4abb585edef></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/topics/git/troubleshooting_git.html>
Troubleshooting Git
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_64def3e7-4e4a-4c23-aa70-dc82171bd024></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/topics/git/numerous_undo_possibilities_in_git/>
Undo with Git
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4543ff7f-62e5-42c8-8e6e-142e83b32965></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/topics/git/useful_git_commands.html>
Useful commands
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_91d649e9-b687-4dc0-9214-97f7a0e5d235></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/push_options.html>
Push options
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a8df3abf-b43a-4af5-8255-12d79304d06a></div>
</span>
</div>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/topics/build_your_application.html>
Build your application
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_b17211dd-eb2d-404e-8077-8e6f1785f223></div>
</span>
<div class=collapse id=cat_b17211dd-eb2d-404e-8077-8e6f1785f223>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/user/project/repository/>
Repositories
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_5f6130d9-a1e1-4594-bc77-c496e8650986></div>
</span>
<div class=collapse id=doc_5f6130d9-a1e1-4594-bc77-c496e8650986>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/code_owners.html>
Code owners
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_fd5cec6c-1db8-4092-abfe-a701231e5b34></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/snippets.html>
Snippets
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d42840dc-9547-4b76-b1d2-fd4ad2229cf7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/static_site_editor/>
Static Site Editor
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_252cb77e-83b5-415f-975c-e07b0cb59d4b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/repository/branches/>
Branches
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_77883f66-444e-47ad-9b3c-4858101a3bd8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/repository/branches/default.html>
Default branch
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_cea74bf7-0b9b-41c9-bcc2-8dbe096c8529></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/repository/forking_workflow.html>
Forking workflow
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4df04c59-ad28-481c-acf2-a0ec61d76248></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/git_attributes.html>
Git attributes
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c0cc6655-00ef-4a1e-83ba-353232ca0b18></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/topics/git/lfs/>
Git LFS
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_2ffe6d39-a41f-40e2-819a-2ccbd5edb1c0></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/repository/jupyter_notebooks/>
Jupyter notebook files
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_8734f97d-63ac-4a1a-8a6d-f784adda37ae></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/file_lock.html>
Locked files
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9bdb118b-8cf2-4a23-9c7c-165144cde781></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/repository/git_blame.html>
File Blame
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7ece18de-826a-44b1-b10b-fb3bf779e7fe></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/repository/git_history.html>
File History
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4e41b9a9-9423-4faf-b553-310478a6e052></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/repository/repository_mirroring.html>
Mirroring
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f1625911-e813-45f3-8453-be4b54884a50></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/protected_branches.html>
Protected branches
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ea0d8164-7a1b-459d-879e-2a877d9118d6></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/protected_tags.html>
Protected tags
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ea8298e4-5603-425b-9af3-492f2ace80d1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/push_rules/push_rules.html>
Push rules
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e34b3ca6-9d92-41ad-a185-629437979f05></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/repository/reducing_the_repo_size_using_git.html>
Reduce repository size
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_bd6eb357-4db6-4d6c-a2b9-2c1b0f58fb1e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3  active" href=/ee/user/project/repository/gpg_signed_commits/>
Signed Commits
</a>
<div class=active data-toggle=collapse aria-expanded=false data-target=#doc_35074abb-6455-42f7-a20f-f83579491416></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/repository/x509_signed_commits/>
Signing commits and tags with X.509
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0fbbe4bc-f5d4-4836-8f7b-0a05f1bbb145></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/highlighting.html>
Syntax highlighting
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d6b7ee17-c1a2-4793-95d8-3f7dc834c2c4></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/repository/web_editor.html>
Web Editor
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c9b5ca6e-db70-4b3d-a77d-617bc8cf9b96></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/web_ide/>
Web IDE
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_663d3f25-35b7-4b28-a44d-0a8a6c226c9c></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/user/project/merge_requests/>
Merge requests
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_fc16ead9-93c3-467d-89b2-212de5acf45a></div>
</span>
<div class=collapse id=doc_fc16ead9-93c3-467d-89b2-212de5acf45a>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/merge_requests/getting_started.html>
Get started
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_2e24642f-df2a-4300-b84f-e0342ecdc3a1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/merge_requests/allow_collaboration.html>
Allow collaboration
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d5cbc05d-e61c-4edd-8a93-5b2a6e076fc5></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/user/project/merge_requests/approvals/>
Approvals
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_ea46ce64-9068-4aa7-a763-2330ec0dbab0></div>
</span>
<div class=collapse id=doc_ea46ce64-9068-4aa7-a763-2330ec0dbab0>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/project/merge_requests/approvals/rules.html>
Approval rules
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/project/merge_requests/approvals/settings.html>
Approval settings
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/merge_requests/creating_merge_requests.html>
Create merge requests
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d2c48624-d46f-4d83-a4ef-b46c6c21e0d8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/merge_requests/cherry_pick_changes.html>
Cherry pick changes
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4e195a3a-1a5d-42ab-b44d-ec068ffca073></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/merge_requests/drafts.html>
Draft merge requests
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6f70212a-efd6-4806-b13a-9f533dd8ee22></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/merge_requests/csv_export.html>
Export merge requests to CSV
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_129adfc8-3b37-47e8-bb91-9fee6a4efd0a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/merge_requests/merge_request_dependencies.html>
Merge request dependencies
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ecdd1189-468e-4a67-8c5f-a735cbcb468f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/merge_requests/fast_forward_merge.html>
Fast forward
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7a268fca-0a52-43cb-b9ad-bb39b3882aaa></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/merge_requests/merge_when_pipeline_succeeds.html>
Merge when pipeline succeeds
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_cccc42d4-1a41-4225-b6a5-75b6cd751ca4></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/merge_requests/resolve_conflicts.html>
Resolve conflicts
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_cb810b67-bdb2-42b0-93f6-99ba12ff035c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/merge_requests/revert_changes.html>
Reverting changes
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0d61a419-6c8d-4402-8c57-d64efece3a4d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/user/project/merge_requests/reviews/>
Reviewing and managing merge requests
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_17e81fc4-280e-47de-b611-4a536cdf11cf></div>
</span>
<div class=collapse id=doc_17e81fc4-280e-47de-b611-4a536cdf11cf>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/project/merge_requests/reviews/suggestions.html>
Suggestions
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/merge_requests/squash_and_merge.html>
Squash and merge
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ea7a4c8e-bf1c-4067-a8fd-7123218ceb78></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/merge_requests/versions.html>
Versions
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_26507729-d74e-4514-86d4-9df347f4e9a2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/merge_requests/authorization_for_merge_requests.html>
Workflows
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c3b24be6-16e1-4a78-b33c-74122d9c6927></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/ci/README.html>
CI/CD
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_7159f13f-78bc-46d9-90ad-4e6f9b933b64></div>
</span>
<div class=collapse id=doc_7159f13f-78bc-46d9-90ad-4e6f9b933b64>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/ci/quick_start/>
Get started
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_295d8193-e939-4d8d-864e-50eefd12891e></div>
</span>
<div class=collapse id=doc_295d8193-e939-4d8d-864e-50eefd12891e>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/introduction/>
CI/CD concepts
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/migration/circleci.html>
Migrate from CircleCI
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/migration/jenkins.html>
Migrate from Jenkins
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/enable_or_disable_ci.html>
Enable or disable CI/CD
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/ci/pipelines/>
Pipelines
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_e1c51fd6-095f-41c2-9fa4-99469c0c8497></div>
</span>
<div class=collapse id=doc_e1c51fd6-095f-41c2-9fa4-99469c0c8497>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/pipelines/schedules.html>
Schedule a pipeline
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/triggers/README.html>
Trigger a pipeline
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/pipelines/settings.html>
Pipeline settings
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/pipelines/pipeline_architectures.html>
Pipeline architectures
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/pipelines/pipeline_efficiency.html>
Pipeline efficiency
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/directed_acyclic_graph/>
Directed acyclic graph (DAG)
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/multi_project_pipelines.html>
Multi-project pipelines
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/parent_child_pipelines.html>
Parent-child pipelines
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/merge_request_pipelines/>
Pipelines for merge requests
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/merge_request_pipelines/pipelines_for_merged_results/>
Pipelines for merged results
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/merge_request_pipelines/pipelines_for_merged_results/merge_trains/>
Merge trains
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/ci/jobs/>
Jobs
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_369b1fc7-4de7-4c15-8765-f0193ea34fa4></div>
</span>
<div class=collapse id=doc_369b1fc7-4de7-4c15-8765-f0193ea34fa4>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/jobs/job_control.html>
Choose when jobs run
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/interactive_web_terminal/>
Access a terminal for a running job
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/yaml/script.html>
Format scripts and job logs
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/git_submodules.html>
Git submodules
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/ci/variables/README.html>
Variables
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_e33e888b-4e5c-4ebe-a91f-417d703a16fe></div>
</span>
<div class=collapse id=doc_e33e888b-4e5c-4ebe-a91f-417d703a16fe>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/variables/predefined_variables.html>
Predefined variables
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/variables/where_variables_can_be_used.html>
Where variables can be used
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/ci/environments/>
Environments and deployments
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_d9f99245-b107-41f0-8c38-bee25ece7276></div>
</span>
<div class=collapse id=doc_d9f99245-b107-41f0-8c38-bee25ece7276>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/environments/environments_dashboard.html>
Environments Dashboard
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/environments/protected_environments.html>
Protected environments
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/environments/deployment_safety.html>
Deployment safety
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/environments/incremental_rollouts.html>
Roll out an application incrementally
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/cloud_deployment/>
Deploy to AWS
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/review_apps/>
Review Apps
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/ci/runners/README.html>
Runners
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_5d939399-ba8b-4fee-91be-c499ddfaeb06></div>
</span>
<div class=collapse id=doc_5d939399-ba8b-4fee-91be-c499ddfaeb06>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/large_repositories/>
Best practices for large repositories
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/ci/caching/>
Cache and artifacts
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_294f19fe-4ac8-44c5-8850-63dda3342d81></div>
</span>
<div class=collapse id=doc_294f19fe-4ac8-44c5-8850-63dda3342d81>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/pipelines/job_artifacts.html>
Job artifacts
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/pipelines/pipeline_artifacts.html>
Pipeline artifacts
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/ci/yaml/gitlab_ci_yaml.html>
.gitlab-ci.yml
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_4341afa4-5ba7-4ea0-a5de-5d08a1b09fac></div>
</span>
<div class=collapse id=doc_4341afa4-5ba7-4ea0-a5de-5d08a1b09fac>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/yaml/README.html>
.gitlab-ci.yml reference
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/lint.html>
Validate syntax
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/pipeline_editor/>
Pipeline Editor
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/yaml/includes.html>
Include examples
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/ci/docker/>
Docker
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_0d8d3f57-cb53-4347-bfff-3a1d844e0fc9></div>
</span>
<div class=collapse id=doc_0d8d3f57-cb53-4347-bfff-3a1d844e0fc9>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/docker/using_docker_images.html>
Run CI/CD jobs in Docker containers
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/docker/using_docker_build.html>
Use Docker to build Docker images
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/docker/using_kaniko.html>
Use kaniko to build Docker images
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/ci/services/>
Services
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_fadfa17c-0a42-4379-a809-58da7339f3da></div>
</span>
<div class=collapse id=doc_fadfa17c-0a42-4379-a809-58da7339f3da>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/services/mysql.html>
MySQL service
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/services/postgres.html>
PostgreSQL service
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/services/redis.html>
Redis service
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/services/gitlab.html>
GitLab as a service
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/topics/autodevops/>
Auto DevOps
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_8eb389c1-2439-4232-b18e-3001d7621e45></div>
</span>
<div class=collapse id=doc_8eb389c1-2439-4232-b18e-3001d7621e45>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/topics/autodevops/quick_start_guide.html>
Get started
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/topics/autodevops/requirements.html>
Requirements
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/topics/autodevops/stages.html>
Stages
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/topics/autodevops/customize.html>
Customize
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/topics/autodevops/upgrading_postgresql.html>
Upgrade PostgreSQL
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/topics/autodevops/upgrading_auto_deploy_dependencies.html>
Upgrade Auto Deploy dependencies
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/topics/autodevops/troubleshooting.html>
Troubleshooting
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/ci/unit_test_reports.html>
Testing
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_1c4d871b-8467-4ae5-b0b5-eb4c76bf528c></div>
</span>
<div class=collapse id=doc_1c4d871b-8467-4ae5-b0b5-eb4c76bf528c>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/project/merge_requests/accessibility_testing.html>
Accessibility testing
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/project/merge_requests/browser_performance_testing.html>
Browser performance testing
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/project/merge_requests/code_quality.html>
Code quality
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/project/merge_requests/load_performance_testing.html>
Load performance testing
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/metrics_reports.html>
Metrics reports
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/test_cases/>
Test cases
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/ci/ci_cd_for_external_repos/>
External integrations
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_313ccf36-6b26-4227-b49a-80888093c7da></div>
</span>
<div class=collapse id=doc_313ccf36-6b26-4227-b49a-80888093c7da>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/ssh_keys/>
SSH keys
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/ci_cd_for_external_repos/bitbucket_integration.html>
Bitbucket Cloud
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/ci_cd_for_external_repos/github_integration.html>
GitHub
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/chatops/>
Slack
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/ci/examples/README.html>
CI/CD examples
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_d6b3c737-288d-4ee0-a316-71f159de3787></div>
</span>
<div class=collapse id=doc_d6b3c737-288d-4ee0-a316-71f159de3787>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/examples/deployment/README.html>
Deployment with Dpl
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/examples/end_to_end_testing_webdriverio/>
End-to-end testing
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/examples/semantic-release.html>
NPM with semantic-release
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/examples/php.html>
PHP with PHPunit and atoum
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/examples/deployment/composer-npm-deploy.html>
PHP with NPM and SCP
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/ci/examples/laravel_with_gitlab_and_envoy/>
PHP with Laravel and Envoy
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/ci/troubleshooting.html>
Troubleshooting CI/CD
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_fb0a0c32-888f-4b40-9a64-c881ec050321></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/user/packages/>
Packages & Registries
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_380f5942-af3a-41da-9725-df0d5eeb4fb5></div>
</span>
<div class=collapse id=doc_380f5942-af3a-41da-9725-df0d5eeb4fb5>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/user/packages/package_registry/>
Package Registry
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_f7f2f081-12eb-48e0-a6e7-75508e145ff1></div>
</span>
<div class=collapse id=doc_f7f2f081-12eb-48e0-a6e7-75508e145ff1>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/packages/composer_repository/>
Composer
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/packages/conan_repository/>
Conan
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/packages/go_proxy/>
Go Proxy
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/packages/maven_repository/>
Maven
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/packages/npm_registry/>
npm
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/packages/nuget_repository/>
NuGet
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/packages/pypi_repository/>
PyPI
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/packages/rubygems_registry/>
Ruby gems
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/packages/generic_packages/>
Generic
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/packages/workflows/project_registry.html>
Store all packages in one project
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/packages/container_registry/>
Container Registry
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0f1f4611-d4c4-4d18-b32f-c79d68ea0d34></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/packages/dependency_proxy/>
Dependency Proxy
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3bfb6d25-9adc-4a30-a78f-d8fafb246e41></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/user/project/clusters/>
Application infrastructure
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_711a1f09-0489-4ed7-8483-da8de495a709></div>
</span>
<div class=collapse id=doc_711a1f09-0489-4ed7-8483-da8de495a709>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/user/project/clusters/add_remove_clusters.html>
Adding and removing clusters
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_ca517901-7d5c-41af-a3d4-d24f78416886></div>
</span>
<div class=collapse id=doc_ca517901-7d5c-41af-a3d4-d24f78416886>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/project/clusters/add_eks_clusters.html>
Add EKS clusters
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/project/clusters/add_gke_clusters.html>
Add GKE clusters
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/group/clusters/>
Group-level clusters
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_433d7fcf-82c5-4999-b33d-362529192406></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/instance/clusters/>
Instance-level clusters
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_47e86301-0ae3-4ca5-a2d0-3a93efd4a376></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/canary_deployments.html>
Canary deployments
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b1d5ea85-57f0-4a98-897d-fe56f5beb71e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/clusters/environments.html>
Cluster environments
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9f10ec32-bc19-4a4b-93e0-c010b1049f64></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/clusters/cost_management.html>
Cluster cost management
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e005e77d-f2bc-4c84-aca4-64094d063c93></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/deploy_boards.html>
Deploy boards
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_42b9c192-b363-4e35-bf00-cec18bdffde3></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/user/clusters/applications.html>
GitLab Managed Apps
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_922f0e73-223c-4dbd-a243-91126779c2c3></div>
</span>
<div class=collapse id=doc_922f0e73-223c-4dbd-a243-91126779c2c3>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/clusters/crossplane.html>
Configuring Crossplane
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/user/infrastructure/>
Infrastructure as code
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_661cd396-7807-4ea6-9fba-0af9c498572d></div>
</span>
<div class=collapse id=doc_661cd396-7807-4ea6-9fba-0af9c498572d>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/infrastructure/terraform_state.html>
GitLab managed Terraform state
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/infrastructure/mr_integration.html>
Terraform integration in merge requests
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/user/clusters/agent/>
Kubernetes Agent
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_0bc8f5cc-d9ed-40bf-a278-25673426367c></div>
</span>
<div class=collapse id=doc_0bc8f5cc-d9ed-40bf-a278-25673426367c>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/clusters/agent/repository.html>
Agent configuration repository
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/clusters/management_project.html>
Management project
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1b5fb48b-c5c1-4ba0-8fac-630c1cf5fd83></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/clusters/kubernetes_pod_logs.html>
Pod logs
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c9261d9b-50e7-4437-8453-97ae00e63314></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/clusters/runbooks/>
Runbooks
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0045d794-2378-48e2-814f-2a5c37283d16></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/user/project/clusters/serverless/>
Serverless
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_8a86d7da-7bbe-48f3-bf81-7c1d16a1beeb></div>
</span>
<div class=collapse id=doc_8a86d7da-7bbe-48f3-bf81-7c1d16a1beeb>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/project/clusters/serverless/aws.html>
Deploying AWS Lambda functions
</a>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/user/project/clusters/protect/>
Securing your deployed applications
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_232ffe64-8f21-4cdd-bd27-a3e97c65fb68></div>
</span>
<div class=collapse id=doc_232ffe64-8f21-4cdd-bd27-a3e97c65fb68>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/project/clusters/protect/web_application_firewall/>
Web Application Firewall
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/project/clusters/protect/container_network_security/>
Container Network Security
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/user/project/clusters/protect/container_host_security/>
Container Host Security
</a>
</span>
</div>
</div>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/user/application_security/>
Secure your application
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_f38846ac-6811-422f-89e1-c75b0856e00b></div>
</span>
<div class=collapse id=cat_f38846ac-6811-422f-89e1-c75b0856e00b>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/application_security/configuration/>
Security Configuration
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_72d684ec-1f0e-4628-a24e-4d308382d612></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/code_owners.html>
Code owners
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ab6b520a-69ee-4f62-937b-4a64d9ab3764></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/application_security/container_scanning/>
Container Scanning
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_befe2b2d-bd39-4841-9f73-20bfc97c9253></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/application_security/threat_monitoring/>
Threat Monitoring
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c8d735a0-7b99-4a38-934c-5e2a3faf6df8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/application_security/dependency_scanning/>
Dependency Scanning
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_bde112b4-cc0e-4e11-a8ab-bf2fc860e8b8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/application_security/dependency_scanning/analyzers.html>
Dependency Scanning Analyzers
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_aa2a3558-936c-4256-a3b3-14e975b14deb></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/application_security/dependency_list/>
Dependency List
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0a68252a-e22a-468c-9166-26ef83824206></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/application_security/sast/>
Static Application Security Testing
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_28e2e37d-66dd-4bf5-ba58-fc7191d3420d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/application_security/sast/analyzers.html>
SAST Analyzers
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_01648897-a751-43df-8628-126c4eb1efd0></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/application_security/secret_detection/>
Secret Detection
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d433f801-3a35-440e-b353-44ac02117e64></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/user/application_security/dast/>
Dynamic Application Security Testing (DAST)
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_7ca33df3-1cb7-4d74-bd2c-75dea3d3d262></div>
</span>
<div class=collapse id=doc_7ca33df3-1cb7-4d74-bd2c-75dea3d3d262>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/application_security/dast/browser_based.html>
DAST browser-based crawler
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_766063c8-e159-46bf-a944-2f6879d8547e></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/application_security/dast_api/>
DAST API
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_fb90174c-7560-4dab-9c90-161905629bfc></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/application_security/dast/dast_troubleshooting.html>
DAST Troubleshooting
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1e20f1c8-02cc-44c8-a7e2-9b7223a319f2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/user/application_security/api_fuzzing/>
API Fuzzing
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_ee60d364-683c-4bc3-8c45-18f0389d782f></div>
</span>
<div class=collapse id=doc_ee60d364-683c-4bc3-8c45-18f0389d782f>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/application_security/api_fuzzing/create_har_files.html>
HTTP Archive format
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0a93e882-0fdb-4b4e-a0ef-421837714641></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/application_security/coverage_fuzzing/>
Coverage Fuzzing
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f485baf7-f42a-4524-8eb9-11216c1cef5e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/application_security/security_dashboard/>
Security Dashboard
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_985c3bd5-f98a-4b7a-b522-72f0a6eaf403></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/application_security/offline_deployments/>
Offline Environments
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5c581829-1da2-45cc-ab47-5a429d8aba72></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/application_security/vulnerability_report/>
Vulnerability Reports
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_505d2b63-5137-4349-a1e4-302ce29e60d4></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/application_security/vulnerabilities/>
Vulnerability Pages
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_803e64ef-d909-4600-ae2b-0cce75d1e33a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/application_security/policies/>
Scan Policies
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_fdad49c4-2bd7-4c8b-9226-c39ffa3a0430></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/integrations/secure.html>
Security scanner integration
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_10fb0f43-0bb9-4530-9433-926907980d76></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/application_security/terminology/>
Secure and Protect Terminology
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_20addc6a-5c98-45e6-b670-6f693bc8690f></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/topics/release_your_application.html>
Release your application
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_20446510-36ef-433e-9840-05a53084fcf3></div>
</span>
<div class=collapse id=cat_20446510-36ef-433e-9840-05a53084fcf3>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/releases/>
Releases
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_10b75625-d2bd-4283-ac1b-50093a56b8f3></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/operations/feature_flags.html>
Feature flags
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_14ccf65e-95e4-436c-a3a2-e74fac3bc5e1></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/operations/>
Monitor application performance
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_6cdef59d-86b5-497e-aa02-2410922fb3ec></div>
</span>
<div class=collapse id=cat_6cdef59d-86b5-497e-aa02-2410922fb3ec>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/operations/error_tracking.html>
Error Tracking
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_df19dc4f-5cdb-4e3e-9bb3-b1893cf55eb6></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/operations/tracing.html>
Tracing
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_56ed2a08-cf5e-463b-b473-ec4238284a6c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/operations/product_analytics.html>
Product analytics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f27553fc-6472-4610-8a0a-dcf2d699444c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/operations/incident_management/>
Incident management
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_7f98689f-b800-441a-b855-54d156a1f6bc></div>
</span>
<div class=collapse id=doc_7f98689f-b800-441a-b855-54d156a1f6bc>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/operations/incident_management/alerts.html>
Alerts
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c97a7de7-2225-459c-983d-943ac711b1ed></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/operations/incident_management/paging.html>
Paging and notifications
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_66f039da-b28b-435d-bdcf-90497c8bef2c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/operations/incident_management/incidents.html>
Incidents
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f488c7b9-ca59-4708-ab3e-7f0147acefdc></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/operations/incident_management/integrations.html>
Integrations
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d2b79ce1-d615-4338-a816-3e0a85196e42></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/operations/incident_management/status_page.html>
Status page
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9a05caa5-fcf2-4601-b1de-97ad2455bb2c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/operations/incident_management/oncall_schedules.html>
On-call schedules
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_004e8bc9-1ea5-45d5-8c47-3aec57282bf8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3 has-collapse" href=/ee/operations/metrics/>
Metrics dashboard
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_52c1401c-fcea-42ff-b946-0bcf1e9daa19></div>
</span>
<div class=collapse id=doc_52c1401c-fcea-42ff-b946-0bcf1e9daa19>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/operations/metrics/alerts.html>
Set up alerts for metrics
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/operations/metrics/embed.html>
Embedding metrics in Markdown
</a>
</span>
<span class=nav-link>
<a class="global-nav-link level-4" href=/ee/operations/metrics/embed_grafana.html>
Embedding metrics in Grafana
</a>
</span>
</div>
</div>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/user/project/integrations/prometheus_library/>
Metrics library
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_f04cb78c-388b-45a9-bf3e-97d1a17ad679></div>
</span>
<div class=collapse id=doc_f04cb78c-388b-45a9-bf3e-97d1a17ad679>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/integrations/prometheus_library/cloudwatch.html>
Monitoring AWS resources
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_562c44ce-700c-4892-9c41-fd8df34e9468></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/integrations/prometheus_library/haproxy.html>
HAProxy
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b5300819-3267-4b8d-964a-968e7e75fd7a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/integrations/prometheus_library/kubernetes.html>
Kubernetes
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_bc763f07-ac35-4c68-96c9-cc81266f2c6b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/integrations/prometheus_library/nginx.html>
NGINX
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1d622d52-585b-431b-b0ad-8aa8939531c7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/integrations/prometheus_library/nginx_ingress.html>
NGINX Ingress
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e005a58d-5758-4063-8016-51385ed5adc2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/user/project/integrations/prometheus_library/nginx_ingress_vts.html>
NGINX Ingress VTS
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a3b6e761-d358-49c6-b802-43c912364665></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/operations/metrics/dashboards/>
Custom dashboards
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_3d1a8691-0477-4a5a-b576-32e5d4fb834b></div>
</span>
<div class=collapse id=doc_3d1a8691-0477-4a5a-b576-32e5d4fb834b>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/operations/metrics/dashboards/default.html>
GitLab-defined metrics dashboards
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0a138afe-ec94-4e6b-a301-3c7f40d36a17></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/operations/metrics/dashboards/yaml.html>
Dashboard YAML properties
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0ca0b340-71f4-4b11-a06c-2fa63a2e821a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/operations/metrics/dashboards/settings.html>
Dashboard settings
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ba027630-ccbf-448f-9d2e-4d9016a20791></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/operations/metrics/dashboards/panel_types.html>
Panel types for dashboards
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9a198ab4-fda6-4024-aff0-949dc3d17efd></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/operations/metrics/dashboards/variables.html>
Using variables
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7d6d1e1e-e8dd-47c0-8f2b-9c756817fbcb></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/operations/metrics/dashboards/develop.html>
Templates for custom dashboards
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_eba7b870-2a2c-407d-affd-597d56381f4e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/operations/metrics/dashboards/templating_variables.html>
Templating variables for dashboards
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4824f952-b339-49d6-9168-b3986c959197></div>
</span>
</div>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/user/analytics/>
Analyze GitLab usage
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_1091b170-ff2e-4292-a8e2-0590cca6db8e></div>
</span>
<div class=collapse id=cat_1091b170-ff2e-4292-a8e2-0590cca6db8e>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/analytics/ci_cd_analytics.html>
CI/CD analytics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f0cae7a6-8c4f-4645-894a-8535665f5baa></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/analytics/code_review_analytics.html>
Code review analytics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_98e8147b-31f6-4c37-9f14-9b0f0de0651d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/group/contribution_analytics/>
Contribution analytics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_cbed0d95-c9ee-40d6-9abb-d6022d31f2e5></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/analytics/dev_ops_report.html>
DevOps adoption by instance
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f091504a-b8be-4231-b9ff-581201c057f2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/group/devops_adoption/>
DevOps adoption by group
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_73c0743e-3416-4238-a7ad-fa800eaeafe6></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/project/insights/>
Insights
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_43c97650-fbad-47d2-9192-786a03bf3b75></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/analytics/issue_analytics.html>
Issue analytics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f1e7f64b-9671-4509-8f4f-f7c5eba637d9></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/group/issues_analytics/>
Issue analytics for groups
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_68e0d950-cded-420a-b5e8-969dcf518b97></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/analytics/merge_request_analytics.html>
Merge request analytics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4ec94107-4377-41bd-9b19-e3ba0e750483></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/analytics/productivity_analytics.html>
Productivity analytics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_94167084-355a-466b-ab6d-958f27b9527c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/analytics/repository_analytics.html>
Repository analytics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6dc121c2-cb11-4c13-a382-95d5db23d209></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/group/repositories_analytics/>
Repository analytics for groups
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3e2ef9da-3f3f-48b8-9f16-15a821925d65></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/admin_area/analytics/usage_trends.html>
Usage trends
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_236a613f-79c3-40be-8747-69e8f6fc02d0></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/analytics/value_stream_analytics.html>
Value stream analytics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_26a5aef1-8d8f-4d17-a704-123d0b5a77a4></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/user/group/value_stream_analytics/>
Value stream analytics for groups
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_dcb164c5-5be9-44ce-9e4b-0eecc105f709></div>
</span>
</div>
</div>
</div>
<div class=global-nav-section>
<span class="global-nav-block-top nav-link">
<a class="global-nav-link level-0 has-collapse" href=/ee/api/README.html>
Use the API
</a>
<div class="section-title collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#sec_b3d34bb0-29b2-4c2b-82fa-579f61587cb2></div>
</span>
<div class=collapse id=sec_b3d34bb0-29b2-4c2b-82fa-579f61587cb2>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/api/api_resources.html>
Resources
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_19862911-63fe-41e2-8378-a7c14d2c0b91></div>
</span>
<div class=collapse id=cat_19862911-63fe-41e2-8378-a7c14d2c0b91>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/templates/gitignores.html>
.gitignore (templates)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ae2330fb-cee5-40a8-816d-ee3c6c184357></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/templates/gitlab_ci_ymls.html>
.gitlab-ci.yml (templates)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d6c106b4-41b2-4e1e-a938-a40785508804></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/access_requests.html>
Access requests
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ba4f8030-e870-46b3-962f-077cf0848081></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/appearance.html>
Appearance (application)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7d98aee2-cf3a-49f7-b4fe-bc971b49a89b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/applications.html>
Applications
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5c6e4825-5d5a-4fc4-a9ca-41715ec3e689></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/audit_events.html>
Audit events
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_cddb758c-52bb-4730-9a6a-ae15692df175></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/avatar.html>
Avatar
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_8be0778c-576a-45e8-b62e-f4cef14d7210></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/award_emoji.html>
Award emoji
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5f26c622-e9c1-43bc-aadf-3c020095377d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/project_badges.html>
Badges (project)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_42c30263-edee-4a28-8ce0-03a5d77b90fc></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/group_badges.html>
Badges (group)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_caa29969-eb89-4ff6-9e81-0a4168ed693d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/branches.html>
Branches
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a2988738-a061-4522-aa6f-9604f4800cb2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/broadcast_messages.html>
Broadcast messages
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_cdc0e1b3-fcc8-453d-876b-dbd73d1ea4ce></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/project_clusters.html>
Clusters (project)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_714224bf-6e79-4422-8163-e10c4b4eaa0f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/group_clusters.html>
Clusters (group)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e5be68ee-19d6-48ff-b168-a6e920a48cc7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/instance_clusters.html>
Clusters (instance)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_99a9f0d0-055f-42b9-ad3f-d5bc8ea70eb8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/commits.html>
Commits
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5dc2fbce-cb8a-4691-b0de-a31a1b923e4f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/packages/composer.html>
Composer
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4588b178-0f8c-49d3-9a30-deed83312181></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/packages/conan.html>
Conan
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7942706c-70a2-45f0-a679-1c825fb3dac5></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/container_registry.html>
Container Registry
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b1c3a52a-bf1e-48cd-a6a9-4e7af7517110></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/custom_attributes.html>
Custom attributes
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_fdc30f42-f014-491a-a127-0b99a8dae244></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/metrics_dashboard_annotations.html>
Dashboard annotations
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c89ce00c-5f96-4b4b-8d09-40e0b4cd6210></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/dependencies.html>
Dependencies
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3ab95352-080c-4de9-8054-8ca119e7c8fd></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/dependency_proxy.html>
Dependency Proxy
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_368b4349-a4f1-48bd-b614-f1d7b3756c0a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/deploy_keys.html>
Deploy keys
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_8be44c6c-d4e7-480a-ac62-3c88e80c5555></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/deploy_tokens.html>
Deploy tokens
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_81e7e836-7054-41ba-ada1-395a8c96966d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/deployments.html>
Deployments
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e3a00bb0-a9c6-4afc-bfcd-0d91fa00646e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/discussions.html>
Discussions
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e843458d-f176-4f3d-bd7a-2d591b91b081></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/templates/dockerfiles.html>
Dockerfile (templates)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a79648f8-e2d5-42b9-b1d0-060f4e582f0c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/dora/metrics.html>
DORA4 metrics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3e14dea5-f852-4ea9-b840-4d91c0d128ca></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/dora4_project_analytics.html>
DORA4 project analytics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a783dd54-4046-4f92-8e1b-2b59ff58beb8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/environments.html>
Environments
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f63a9cab-a5f7-4a1d-95e5-574e072a132f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/epics.html>
Epics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3bb446ef-d5b0-41e0-81fd-5ce70377d8b0></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/error_tracking.html>
Error tracking
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f5f7d1ba-7938-4267-ba2f-de5bb4ab1906></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/events.html>
Events
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_73572c7e-cae9-4075-a70b-d99870ebf156></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/experiments.html>
Experiments
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a593188e-d642-4288-a1bf-6568d7a976a7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/feature_flags.html>
Features flags
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_715d9964-4d58-498b-ba33-2e196ca122db></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/feature_flag_user_lists.html>
Feature flag user lists
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_2088cbda-e36c-49a6-8b9b-1a6d2bbf93c9></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/freeze_periods.html>
Freeze periods
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3037e3aa-9266-4b65-ac05-91b13baf0897></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/geo_nodes.html>
Geo nodes
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_73a9792c-f2c5-4718-aabb-32b79d478567></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/pages.html>
GitLab Pages
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c3e2aeb3-8dbe-47d4-9250-e6260e0d4ad1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/packages/go_proxy.html>
Go Proxy
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_276a5a43-4094-4acd-99b3-143c979c7f9f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/group_activity_analytics.html>
Group activity analytics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c83613b7-ee18-4a2e-af35-34392262e161></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/group_import_export.html>
Group Import/Export
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9f290778-b388-4097-94ed-dd618d6f8890></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/group_relations_export.html>
Group relations export
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_216f0101-b644-4981-bff8-8fd05e629e38></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/group_repository_storage_moves.html>
Group repository storage moves
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6f13e314-201e-4d08-ba8e-9bb448e8bba9></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/group_wikis.html>
Group wikis
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4669fef7-1aec-40db-8bbc-584216727a0d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/groups.html>
Groups
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5ca94a79-79cf-4e22-bdfb-468b1b994bc2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/import.html>
Import
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9c28fcfe-65b2-42bf-bf74-8bc24ee28b9a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/instance_level_ci_variables.html>
Instance-level CI/CD variables
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ba4dc07b-9e13-4869-be23-1fb797b5160f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/invitations.html>
Invitations
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5c25ac57-b1bd-4c19-8a5d-2b8ac588942c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/boards.html>
Issue boards (project)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ba488016-0edf-425e-8a72-edfe9756eafa></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/group_boards.html>
Issue boards (group)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_46855f78-2f80-4a55-b91a-10545c6368bd></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/issues.html>
Issues
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0f540eb6-cf66-4d05-9ae9-dde20342b9ac></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/epic_issues.html>
Issues (epic)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_366f0e84-e821-4f85-8b98-4be836f180b2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/issues_statistics.html>
Issues statistics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a5f075f0-6967-40ce-965e-b47c0bc73062></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/iterations.html>
Iterations (project)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c1d47158-b832-4bf5-82c2-34037b9f4adf></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/group_iterations.html>
Iterations (group)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_553897ce-5878-42e2-a4dc-86e1ece9d0b5></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/jobs.html>
Jobs
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_20a56fa6-0c71-4359-ae96-87dd972d7a40></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/job_artifacts.html>
Job artifacts
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c4d0bf6c-02d0-4cd1-a3df-1665d33b488c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/keys.html>
Keys
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6bc4d204-0ecb-4b69-ba1c-20584c88ed06></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/labels.html>
Labels (project)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_bac84083-e0c4-4212-a1a0-56165644857b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/group_labels.html>
Labels (group)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5606efb2-ff3f-4edb-acb3-85d7d431e8d9></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/license.html>
License
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0289ccff-5706-47db-bf5a-477e7da1dc5e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/templates/licenses.html>
Licenses (templates)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_2d719a48-7477-4057-ba71-696364e84a6d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/issue_links.html>
Links (issue)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7bfee444-6ef4-4b61-9073-be25f39eae34></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/epic_links.html>
Links (epic)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c2164b33-e635-4c3e-b9e9-5ca5d205700c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/managed_licenses.html>
Managed licenses
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7d17a34b-5472-4e21-9134-d5b72ad748f1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/markdown.html>
Markdown
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_39774bcb-d36b-412c-8b4d-8e41957586ed></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/packages/maven.html>
Maven
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a17b6d17-12cb-487f-a681-f49bf9f0bc83></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/members.html>
Members
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_86647786-cf73-4163-83ca-ac522b544156></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/merge_request_approvals.html>
Merge request approvals
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3e229ba4-bfe5-4cf6-867b-0e2d423bd37a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/merge_request_context_commits.html>
Merge request context commits
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c4545082-6c74-4078-ad01-d7fc0fb521fe></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/merge_requests.html>
Merge requests
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c81dd833-d928-4c32-babd-067a00755302></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/merge_trains.html>
Merge trains
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e3df4fb9-a902-4a74-80a8-1104e07d6453></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/milestones.html>
Milestones (project)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_991005cc-dbda-47d7-8a79-5688af826987></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/group_milestones.html>
Milestones (group)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_635aece8-fc9e-48b6-8445-58ed0558b814></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/namespaces.html>
Namespaces
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ce8aacc4-84ea-4ad6-8543-f28670d834fc></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/notes.html>
Notes (comments)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b6fb5f62-5c35-473d-abce-378d7177f9e2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/notification_settings.html>
Notification settings
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d5987cac-4e85-4e3d-ac8e-45c68ed05a1b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/packages/npm.html>
npm
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e92b6ccf-3f31-46c8-98f6-b523812eeb9d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/packages/nuget.html>
NuGet
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_64a72a4a-7751-4f76-a7b1-10f7a54f1baa></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/packages.html>
Packages
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4c1f9786-af55-480c-a01d-a9e543e58c6d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/pages_domains.html>
Pages domains
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_33be3a92-9ebd-43e7-b41a-c68e18cdc423></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/personal_access_tokens.html>
Personal access tokens
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_148db18b-a2b4-47ce-9dcd-ecc363a21098></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/pipeline_schedules.html>
Pipelines schedules
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c9e31a44-f991-49a3-9609-1205a7a4f838></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/pipeline_triggers.html>
Pipeline triggers
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b66232cb-ed4b-485a-8e34-97a803b3879f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/pipelines.html>
Pipelines
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c50aa318-264c-40b6-928e-5d019b53b0e2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/plan_limits.html>
Plan limits
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_71582f92-f28a-4e4b-b103-be466bfa21d0></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/resource_access_tokens.html>
Project access tokens
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e72415f3-4ddb-4ba8-aba9-116612474c42></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/project_aliases.html>
Project aliases
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_820988e0-1f86-4951-8263-5e1bf3303e79></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/project_import_export.html>
Project import/export
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4de175a7-4088-43f7-8182-57647b328dda></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/remote_mirrors.html>
Project remote mirrors
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_2d3b64a0-8a47-4014-918f-f69b217c0d6b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/project_repository_storage_moves.html>
Project repository storage moves
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_fd173ec7-2442-453a-aad6-32e59767860a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/project_statistics.html>
Project statistics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_270f26ab-e761-4dce-b326-8346617ca48e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/project_templates.html>
Project templates
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f7d8be46-937e-4133-96ec-c1fb769e0c2f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/project_vulnerabilities.html>
Project vulnerabilities
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_78edd30d-d6de-45a8-a98d-8be209a20ee5></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/projects.html>
Projects
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5c293b1e-198f-43aa-b381-7ddf0fb8253c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/protected_branches.html>
Protected branches
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_00f20b60-eb74-416a-a855-d508f3ec97e5></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/protected_environments.html>
Protected environments
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_922354b9-302a-4d1a-bb5f-d14ba2d7442e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/protected_tags.html>
Protected tags
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b3581c00-3fcf-431a-aa05-96c1ee568e5b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/packages/pypi.html>
PyPI
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_63da4150-a56c-44fd-8fcf-f2f5c1497368></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/releases/>
Releases
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e4f50486-1d3f-444e-a363-be5c8374e7cc></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/releases/links.html>
Release links
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f98f29e2-9cf0-4c46-9b35-0d7be570205a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/repositories.html>
Repositories
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6af357aa-7308-4668-890f-8d68ad0fc14b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/repository_files.html>
Repository files
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0418049a-6092-4d43-b044-24e352e84659></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/repository_submodules.html>
Repository submodules
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_46d215f8-b050-426a-9042-6960977980b4></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/resource_iteration_events.html>
Resource iteration events
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_2ea5f9fe-e06d-4d46-96fd-0e20b3220829></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/resource_label_events.html>
Resource label events
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_8ff92667-1817-4737-aeab-1377b80759b6></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/resource_milestone_events.html>
Resource milestone events
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_971a2c79-519b-4cf2-a420-25f8a3874273></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/resource_state_events.html>
Resource state events
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_495c47fa-4ad6-4d61-9148-216656b16800></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/resource_weight_events.html>
Resource weight events
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b2c97e19-e0d7-4ce5-bb5e-fcf5604b2c82></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/packages/rubygems.html>
Ruby gems
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_efc3b0d2-dbd3-4208-8a72-953d990ea57c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/runners.html>
Runners
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7512a535-a445-4aab-ae11-f1e9be5ca667></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/scim.html>
SCIM
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a032f042-ed74-4b7d-ab60-6868e8f092c4></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/search.html>
Search
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3675509b-8ce2-4f6a-af7f-1087a8634752></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/services.html>
Services
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1b5b07bd-8e87-4e9c-b07e-d33817460984></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/settings.html>
Settings (application)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_513b4a04-c7bd-461b-8598-feadf022df16></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/sidekiq_metrics.html>
Sidekiq metrics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9fe33da4-abff-401f-aebb-0a32eaf8c80b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/admin_sidekiq_queues.html>
Sidekiq queues
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1c91601c-c5ab-4847-afed-5c8481e721ec></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/snippet_repository_storage_moves.html>
Snippet repository storage moves
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5f5c4c17-d13e-4570-a461-e2d5aa571411></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/snippets.html>
Snippets
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c7f60994-77b5-4139-91a4-aeda71d92f51></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/project_snippets.html>
Snippets (project)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_479ef495-ce37-4385-9e43-c9a3df5b4974></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/statistics.html>
Statistics (application)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6a36d1f3-ee77-4f05-b21a-77fa96b62bd1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/suggestions.html>
Suggestions
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_50728d68-7002-4d36-98a4-f152ff104bd7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/system_hooks.html>
System hooks
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_21492bb6-ae91-4791-b4a5-77ae5a739945></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/tags.html>
Tags
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_27f0f32d-cc03-4269-a220-4452d4e93be6></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/todos.html>
To-Do lists
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_350231c7-c135-4bfd-846a-9b198b155c38></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/usage_data.html>
Usage Data
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b331361f-8ab8-4deb-9395-c74e8d4122df></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/users.html>
Users
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4bf33206-dcc5-4f56-a0ef-ab1d166d6f0a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/metrics_user_starred_dashboards.html>
User-starred metrics dashboards
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1a232549-66fe-4f70-a1e4-309656803db9></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/project_level_variables.html>
Variables (project)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0d83f8d8-7611-4366-970a-86a461f3aff7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/group_level_variables.html>
Variables (group)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3a5f6a49-9d78-4653-92e5-fdd591784d96></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/version.html>
Version
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3b504d24-9c5d-45e0-9277-ccf0218dd2ee></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/visual_review_discussions.html>
Visual Review discussions
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c5083065-85d6-4ebb-9993-2b0176fb49f6></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/vulnerabilities.html>
Vulnerabilities
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_71102a83-ba5e-4d6d-b882-2ee6e2aa31d7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/vulnerability_exports.html>
Vulnerability export
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b437f7f2-8a21-45a5-bebf-27c5aa9d8a85></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/vulnerability_findings.html>
Vulnerability Findings
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a1e19b30-e988-4933-84a0-7f577f77abad></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/ee/api/wikis.html>
Wikis
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_169d12c3-63b8-4caf-acde-4871c172da0d></div>
</span>
<div class=collapse id=doc_169d12c3-63b8-4caf-acde-4871c172da0d>
<span class=nav-link>
<a class="global-nav-link level-3" href=/ee/api/group_wikis.html>
Wikis (group)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e3648e0b-ef66-42f2-9f3b-f0980e88d903></div>
</span>
</div>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/api/graphql/>
GraphQL
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_2f6ce314-6d89-4420-b624-66f18e46eb4b></div>
</span>
<div class=collapse id=cat_2f6ce314-6d89-4420-b624-66f18e46eb4b>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/graphql/getting_started.html>
Get started
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9436e014-60e7-4b1e-b033-f09c743c0051></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/graphql/reference/>
GraphQL reference
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_46f329c4-9446-4ce9-8b5a-86d864d22395></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/graphql/audit_report.html>
Create audit report (example)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d3b77866-ec99-4b3f-936f-e2b84a5c1642></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/graphql/sample_issue_boards.html>
Identify issue boards (example)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_cbd7e284-7b97-4295-9ef3-91eac2684805></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/api/graphql/removed_items.html>
Removed items
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_436c5093-c779-4c93-b2c7-27fc9114aa52></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/api/lint.html>
Lint .gitlab-ci.yml
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_5ca05bae-43df-466c-9216-d6a5ce6be45c></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/api/oauth2.html>
GitLab as an OAuth2 provider
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_87f88f05-cca1-4ef2-bffe-c04bb344c07c></div>
</span>
</div>
</div>
<div class=global-nav-section>
<span class="global-nav-block-top nav-link">
<a class="global-nav-link level-0 has-collapse" href=/runner/>
GitLab Runner
</a>
<div class="section-title collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#sec_490d0997-31c0-4333-89b4-827a3161841c></div>
</span>
<div class=collapse id=sec_490d0997-31c0-4333-89b4-827a3161841c>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/runner/install/>
Install
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_5065ad66-6962-4c81-934d-2cad62539b20></div>
</span>
<div class=collapse id=cat_5065ad66-6962-4c81-934d-2cad62539b20>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/install/docker.html>
Docker
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7f2e77a0-e519-446b-9b3c-0d6f0f36abe2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/install/freebsd.html>
FreeBSD
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_98b5f97a-0769-4689-9756-8bb7282a14bf></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/install/kubernetes.html>
Kubernetes (Helm Chart)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_bd0496b7-3340-40f9-a614-4f62330f5b84></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/install/kubernetes-agent.html>
Kubernetes (Agent)
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_13b88ab0-6732-48cb-addd-3eaf31812bb5></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/install/linux-manually.html>
Linux
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_bdd143ca-2793-40ca-8de9-cb7eb40a588b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/install/osx.html>
macOS
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_dfaed954-6a66-49fc-aa4a-53b51462fffe></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/install/openshift.html>
OpenShift
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d2bdeaaf-8945-4a27-a8a6-3c81cc76ce4a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/install/windows.html>
Windows
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_62727e4d-5b48-4102-9053-4043130ae013></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/install/bleeding-edge.html>
Bleeding edge releases
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1f9bece4-f05b-472e-bd28-8a9419f07d4f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/install/linux-repository.html>
Official Linux packages
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_72f9cc7b-fb9f-4a8a-a3c3-ce9c47270aa4></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/install/old.html>
Old GitLab Runner URLs
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_bf46e6b5-343a-4f90-a255-9c9b1cdde084></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/runner/configuration/>
Configure
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_7784c19a-2a98-4c20-9098-07ef40897a9c></div>
</span>
<div class=collapse id=cat_7784c19a-2a98-4c20-9098-07ef40897a9c>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/configuration/advanced-configuration.html>
Advanced config
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_dd613507-c847-4cdc-9e6b-9471b78161b7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/configuration/autoscale.html>
Autoscale config
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_2305f8a3-2b97-4993-9801-512048b7a84d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/configuration/runner_autoscale_aws/>
Autoscale on AWS EC2
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_61abf8fd-bde3-4c42-8104-c7d7dfd416b6></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/configuration/runner_autoscale_aws_fargate/>
Autoscale on AWS Fargate
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_fdb75c65-ccca-4f21-8f17-a6b3244b2226></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/commands/README.html>
Commands
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5b2436be-c130-46ca-b950-4e5df8f4eb12></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/configuration/feature-flags.html>
Feature flags
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b06ee254-6f77-445f-9383-a31bae65513b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/configuration/configuring_runner_openshift.html>
OpenShift
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a4ad263b-e881-4180-bb0b-069950d31486></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/configuration/proxy.html>
Running behind a proxy
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f875179d-f4bf-4ac8-a2b5-26c631f73978></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/configuration/proxy.html#handling-rate-limited-requests>
Rate limited requests
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0c30fb36-ccf4-4509-914e-a8f948d09c3b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/configuration/tls-self-signed.html>
Self-signed certificates
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e52369c9-47ae-43c2-92dd-a2304d40a629></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/configuration/init.html>
System services
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1f80cd35-0f07-4ea6-957a-c70927cc2fc5></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/configuration/speed_up_job_execution.html>
Speed up job execution
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6e40c986-e4db-4ba1-bf2e-48c9d827879a></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/runner/register/>
Register
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_cf11b011-4ea1-485c-be8a-c22f2e6f6fe3></div>
</span>
<div class=collapse id=cat_cf11b011-4ea1-485c-be8a-c22f2e6f6fe3>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/examples/gitlab.html>
Examples
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ba9f0e71-be87-4b44-b9b0-e184c17eec9a></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/runner/executors/README.html>
Executors
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_7499df0e-bc2e-4be9-bb4d-60e008a5e192></div>
</span>
<div class=collapse id=cat_7499df0e-bc2e-4be9-bb4d-60e008a5e192>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/runner/executors/custom.html>
Custom
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_49a3cb03-a9b0-4814-bed8-4dd2b8c901d5></div>
</span>
<div class=collapse id=doc_49a3cb03-a9b0-4814-bed8-4dd2b8c901d5>
<span class=nav-link>
<a class="global-nav-link level-3" href=/runner/executors/custom_examples/libvirt.html>
libvirt
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1d430f1b-8bf6-4eca-830c-2b3c1448f873></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/runner/executors/custom_examples/lxd.html>
LXD
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_588e8e1a-2a17-4ade-b15e-ec125725a8cb></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/executors/docker.html>
Docker
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1cc745a9-d5e7-4330-9212-64e8047f83b7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/executors/docker_machine.html>
Docker Machine
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0fa43bf1-326a-48b4-80eb-e4cc74661a84></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/executors/kubernetes.html>
Kubernetes
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9d4e7519-a4cf-4ef7-9764-d3f593317149></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/executors/shell.html>
Shell
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_62e33419-218a-4be2-ace0-8631db212144></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/executors/ssh.html>
SSH
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_8e033656-1a7e-4b06-8e84-86bdc4bfd2fa></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/executors/parallels.html>
Parallels
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e6943068-77dd-4488-9829-5cf8dc3635fe></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/executors/virtualbox.html>
Virtual Box
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_21ab0714-425d-42de-a206-9731f69211ef></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/runner/monitoring/README.html>
Monitor
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_bd4a7549-f79d-4dfe-9d22-764679b8ea40></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/runner/security/>
Security
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_14a9662e-76b4-46f5-a6c6-36ae63326d8a></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/runner/shells/>
Shells
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_faa588c3-5f43-4495-9a6e-2cec90a8f1b2></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/runner/faq/README.html>
Troubleshoot
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_d1b9fc18-e681-4de7-b03f-fc33bb7d2fa3></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/runner/best_practice/>
Best Practices
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_9f608dd6-d1d5-4e35-a498-1b8896ab7a8d></div>
</span>
</div>
</div>
<div class=global-nav-section>
<span class="global-nav-block-top nav-link">
<a class="global-nav-link level-0 has-collapse" href=/ee/development/README.html>
Contribute to GitLab development
</a>
<div class="section-title collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#sec_07eb87d4-1728-4582-91f6-ca99c78e3e3e></div>
</span>
<div class=collapse id=sec_07eb87d4-1728-4582-91f6-ca99c78e3e3e>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/development/contributing/>
Get started
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_c7bca71e-2e19-495c-abe0-93af5a4574c8></div>
</span>
<div class=collapse id=cat_c7bca71e-2e19-495c-abe0-93af5a4574c8>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/changelog.html>
Changelog entries
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_63172e38-d5f9-4bf7-9468-e7b772298508></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/contributing/community_roles.html>
Community roles
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5271dc2d-5bd4-4ac1-8626-cb0d38f8f608></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/contributing/design.html>
Design and UI
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5947bcdc-b687-4bd3-a664-22681e1cf856></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=https://gitlab.com/gitlab-org/gitlab-development-kit/blob/main/README.md target=_blank>
GitLab Development Kit
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d75ea334-945e-4c67-9747-c31fa8199446></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/contributing/issue_workflow.html>
Issues workflow
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_65ecee99-4efc-468b-a266-eaa6e39d8cb1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/contributing/merge_request_workflow.html>
Merge request workflow
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a21fd518-c6dc-4144-8ec2-ac86359f8325></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/code_review.html>
Code review guidelines
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0f80cfec-a453-4894-b1b0-8b958a3e1b36></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/contributing/style_guides.html>
Style guides
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_af7fb6d3-39eb-4d0a-911f-0f0233f28f89></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/approval_rules.html>
Approval rules development guide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_6753c924-53ee-4382-bffc-4b570fee36a6></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/architecture.html>
Architecture
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_54f1f8ed-959b-474d-a7b9-6b9acb6a9663></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/audit_event_guide/>
Audit Event development guide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_ed45492c-2c18-47e5-8336-96fc30d81340></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/development/cicd/>
CI/CD development
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_5a5d84b4-5ce2-47a0-9f28-50d01591d84c></div>
</span>
<div class=collapse id=cat_5a5d84b4-5ce2-47a0-9f28-50d01591d84c>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/cicd/cicd_reference_documentation_guide.html>
CI/CD reference styleguide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_89a50673-2073-4ea7-b373-7f48f8941564></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/cicd/templates.html>
CI/CD template development
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6b39f4c1-5c4c-4e5e-b785-b7ef5f54b864></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/auto_devops.html>
Auto DevOps development
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a5761c1d-d9e9-45ec-bdc5-c37fc1300f15></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/code_intelligence/>
Code intelligence
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_00fb1668-0311-46b0-b6ad-aa6257c38aae></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/dangerbot.html>
Danger bot
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_cfff8d2d-a33c-4f8d-b2a8-f83c734a4704></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/development/database/>
Database development
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_7bb5fe42-2d29-44d6-a5c4-1fed347d79b1></div>
</span>
<div class=collapse id=cat_7bb5fe42-2d29-44d6-a5c4-1fed347d79b1>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/filtering_by_label.html>
Case study - filtering by label
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4cafb77a-6eaa-4afc-99c5-401b82b4ef5d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/namespaces_storage_statistics.html>
Case study - namespaces storage statistics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5fa1ba86-6a84-4c84-9aa6-ac47d21ad6e2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/database_review.html>
Database review guidelines
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6918f1c2-4438-421c-bc29-95985c3fae16></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/migration_style_guide.html>
Migrations style guide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_de543063-c926-42af-b88e-da6d744f05e3></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/sql.html>
SQL guidelines
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_30a2c867-c13c-44fa-9010-7703d505a332></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/understanding_explain_plans.html>
Understanding EXPLAIN plans
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_56cdc3df-055f-4c76-9197-4750c00191b3></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/avoiding_downtime_in_migrations.html>
Avoiding downtime in migrations
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_09c6f28d-ab8f-4d00-8383-706724c7d487></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/logging.html>
Developer guide to logging
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_cb710dee-256d-48e6-9472-9c0e98ad8b40></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/development/rake_tasks.html>
Development Rake tasks
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_4c3c0260-e3cd-4276-a7c4-0b15b94ce72a></div>
</span>
<div class=collapse id=cat_4c3c0260-e3cd-4276-a7c4-0b15b94ce72a>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/mass_insert.html>
Mass insert Rails models
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b43f7d81-8257-4b78-ae5c-f2438d08351e></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/development/documentation/>
Documentation
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_fe62b639-6b6b-49ca-a891-086fb737a970></div>
</span>
<div class=collapse id=cat_fe62b639-6b6b-49ca-a891-086fb737a970>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/documentation/styleguide/>
Style guide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3c056c52-02ef-4be4-b6f4-1f3d85f14c37></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/documentation/graphql_styleguide.html>
GraphQL style guide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_79c9e977-666f-4464-a567-357b8a304c43></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/documentation/restful_api_styleguide.html>
RESTful API style guide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9e2c73b8-a215-4ef1-b9b3-b7328f7a4f92></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/documentation/structure.html>
Topic types
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0e4d2861-dcd9-4ff4-ac29-e1ec4f336da8></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/documentation/workflow.html>
Process
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6681a573-27be-4e24-8ebc-fb2f4fff09dd></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/documentation/testing.html>
Testing
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_17d78364-29ba-4321-bd61-1f27735bdc57></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/documentation/site_architecture/>
Site architecture
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d1abc1d3-5fc9-4253-ac61-cf48eaefff94></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/documentation/site_architecture/global_nav.html>
Global navigation
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_82b7109e-53f6-4f04-8c87-4a1d3183f029></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/documentation/site_architecture/deployment_process.html>
Deployment process
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ffaeb028-d306-4296-b6b2-4d5ae6de6160></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/distributed_tracing.html>
Distributed tracing
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_c4a1b9c9-d7e6-4b77-a95f-c3521d66b1de></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/development/experiment_guide/>
Experiments
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_63a77b22-2458-4eaf-b8db-655f5e1687f5></div>
</span>
<div class=collapse id=cat_63a77b22-2458-4eaf-b8db-655f5e1687f5>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/experiment_guide/experimentation.html>
Experimentation module
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_379402ce-6724-4a53-8549-da7758fa84fb></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/experiment_guide/gitlab_experiment.html>
GLEX
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c17bd8c5-9f21-4e60-bbde-c8eb23cd325a></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/development/feature_flags/>
Feature flags for GitLab development
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_74c45674-eab2-42bb-8a32-404af25c37a4></div>
</span>
<div class=collapse id=cat_74c45674-eab2-42bb-8a32-404af25c37a4>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/feature_flags/controls.html>
Controlling feature flags
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f1adffcd-d8d2-4bb4-a1f6-3a258b692627></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/documentation/feature_flags.html>
Documenting feature flags
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_8747b615-ea88-4877-ba55-06798f1f21e8></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/policies.html>
Framework - DeclarativePolicy
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_930e88c1-f394-4a71-ae63-fd97da6f0250></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/development/fe_guide/>
Frontend development
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_c78aeee1-8045-475e-80ee-b0cbb6138245></div>
</span>
<div class=collapse id=cat_c78aeee1-8045-475e-80ee-b0cbb6138245>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/accessibility.html>
Accessibility
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_370eeb48-2cc8-4f25-8243-5f5015705b65></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/architecture.html>
Architecture
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_78b26db5-1a64-4583-9228-5bc3ed21e0a1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/axios.html>
Axios
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_28c4672e-2d69-4e69-9d39-2a4b3f19725e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/dark_mode.html>
Dark mode
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_41b2e1b3-28f3-461f-adc1-7af64fc5c8f9></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/design_patterns.html>
Design patterns
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3a33363a-e8a4-477b-a768-15aaff49464f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/development_process.html>
Development process
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d3b97111-1710-4d9d-ab16-a6ad90f2b6bc></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/droplab/droplab.html>
Droplab
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d05788b8-8a29-4ad0-8a78-020a310201bb></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/editor_lite.html>
Editor lite
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f99a0e30-07cc-4f0e-9053-60ef3501422c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/emojis.html>
Emojis
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_20721417-24d0-4372-8ce8-6737a5257cfc></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/droplab/plugins/filter.html>
Filter
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_90d31af7-b4b8-4dbd-acf6-ca977b5b9baf></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/frontend_faq.html>
Frontend FAQ
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_011bcf67-e1b8-46c1-8494-fd51302c6bfe></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/graphql.html>
GraphQL
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a2edf71d-9b42-4dbc-8fb8-0bd75961a2cd></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/icons.html>
Icons and SVG illustrations
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f60bd343-ad01-4bff-a9ee-a5075bcf4ada></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/droplab/plugins/input_setter.html>
InputSetter
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_84989ae3-3603-4907-b4e4-5045f98ff7df></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/new_fe_guide/modules/widget_extensions.html>
Merge request widget extensions
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_037d6c1c-20d1-4a66-9c5c-04542e3e3f94></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/performance.html>
Performance
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e17fba20-58e0-49d0-9248-23d7002acbea></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/principles.html>
Principles
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6d8e2100-f912-4b01-9add-9b80492f844f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/security.html>
Security
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_fef9e4b9-8236-4a04-92a6-8a78f5c6a4c3></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/tooling.html>
Tooling
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3d1b6576-3ae7-4323-91ff-80141b1ecfd1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/vuex.html>
Vuex
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_608ebf77-f82e-48a0-8ed9-34688e89aeb6></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/vue.html>
Vue
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_55e95bfd-d9bd-4492-9c5d-f6ddca34d181></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/widgets.html>
Widgets
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_31afcef7-e867-4c07-8ba8-bf0855be08d9></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=https://gitlab.com/gitlab-org/gitlab-development-kit/blob/main/doc/howto/pages.md target=_blank>
GitLab Pages development
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_ce85ffdb-d9ff-4466-8563-516cff95c477></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/development/geo.html>
Geo development
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_cf428f0f-c98d-44fc-b62e-52c835c91033></div>
</span>
<div class=collapse id=cat_cf428f0f-c98d-44fc-b62e-52c835c91033>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/geo/framework.html>
Geo framework
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_2cee2c8b-6a31-4807-9c9a-471242bfb3e3></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/lfs.html>
Git LFS
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_9d586618-073b-4037-b2b5-cd795986ebb5></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/gitaly.html>
Gitaly development
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_bf0a898e-1c3c-4f06-be61-cbb1ffcbad2f></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=https://design.gitlab.com target=_blank>
GitLab Design System
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_45d32d99-6ebe-45e6-9c49-e4c138952116></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/development/fe_guide/style/>
GitLab development style guides
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_2457c971-ee3f-4ee2-bffe-76efed0cb2a0></div>
</span>
<div class=collapse id=cat_2457c971-ee3f-4ee2-bffe-76efed0cb2a0>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/api_styleguide.html>
API style guide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_068c9fcf-55b0-423e-9efc-15eb7eccbca1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/go_guide/>
Go standards and style guidelines
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4b920041-1a5e-4eab-9eff-ebefc8cb2020></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/api_graphql_styleguide.html>
GraphQL API style guide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a5db20d2-fe9e-427a-8eaa-ea5fd640a2b1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/shell_commands.html>
Guidelines for shell commands
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6345e65f-4f84-47eb-8969-027fafc5b5c1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/style/html.html>
HTML style guide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f682453e-4ad7-4996-b52e-0af97d2c3f38></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/style/javascript.html>
JavaScript style guide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_6726c7a4-410f-42be-9364-fb1a83aff98d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/newlines_styleguide.html>
Newlines style guide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a8875ddb-79d2-4908-9507-b9d635ff9986></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/python_guide/>
Python development guidelines
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_04f451b6-e79f-4e56-8e28-80267986b4df></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/style/scss.html>
SCSS style guide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9817b294-535d-4527-8d84-d78b8254b38f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/shell_scripting_guide/>
Shell scripting standards and style guidelines
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_79b078b4-609d-49c9-9214-6480c8d81523></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/administration/troubleshooting/sidekiq.html>
Sidekiq debugging
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b4758bad-dfb2-4f8a-b7ba-fb567a3aa833></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/sidekiq_style_guide.html>
Sidekiq style guide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1be644ae-6343-4a00-9c50-b3842f7fb4ed></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/fe_guide/style/vue.html>
Vue style guide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0211af4e-7a55-4884-af10-45168fa4df5c></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/bulk_import.html>
GitLab group migration
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_6c705ea2-0bbd-4338-b5b6-9bf050889efc></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/pipelines.html>
GitLab project pipelines
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_f32ef27b-7241-4159-b37b-502690ed705e></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/runner/development/README.html>
GitLab Runner
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_b02c2629-ff67-436a-aa62-0943c8741566></div>
</span>
<div class=collapse id=cat_b02c2629-ff67-436a-aa62-0943c8741566>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/development/reviewing-gitlab-runner.html>
Review GitLab Runner
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_782f2504-b4ff-4af9-becb-c89be012f517></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/runner/development/add-windows-version.html>
Add new Windows version support for Docker executor
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_94f51061-703f-477f-94bd-ff1db5ea9648></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/development/graphql_guide/>
GraphQL development
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_76417c46-e87e-4883-af78-ef6e1946f011></div>
</span>
<div class=collapse id=cat_76417c46-e87e-4883-af78-ef6e1946f011>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/graphql_guide/batchloader.html>
GraphQL BatchLoader
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d6856569-e239-4d53-9757-e2f8319a0d0c></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/graphql_guide/pagination.html>
GraphQL pagination
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_bc99f55d-76a4-48b4-b401-41284588e890></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/graphql_guide/graphql_pro.html>
GraphQL Pro
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ca6e6074-f12c-44ba-8f6e-7009035182a5></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/charts/development/>
Helm Charts
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_fdb01737-66ec-47f1-9549-b06ea705e7b6></div>
</span>
<div class=collapse id=cat_fdb01737-66ec-47f1-9549-b06ea705e7b6>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/charts/architecture/>
Architecture of Cloud native GitLab Helm charts
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_4776e721-4e74-48c0-8936-6d4fd5d73c0c></div>
</span>
<div class=collapse id=doc_4776e721-4e74-48c0-8936-6d4fd5d73c0c>
<span class=nav-link>
<a class="global-nav-link level-3" href=/charts/architecture/backup-restore.html>
Backup and Restore
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4dc2847a-1a30-4e59-bb02-6b6e8ca25d90></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/charts/architecture/goals.html>
Goals
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b648e9f9-0627-44a9-9f2e-ad3516ea4032></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/charts/architecture/architecture.html>
Architecture
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5ffcb72c-18ac-41c8-ba79-e67037adb1d2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/charts/architecture/decisions.html>
Design Decisions
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_9fc32d86-0bea-44d2-a602-833fc07f8907></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/charts/architecture/resource-usage.html>
Resource Usage
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_62d4d8d5-8e61-4ab9-96e1-06a4ff464ccc></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2" href=/charts/development/environment_setup.html>
Environment setup
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1c99deb5-b96e-46fc-96ea-59fb7f1bbe0b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/charts/development/style_guide.html>
Style guide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3baeca3d-59db-41fe-84b1-3dc7560e383d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/charts/development/release.html>
Versioning and release
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b298b5d9-4048-4e49-aa17-cd6511410f14></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/import_export.html>
Import/Export
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_ecf48cda-5585-4074-bcf7-fc1034b6623f></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/instrumentation.html>
Instrumenting Ruby code
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_95507f3f-49d1-44ed-b508-fa5ae458a9fd></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/internal_api.html>
Internal API
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_f6752cf3-e509-4317-bf2f-fba6df8c5799></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/issuable-like-models.html>
Issuable-like Rails models utilities
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_cc95478e-4670-484b-92ec-1ea9c43bb996></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/issue_types.html>
Issue types
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_e3926fff-af30-4a2b-b37f-7dbf99e1eac9></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/integrations/jenkins.html>
Jenkins in local environments
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_c65f4cfb-2207-4d3e-b6c4-00cdfb92e7c6></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/integrations/jira_connect.html>
Jira development environment
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_81136b94-bfbe-4a35-bcc3-927b7be1d120></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/development/agent/>
Kubernetes Agent
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_aea651a0-06f4-4bfb-b8f3-a186aebed8ea></div>
</span>
<div class=collapse id=cat_aea651a0-06f4-4bfb-b8f3-a186aebed8ea>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/agent/routing.html>
Routing kas requests
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_71fe8741-ff8a-4585-bee3-ed9712e53c51></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/agent/repository_overview.html>
Repository overview
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_626b21c5-74f3-4cc9-b079-c53cca6f14d9></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/agent/identity.html>
Identity and authentication
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_2a094437-4213-4fed-a4d5-f2236885bef4></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/agent/user_stories.html>
User stories
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_c8090391-aaa1-43b1-8ad6-cee8e2663dfa></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/agent/gitops.html>
GitOps with the Kubernetes Agent
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_fbcf20a9-196f-4267-8735-2ec9bf1bdb97></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/agent/local.html>
Running locally
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_8259292f-0c84-4fa5-ae1e-d125094c92a1></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/kubernetes.html>
Kubernetes integration
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_9262cf30-6bfd-4cad-bcd1-e664583af661></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/omnibus/development/README.html>
Omnibus GitLab
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_a7bef84f-caff-4686-8747-3c6a1bd0f10f></div>
</span>
<div class=collapse id=cat_a7bef84f-caff-4686-8747-3c6a1bd0f10f>
<span class=nav-link>
<a class="global-nav-link level-2 has-collapse" href=/>
Build locally
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#doc_5c0dbfe3-63bf-4c9b-84c2-b225382f0f0a></div>
</span>
<div class=collapse id=doc_5c0dbfe3-63bf-4c9b-84c2-b225382f0f0a>
<span class=nav-link>
<a class="global-nav-link level-3" href=/omnibus/build/build_package.html>
Build Omnibus GitLab package
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_a4272546-c27a-414f-a883-d1f564ee6ec6></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/omnibus/build/build_docker_image.html>
Build all-in-one Docker image
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_e6413999-e3f5-451c-a7f0-74c73573a2d7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-3" href=/omnibus/build/team_member_docs.html>
Information for GitLab team members
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d91212ce-c0fb-4dd0-b2c0-d8eb889cc937></div>
</span>
</div>
<span class=nav-link>
<a class="global-nav-link level-2" href=/omnibus/development/setup.html>
Set up a development environment
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_14781671-11e4-4bf0-9454-bfa616ba7f0a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/omnibus/settings/configuration.html>
Config options
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_01cb69d0-e3d9-4b6a-944c-00c6d761dc55></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/omnibus/settings/gitlab.yml.html>
Changing YAML config options
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_d7d139c1-78d6-4a0d-a1e9-c99a1d9a1d8e></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/omnibus/development/adding-deprecation-messages.html>
Adding deprecation messages
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_574ee27a-c2e7-4846-a573-5052819a3ae5></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/omnibus/development/gitlab-ctl-commands.html>
Adding new gitlab-ctl commands
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f0937fb8-d68d-47c0-ba17-ef1424760f43></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/omnibus/development/new-services.html>
Adding new services
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_90715545-3142-4932-b223-035f5cd0556a></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/omnibus/development/new-software-definition.html>
Adding new software definitions
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_7702a013-2d01-4f11-839d-0cfc8bc026da></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/omnibus/development/creating-patches.html>
Creating patches
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5a24f094-5b4b-499a-ad79-f4f88d081b3d></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/omnibus/development/managing-postgresql-versions.html>
Managing PostgreSQL versions
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1fa80275-361f-4a29-a664-742fe0899d6b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/omnibus/development/public-attributes.html>
Working with public_attributes.json
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_3766d2ff-5ca6-4c73-94d9-043c1b20ad24></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/packages.html>
Package development
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_8354538f-fcff-4823-aa4f-06ede77d8cc7></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/permissions.html>
Permissions guide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_074d83b5-3246-40bc-a16b-942f9d2960d9></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/development/testing_guide/>
Testing standards and styles
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_0ee2a3c3-8dc4-4f29-90b9-9ef0ef88feac></div>
</span>
<div class=collapse id=cat_0ee2a3c3-8dc4-4f29-90b9-9ef0ef88feac>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/testing_guide/flaky_tests.html>
Flaky tests
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_15073c9d-ca2b-45ea-850c-cb635410a410></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/testing_guide/frontend_testing.html>
Frontend testing standards and style guidelines
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b2317f91-030f-4499-9138-8c0533dbafb7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/testing_guide/ci.html>
GitLab tests in CI context
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_632da59e-59d4-46cd-9ba5-4ec5e30f90b2></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/testing_guide/review_apps.html>
Review apps
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_162dcdb7-19c4-4014-ad8e-4b5a7b56b6c7></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/testing_guide/smoke.html>
Smoke tests
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_4afc8bbd-df33-49e6-9a5d-da2346145348></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/testing_guide/best_practices.html>
Testing best practices
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_465ee4e3-5557-4b7f-9121-667d63cd6397></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/testing_guide/testing_levels.html>
Testing levels
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_bf879499-d7dd-407f-97f5-ca3a9925aea3></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/testing_guide/testing_migrations_guide.html>
Testing Rails migrations
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_379ed92e-33bd-4c25-a156-53a8463fb93b></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/testing_guide/testing_rake_tasks.html>
Testing Rake tasks
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_393c8ebf-b854-40fc-bbe7-c06c496574f0></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/development/testing_guide/end_to_end/>
Testing (end to end)
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_10b9f92d-dec9-46e0-addc-fb869d4eb2f1></div>
</span>
<div class=collapse id=cat_10b9f92d-dec9-46e0-addc-fb869d4eb2f1>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/testing_guide/end_to_end/beginners_guide.html>
Beginner's guide to writing end-to-end tests
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ab42c1e0-27df-40a9-a418-da9173d618d3></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/testing_guide/end_to_end/best_practices.html>
Best practices when writing end-to-end tests
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_cf8bb236-7555-4f45-aed3-a976e6bb230f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/testing_guide/end_to_end/dynamic_element_validation.html>
Dynamic element validation
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_fc8a704a-d24f-4863-a8a3-b73939c29a67></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/testing_guide/end_to_end/flows.html>
Flows in GitLab QA
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1d960385-f8d1-47da-bd08-f6ccbf1c5227></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/testing_guide/end_to_end/page_objects.html>
Page objects in GitLab QA
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_cce09c7f-7d41-4992-bffc-734567108705></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/testing_guide/end_to_end/resources.html>
Resource class in GitLab QA
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1663cfbe-ead1-4ac8-92a6-6630dfdd020f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/testing_guide/end_to_end/style_guide.html>
Style guide for writing end-to-end tests
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_46b75aa5-a923-4fa1-b069-10543a7e42f6></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/testing_guide/end_to_end/feature_flags.html>
Testing with feature flags
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_24dc0741-f008-48ca-bf77-2dbd9ecc3895></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/development/i18n/>
Translate GitLab
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_cf66a664-d827-4d9e-a25c-466b4cafd81c></div>
</span>
<div class=collapse id=cat_cf66a664-d827-4d9e-a25c-466b4cafd81c>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/i18n/externalization.html>
Externalization
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_0aca2e0e-f726-4ccd-bada-a21df5dc78a1></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/i18n/translation.html>
Translation
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_32a2119e-973e-40e1-adc4-1536abc6ff62></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/i18n/proofreader.html>
Proofreading
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_1ac61df8-79f8-4cf6-9b46-5a0e4ac31722></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/i18n/merging_translations.html>
Merging
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_204e96f3-2cc5-4d6e-885d-b56b606c6bbd></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/development/snowplow/>
Snowplow guide
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_2e4da3fc-5901-45ed-ae6c-e040bf098fac></div>
</span>
<div class=collapse id=cat_2e4da3fc-5901-45ed-ae6c-e040bf098fac>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/snowplow/event_dictionary_guide.html>
Event dictionary guide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_f041f90d-3bb2-4aba-a9d6-c9a5c253b999></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/snowplow/dictionary.html>
Event dictionary
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_48fe372e-b9c7-4d57-9a6f-ac4426487ea7></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1 has-collapse" href=/ee/development/usage_ping/>
Usage Ping guide
</a>
<div class="collapse-toggle collapsed" data-toggle=collapse aria-expanded=false data-target=#cat_b8062a4b-7bcd-4541-8f92-328cd1a8dd0d></div>
</span>
<div class=collapse id=cat_b8062a4b-7bcd-4541-8f92-328cd1a8dd0d>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/usage_ping/metrics_instrumentation.html>
Metrics instrumentation
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_5443c7fe-d180-4ad3-99a3-c51e1bd30735></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/usage_ping/metrics_dictionary.html>
Metrics dictionary guide
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_b31cec53-2c38-492a-ba81-78c703faca08></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/usage_ping/dictionary.html>
Metrics dictionary
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_ad3c4f94-c662-460c-80aa-3fb7be850c8f></div>
</span>
<span class=nav-link>
<a class="global-nav-link level-2" href=/ee/development/usage_ping/product_intelligence_review.html>
Product Intelligence review
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#doc_86b454cc-0809-4200-93f2-b99fa8de49c6></div>
</span>
</div>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/value_stream_analytics.html>
Value Stream Analytics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_88c7f778-e1ac-4db3-a410-98f68854d712></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/wikis.html>
Wikis
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_2bd0a23d-5b72-40de-a3fc-e4a078559079></div>
</span>
<span class="global-nav-cat nav-link">
<a class="global-nav-link level-1" href=/ee/development/prometheus_metrics.html>
Working with Prometheus metrics
</a>
<div class=collapsed data-toggle=collapse aria-expanded=false data-target=#cat_48be02b1-2bb6-4274-9900-4ee0ec2fe404></div>
</span>
</div>
</div>
</nav>
</aside>
<div id=js-nav-toggle></div>
</div>
</div>
<div class="main class pl-lg-4 wrapper js-main-wrapper col-12 col-lg-7">
<div class=row>
<div class=col>
<div id=js-version-banner data-latest-version-url=/ee/user/project/repository/gpg_signed_commits/index.html data-archives-url=/archives/></div>
</div>
</div>
<div class=row>
<div class=col>
</div>
</div>
<div class=row>
<div class=col>
<div class="my-3 my-lg-0">
<a class="position-absolute text-muted mt-2 pt-1 text-decoration-none border-bottom-0 mobile-nav-toggle" href=#><i class="fa fa-bars fa-lg" aria-hidden=true></i> | </a>
<div class="gl-breadcrumbs d-flex w-100">
<img src="https://assets.gitlab-static.net/uploads/-/system/group/avatar/9970/logo-extra-whitespace.png?width=15" class=gl-breadcrumb-avatar-tile alt>
<ol class="breadcrumb gl-breadcrumb-list ml-1 mt-0 pl-0">
<li class=gl-breadcrumb-item><a href=/ee/README.html>GitLab Docs</a>
<span data-testid=separator class=gl-breadcrumb-separator><svg viewBox="0 0 16 16"><path d="M9.9 8.064 5.656 3.821A1 1 0 0 1 7.07 2.407l4.95 4.95a1 1 0 0 1 0 1.414l-4.95 4.95a1 1 0 0 1-1.414-1.414l4.242-4.243z" fill-rule="evenodd"/></svg></span>
<li class=gl-breadcrumb-item><a href=/ee/user/>User Docs</a>
<span data-testid=separator class=gl-breadcrumb-separator><svg viewBox="0 0 16 16"><path d="M9.9 8.064 5.656 3.821A1 1 0 0 1 7.07 2.407l4.95 4.95a1 1 0 0 1 0 1.414l-4.95 4.95a1 1 0 0 1-1.414-1.414l4.242-4.243z" fill-rule="evenodd"/></svg></span>
<li class=gl-breadcrumb-item><a href=/ee/user/project/>Organize work with projects</a>
<span data-testid=separator class=gl-breadcrumb-separator><svg viewBox="0 0 16 16"><path d="M9.9 8.064 5.656 3.821A1 1 0 0 1 7.07 2.407l4.95 4.95a1 1 0 0 1 0 1.414l-4.95 4.95a1 1 0 0 1-1.414-1.414l4.242-4.243z" fill-rule="evenodd"/></svg></span>
<li class=gl-breadcrumb-item><a href=/ee/user/project/repository/>Repository</a>
<span data-testid=separator class=gl-breadcrumb-separator><svg viewBox="0 0 16 16"><path d="M9.9 8.064 5.656 3.821A1 1 0 0 1 7.07 2.407l4.95 4.95a1 1 0 0 1 0 1.414l-4.95 4.95a1 1 0 0 1-1.414-1.414l4.242-4.243z" fill-rule="evenodd"/></svg></span>
<li class=gl-breadcrumb-item>Signing commits with GPG
</ol>
</div>
</div>
</div>
</div>
<div class="row d-lg-none">
<div class=col>
<div class=doc-nav></div>
</div>
</div>
<main>
<div class=row>
<div class=col>
<div class=article-metadata>
</div>
<div class="article-content js-article-content" role=main itemscope itemprop=mainContentOfPage>
<ul id=markdown-toc>
<li><a href=#how-gitlab-handles-gpg id=markdown-toc-how-gitlab-handles-gpg>How GitLab handles GPG</a>
<li><a href=#generating-a-gpg-key id=markdown-toc-generating-a-gpg-key>Generating a GPG key</a>
<li><a href=#adding-a-gpg-key-to-your-account id=markdown-toc-adding-a-gpg-key-to-your-account>Adding a GPG key to your account</a>
<li><a href=#associating-your-gpg-key-with-git id=markdown-toc-associating-your-gpg-key-with-git>Associating your GPG key with Git</a>
<li><a href=#signing-commits id=markdown-toc-signing-commits>Signing commits</a>
<li><a href=#verifying-commits id=markdown-toc-verifying-commits>Verifying commits</a>
<li><a href=#revoking-a-gpg-key id=markdown-toc-revoking-a-gpg-key>Revoking a GPG key</a>
<li><a href=#removing-a-gpg-key id=markdown-toc-removing-a-gpg-key>Removing a GPG key</a>
<li><a href=#rejecting-commits-that-are-not-signed id=markdown-toc-rejecting-commits-that-are-not-signed>Rejecting commits that are not signed <span class="badge-trigger premium"></span></a>
<li><a href=#gpg-signing-api id=markdown-toc-gpg-signing-api>GPG signing API</a>
<li><a href=#further-reading id=markdown-toc-further-reading>Further reading</a>
</ul>
<h1 id=signing-commits-with-gpg>Signing commits with GPG <span class="badge-trigger free"></span><a href=#signing-commits-with-gpg title=Permalink class=anchor></a>
</h1>
<div class="introduced-in mb-3">Version history<button class=text-expander type=button data-toggle=collapse data-target=#release_version_notes_1 aria-expanded=false aria-controls=release_version_notes_1 aria-label="Version history"></button><div class="introduced-in-content collapse" id=release_version_notes_1>
<ul>
<li>
<a href=https://gitlab.com/gitlab-org/gitlab-foss/-/merge_requests/9546>Introduced</a> in GitLab 9.5.
<li>Subkeys support was added in GitLab 10.1.
</ul>
</div>
</div>
<p>You can use a GPG key to sign Git commits made in a GitLab repository. Signed
commits are labeled <strong>Verified</strong> if the identity of the committer can be
verified. To verify the identity of a committer, GitLab requires their public
GPG key.
<div class="mt-3 admonition-wrapper note"><div class="admonition alert alert-info">
<svg role="img" aria-label="note" class="gl-icon ml-1 mr-1 s16"><use href="/assets/images/icons.svg#information-o"/><title>note</title></svg>The term GPG is used for all OpenPGP/PGP/GPG related material and
implementations.</div></div>
<p>GPG verified tags are not supported yet.
<p>See the <a href=#further-reading>further reading</a> section for more details on GPG.
<h2 id=how-gitlab-handles-gpg>How GitLab handles GPG<a href=#how-gitlab-handles-gpg title=Permalink class=anchor></a>
</h2>
<p>GitLab uses its own keyring to verify the GPG signature. It does not access any
public key server.
<p>For a commit to be verified by GitLab:
<ul>
<li>The committer must have a GPG public/private key pair.
<li>The committer’s public key must have been uploaded to their GitLab
account.
<li>One of the emails in the GPG key must match a <strong>verified</strong> email address
used by the committer in GitLab.
<li>The committer’s email address must match the verified email address from the
GPG key.
</ul>
<h2 id=generating-a-gpg-key>Generating a GPG key<a href=#generating-a-gpg-key title=Permalink class=anchor></a>
</h2>
<p>If you don’t already have a GPG key, the following steps can help you get
started:
<ol>
<li>
<a href=https://www.gnupg.org/download/index.html>Install GPG</a> for your operating system.
If your operating system has <code class=highlighter-rouge>gpg2</code> installed, replace <code class=highlighter-rouge>gpg</code> with <code class=highlighter-rouge>gpg2</code> in
the following commands.
<li>
<p>Generate the private/public key pair with the following command, which will
spawn a series of questions:
<div class="language-shell highlighter-rouge">
<div class=highlight><pre class=highlight><code>gpg <span class=nt>--full-gen-key</span>
</code></pre></div> </div>
<div class="mt-3 admonition-wrapper note"><div class="admonition alert alert-info">
<svg role="img" aria-label="note" class="gl-icon ml-1 mr-1 s16"><use href="/assets/images/icons.svg#information-o"/><title>note</title></svg>In some cases like Gpg4win on Windows and other macOS versions, the command
here may be <code class=highlighter-rouge>gpg --gen-key</code>.</div></div>
<li>
<p>The first question is which algorithm can be used. Select the kind you want
or press <kbd>Enter</kbd> to choose the default (RSA and RSA):
<div class="language-plaintext highlighter-rouge">
<div class=highlight><pre class=highlight><code>Please select what kind of key you want:
   (1) RSA and RSA (default)
   (2) DSA and Elgamal
   (3) DSA (sign only)
   (4) RSA (sign only)
Your selection? 1
</code></pre></div> </div>
<li>
<p>The next question is key length. We recommend you choose <code class=highlighter-rouge>4096</code>:
<div class="language-plaintext highlighter-rouge">
<div class=highlight><pre class=highlight><code>RSA keys may be between 1024 and 4096 bits long.
What keysize do you want? (2048) 4096
Requested keysize is 4096 bits
</code></pre></div> </div>
<li>
<p>Specify the validity period of your key. This is something
subjective, and you can use the default value, which is to never expire:
<div class="language-plaintext highlighter-rouge">
<div class=highlight><pre class=highlight><code>Please specify how long the key should be valid.
         0 = key does not expire
      &lt;n&gt;  = key expires in n days
      &lt;n&gt;w = key expires in n weeks
      &lt;n&gt;m = key expires in n months
      &lt;n&gt;y = key expires in n years
Key is valid for? (0) 0
Key does not expire at all
</code></pre></div> </div>
<li>
<p>Confirm that the answers you gave were correct by typing <code class=highlighter-rouge>y</code>:
<div class="language-plaintext highlighter-rouge">
<div class=highlight><pre class=highlight><code>Is this correct? (y/N) y
</code></pre></div> </div>
<li>
<p>Enter your real name, the email address to be associated with this key
(should match a verified email address you use in GitLab) and an optional
comment (press <kbd>Enter</kbd> to skip):
<div class="language-plaintext highlighter-rouge">
<div class=highlight><pre class=highlight><code>GnuPG needs to construct a user ID to identify your key.

Real name: Mr. Robot
Email address: &lt;your_email&gt;
Comment:
You selected this USER-ID:
    "Mr. Robot &lt;your_email&gt;"

Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? O
</code></pre></div> </div>
<li>Pick a strong password when asked and type it twice to confirm.
<li>
<p>Use the following command to list the private GPG key you just created:
<div class="language-shell highlighter-rouge">
<div class=highlight><pre class=highlight><code>gpg <span class=nt>--list-secret-keys</span> <span class=nt>--keyid-format</span> LONG &lt;your_email&gt;
</code></pre></div> </div>
<p>Replace <code class=highlighter-rouge>&lt;your_email&gt;</code> with the email address you entered above.
<li>
<p>Copy the GPG key ID that starts with <code class=highlighter-rouge>sec</code>. In the following example, that’s
<code class=highlighter-rouge>30F2B65B9246B6CA</code>:
<div class="language-plaintext highlighter-rouge">
<div class=highlight><pre class=highlight><code>sec   rsa4096/30F2B65B9246B6CA 2017-08-18 [SC]
      D5E4F29F3275DC0CDA8FFC8730F2B65B9246B6CA
uid                   [ultimate] Mr. Robot &lt;your_email&gt;
ssb   rsa4096/B7ABC0813E4028C0 2017-08-18 [E]
</code></pre></div> </div>
<li>
<p>Export the public key of that ID (replace your key ID from the previous step):
<div class="language-shell highlighter-rouge">
<div class=highlight><pre class=highlight><code>gpg <span class=nt>--armor</span> <span class=nt>--export</span> 30F2B65B9246B6CA
</code></pre></div> </div>
<li>Finally, copy the public key and <a href=#adding-a-gpg-key-to-your-account>add it in your user settings</a>
</ol>
<h2 id=adding-a-gpg-key-to-your-account>Adding a GPG key to your account<a href=#adding-a-gpg-key-to-your-account title=Permalink class=anchor></a>
</h2>
<div class="mt-3 admonition-wrapper note"><div class="admonition alert alert-info">
<svg role="img" aria-label="note" class="gl-icon ml-1 mr-1 s16"><use href="/assets/images/icons.svg#information-o"/><title>note</title></svg>After you add a key, you cannot edit it, only remove it. In case the paste
didn’t work, you have to remove the offending key and re-add it.</div></div>
<p>You can add a GPG key in your user settings:
<ol>
<li>In the top-right corner, select your avatar.
<li>Select <strong>Edit profile</strong>.
<li>In the left sidebar, select <strong>GPG Keys</strong>.
<li>
<p>Paste your <em>public</em> key in the <strong>Key</strong> text box.
<p><a href=img/profile_settings_gpg_keys_paste_pub.png target=_blank rel="noopener noreferrer"><img src=img/profile_settings_gpg_keys_paste_pub.png alt="Paste GPG public key"></a>
<li>
<p>Select <strong>Add key</strong> to add it to GitLab. You can see the key’s fingerprint, the corresponding
email address, and creation date.
<p><a href=img/profile_settings_gpg_keys_single_key.png target=_blank rel="noopener noreferrer"><img src=img/profile_settings_gpg_keys_single_key.png alt="GPG key single page"></a>
</ol>
<h2 id=associating-your-gpg-key-with-git>Associating your GPG key with Git<a href=#associating-your-gpg-key-with-git title=Permalink class=anchor></a>
</h2>
<p>After you have <a href=#generating-a-gpg-key>created your GPG key</a> and <a href=#adding-a-gpg-key-to-your-account>added it to
your account</a>, it’s time to tell Git which
key to use.
<ol>
<li>
<p>Use the following command to list the private GPG key you just created:
<div class="language-shell highlighter-rouge">
<div class=highlight><pre class=highlight><code>gpg <span class=nt>--list-secret-keys</span> <span class=nt>--keyid-format</span> LONG &lt;your_email&gt;
</code></pre></div> </div>
<p>Replace <code class=highlighter-rouge>&lt;your_email&gt;</code> with the email address you entered above.
<li>
<p>Copy the GPG key ID that starts with <code class=highlighter-rouge>sec</code>. In the following example, that’s
<code class=highlighter-rouge>30F2B65B9246B6CA</code>:
<div class="language-plaintext highlighter-rouge">
<div class=highlight><pre class=highlight><code>sec   rsa4096/30F2B65B9246B6CA 2017-08-18 [SC]
      D5E4F29F3275DC0CDA8FFC8730F2B65B9246B6CA
uid                   [ultimate] Mr. Robot &lt;your_email&gt;
ssb   rsa4096/B7ABC0813E4028C0 2017-08-18 [E]
</code></pre></div> </div>
<li>
<p>Tell Git to use that key to sign the commits:
<div class="language-shell highlighter-rouge">
<div class=highlight><pre class=highlight><code>git config <span class=nt>--global</span> user.signingkey 30F2B65B9246B6CA
</code></pre></div> </div>
<p>Replace <code class=highlighter-rouge>30F2B65B9246B6CA</code> with your GPG key ID.
<li>
<p>(Optional) If Git is using <code class=highlighter-rouge>gpg</code> and you get errors like <code class=highlighter-rouge>secret key not available</code>
or <code class=highlighter-rouge>gpg: signing failed: secret key not available</code>, run the following command to
change to <code class=highlighter-rouge>gpg2</code>:
<div class="language-shell highlighter-rouge">
<div class=highlight><pre class=highlight><code>git config <span class=nt>--global</span> gpg.program gpg2
</code></pre></div> </div>
</ol>
<h2 id=signing-commits>Signing commits<a href=#signing-commits title=Permalink class=anchor></a>
</h2>
<p>After you have <a href=#generating-a-gpg-key>created your GPG key</a> and <a href=#adding-a-gpg-key-to-your-account>added it to
your account</a>, you can start signing your
commits:
<ol>
<li>
<p>Commit like you used to, the only difference is the addition of the <code class=highlighter-rouge>-S</code> flag:
<div class="language-shell highlighter-rouge">
<div class=highlight><pre class=highlight><code>git commit <span class=nt>-S</span> <span class=nt>-m</span> <span class=s2>"My commit msg"</span>
</code></pre></div> </div>
<li>Enter the passphrase of your GPG key when asked.
<li>Push to GitLab and check that your commits <a href=#verifying-commits>are verified</a>.
</ol>
<p>If you don’t want to type the <code class=highlighter-rouge>-S</code> flag every time you commit, you can tell Git
to sign your commits automatically:
<div class="language-shell highlighter-rouge"><div class=highlight><pre class=highlight><code>git config <span class=nt>--global</span> commit.gpgsign <span class=nb>true</span>
</code></pre></div></div>
<h2 id=verifying-commits>Verifying commits<a href=#verifying-commits title=Permalink class=anchor></a>
</h2>
<ol>
<li>
<p>Within a project or <a href=../../merge_requests/index.html>merge request</a>, navigate to
the <strong>Commits</strong> tab. Signed commits show a badge containing either
<strong>Verified</strong> or <strong>Unverified</strong>, depending on the verification status of the GPG
signature.
<p><a href=img/project_signed_and_unsigned_commits.png target=_blank rel="noopener noreferrer"><img src=img/project_signed_and_unsigned_commits.png alt="Signed and unsigned commits"></a>
<li>
<p>By clicking on the GPG badge, details of the signature are displayed.
<p><a href=img/project_signed_commit_verified_signature.png target=_blank rel="noopener noreferrer"><img src=img/project_signed_commit_verified_signature.png alt="Signed commit with verified signature"></a>
<p><a href=img/project_signed_commit_unverified_signature.png target=_blank rel="noopener noreferrer"><img src=img/project_signed_commit_unverified_signature.png alt="Signed commit with verified signature"></a>
</ol>
<h2 id=revoking-a-gpg-key>Revoking a GPG key<a href=#revoking-a-gpg-key title=Permalink class=anchor></a>
</h2>
<p>Revoking a key <strong>unverifies</strong> already signed commits. Commits that were
verified by using this key changes to an unverified state. Future commits
stay unverified after you revoke this key. This action should be used
in case your key has been compromised.
<p>To revoke a GPG key:
<ol>
<li>In the top-right corner, select your avatar.
<li>Select <strong>Edit profile</strong>.
<li>In the left sidebar, select <strong>GPG Keys</strong>.
<li>Select <strong>Revoke</strong> next to the GPG key you want to delete.
</ol>
<h2 id=removing-a-gpg-key>Removing a GPG key<a href=#removing-a-gpg-key title=Permalink class=anchor></a>
</h2>
<p>Removing a key <strong>does not unverify</strong> already signed commits. Commits that were
verified by using this key stay verified. Only unpushed commits stay
unverified after you remove this key. To unverify already signed commits, you need
to <a href=#revoking-a-gpg-key>revoke the associated GPG key</a> from your account.
<p>To remove a GPG key from your account:
<ol>
<li>In the top-right corner, select your avatar.
<li>Select <strong>Edit profile</strong>.
<li>In the left sidebar, select <strong>GPG Keys</strong>.
<li>Select the trash icon (<svg role="img" class="gl-icon ml-1 mr-1 s16"><use href="/assets/images/icons.svg#remove"/><title/></svg>) next to the GPG key you want to delete.
</ol>
<h2 id=rejecting-commits-that-are-not-signed>Rejecting commits that are not signed <span class="badge-trigger premium"></span><a href=#rejecting-commits-that-are-not-signed title=Permalink class=anchor></a>
</h2>
<p>You can configure your project to reject commits that aren’t GPG-signed
via <a href=../../../../push_rules/push_rules.html>push rules</a>.
<h2 id=gpg-signing-api>GPG signing API<a href=#gpg-signing-api title=Permalink class=anchor></a>
</h2>
<p>Learn how to <a href=../../../../api/commits.html#get-gpg-signature-of-a-commit>get the GPG signature from a commit via API</a>.
<h2 id=further-reading>Further reading<a href=#further-reading title=Permalink class=anchor></a>
</h2>
<p>For more details about GPG, see:
<ul>
<li><a href=https://git-scm.com/book/en/v2/Git-Tools-Signing-Your-Work>Git Tools - Signing Your Work</a>
<li><a href=https://riseup.net/en/security/message-security/openpgp/gpg-keys>Managing OpenPGP Keys</a>
<li><a href=https://riseup.net/en/security/message-security/openpgp/best-practices>OpenPGP Best Practices</a>
<li>
<a href=https://www.void.gr/kargig/blog/2013/12/02/creating-a-new-gpg-key-with-subkeys/>Creating a new GPG key with subkeys</a> (advanced)
<li><a href=../../../admin_area/credentials_inventory.html#review-existing-gpg-keys>Review existing GPG keys in your instance</a>
</ul>
</div>
</div>
</div>
</main>
<div class=row>
<div class=col>
<div class="help-and-feedback-section mb-5">
<a data-toggle=collapse href=#help-feedback-content class="help-and-feedback-toggle text-decoration-none" aria-expanded=false aria-controls=help-feedback-content>
<h4 class=help-and-feedback-title id=help-and-feedback><svg role="img" class="gl-icon ml-1 mr-1 s16 help-icon"><use href="/assets/images/icons.svg#question" /><title/></svg> Help & feedback<svg role="img" class="gl-icon ml-1 mr-1 s16 toggle-icon"><use href="/assets/images/icons.svg#chevron-lg-up" /><title/></svg>
</h4>
</a>
<div class="collapse show" id=help-feedback-content>
<div class="row mt-3">
<div class=col-md-8>
<div>
<h5 class=help-and-feedback-heading>Docs</h5>
<a class=help-and-feedback-link href=https://gitlab.com/gitlab-org/gitlab/blob/master/doc/user/project/repository/gpg_signed_commits/index.md target=_blank rel="noopener noreferrer">Edit this page</a>
to fix an error or add an improvement in a merge request.<br>
<a class=help-and-feedback-link href="https://gitlab.com/gitlab-org/gitlab/-/issues/new?issue[description]=Link%20the%20doc%20and%20describe%20what%20is%20wrong%20with%20it.%0A%0A%3C!--%20Don%27t%20edit%20below%20this%20line%20--%3E%0A%0A%2Flabel%20~documentation%20~%22docs%5C-comments%22%20&issue[title]=Docs%20feedback:%20Write%20your%20title" target=_blank rel="noopener noreferrer">Create an issue</a>
to suggest an improvement to this page.<br>
<a class=help-and-feedback-link href=# onclick="loadDisqus();return false;">Show and post comments</a>
to review and give feedback about this page.
<br>
</div>
<div class=mt-3>
<h5 class=help-and-feedback-heading>Product</h5>
<a class=help-and-feedback-link href="https://gitlab.com/gitlab-org/gitlab/-/issues/new?issue[description]=Describe%20what%20you%20would%20like%20to%20see%20improved.%0A%0A%3C!--%20Don%27t%20edit%20below%20this%20line%20--%3E%0A%0A%2Flabel%20~%22docs%5C-comments%22%20&issue[title]=Docs%20-%20product%20feedback:%20Write%20your%20title" target=_blank>Create an issue</a>
if there's something you don't like about this feature.<br>
<a class=help-and-feedback-link href="https://gitlab.com/gitlab-org/gitlab/-/issues/new?issuable_template=Feature%20proposal%20-%20detailed&issue[title]=Docs%20feedback%20-%20feature%20proposal:%20Write%20your%20title" target=_blank>Propose functionality</a>
by submitting a feature request.<br>
<a class=help-and-feedback-link href=https://about.gitlab.com/community/gitlab-first-look/ target=_blank>Join First Look</a>
to help shape new features.
</div>
<div class=mt-3>
<h5 class=help-and-feedback-heading>Feature availability and product trials</h5>
<a class=help-and-feedback-link href=https://about.gitlab.com/pricing/ target=_blank>View pricing</a>
to see all GitLab tiers and features, or to upgrade.<br>
<a class=help-and-feedback-link href=https://about.gitlab.com/free-trial/ target=_blank>Try GitLab for free</a>
with access to all features for 30 days.<br>
</div>
</div>
<div class="col-md-4 right-col">
<div class=help-subsection>
<h5 class=help-and-feedback-heading>Get Help</h5>
<p>
If you didn't find what you were looking for,
<a class=help-and-feedback-link href=/search/ target=_blank>search the docs</a>.<br>
<p class=mt-3>
If you want help with something specific and could use community support,
<a class=help-and-feedback-link href=https://forum.gitlab.com/ target=_blank>post on the GitLab forum</a>.<br>
<p class=mt-3>
For problems setting up or using this feature (depending on your GitLab
subscription).<br>
</p>
<a href=https://about.gitlab.com/support/ target=_blank class="btn support-btn mt-2 text-decoration-none" role=button>Request support</a>
</div>
</div>
</div>
</div>
</div>
<div id=disqus_thread class=disqus-comments-gitlab></div>
<script>var disqus_config=function(){this.page.url='https://docs.gitlab.com/ee/user/project/repository/gpg_signed_commits/index.html';this.page.title='Signing commits with GPG - GitLab Documentation';this.page.identifier='https://docs.gitlab.com/ee/user/project/repository/gpg_signed_commits/index.html';};var is_disqus_loaded=false;window.loadDisqus=function(){if(!is_disqus_loaded){is_disqus_loaded=true;var disqusThread=document.getElementById('disqus_thread');var d=document,s=d.createElement('script');disqusThread.innerHTML='';s.src='https://gitlab-docs.disqus.com/embed.js';s.setAttribute('data-timestamp',+new Date());(d.head||d.body).appendChild(s);}};</script>
<script src=/frontend/feedback/feedback.js></script>
<noscript>Please enable JavaScript to view the
<a href=https://disqus.com/?ref_noscript rel=nofollow>comments powered by Disqus.</a></noscript>
</div>
</div>
<div class=row>
<div class=col>
<footer class="px-3 border-top footer">
<div class="row py-2">
<div class=col-9>
<a href=https://gitlab.com/dashboard target=_blank> <img src=/assets/images/gitlab-logo.svg alt="Sign in to GitLab.com" aria-hidden=true role=img> </a>
</div>
<div class="col-3 p-0 m-0">
<div class="d-none d-md-flex justify-content-end">
<ul class="list-unstyled list-inline my-0 d-flex flex-wrap social-icons">
<li>
<a href=https://twitter.com/gitlab target=_blank class="pr-3 text-decoration-none gitlab-social"><i class="fa fa-twitter"></i> <span class=sr-only>Twitter</span></a>
<li>
<a href=https://www.facebook.com/gitlab target=_blank class="pr-3 text-decoration-none gitlab-social"><i class="fa fa-facebook-square"></i> <span class=sr-only>Facebook</span> </a>
<li>
<a href=https://www.youtube.com/channel/UCnMGQ8QHMAnVIsI3xJrihhg target=_blank class="pr-3 text-decoration-none gitlab-social"><i class="fa fa-youtube-play"></i> <span class=sr-only>YouTube</span> </a>
<li>
<a href=https://www.linkedin.com/company/gitlab-com target=_blank class="text-decoration-none gitlab-social"><i class="fa fa-linkedin-square"></i> <span class=sr-only>LinkedIn</span> </a>
</ul>
</div>
</div>
</div>
<div class="row py-2">
<div class="col-12 py-1">
<ul class="list-unstyled list-group list-group-horizontal flex-wrap">
<li class=pr-3>
<a href=https://gitlab.com/gitlab-org/gitlab-docs>Docs Repo</a>
<li class=pr-3>
<a href=https://about.gitlab.com/company/>About GitLab</a>
<li class=pr-3>
<a href=https://about.gitlab.com/terms/>Terms</a>
<li class=pr-3>
<a href=https://about.gitlab.com/privacy/>Privacy Policy</a>
<li class=pr-3>
<a href=https://about.gitlab.com/privacy/cookies/ class=text-decoration-none>Cookies Policy</a>
<li class=pr-3>
<a href=https://about.gitlab.com/company/contact/>Contact</a>
</ul>
</div>
</div>
<div class="row py-2">
<div class="col d-block">
<div class="d-block d-sm-inline-flex">
<p class=text-muted>
View <a href=https://gitlab.com/gitlab-org/gitlab/blob/master/doc/user/project/repository/gpg_signed_commits/index.md target=_blank rel="noopener noreferrer"><span class=text-decoration-underline>page source</span></a> -
Edit in <a href=https://gitlab.com/-/ide/project/gitlab-org/gitlab/edit/master/-/doc/user/project/repository/gpg_signed_commits/index.md target=_blank rel="noopener noreferrer"><span class=text-decoration-underline>Web IDE</span></a>
<a href=https://creativecommons.org/licenses/by-sa/4.0/ target=_blank rel="license noopener noreferrer"><img class="d-inline pl-3" src=/assets/images/by-sa.svg alt="Creative Commons License"></a>
</div>
</div>
</div>
<div class="row py-2 d-block d-md-none">
<div class=col>
<ul class="list-unstyled list-inline my-0 d-flex flex-wrap">
<li>
<a href=https://twitter.com/gitlab target=_blank class="pr-3 text-decoration-none gitlab-social"><i class="fa fa-twitter"></i> <span class=sr-only>Twitter</span></a>
<li>
<a href=https://www.facebook.com/gitlab target=_blank class="pr-3 text-decoration-none gitlab-social"><i class="fa fa-facebook-square"></i> <span class=sr-only>Facebook</span> </a>
<li>
<a href=https://www.youtube.com/channel/UCnMGQ8QHMAnVIsI3xJrihhg target=_blank class="pr-3 text-decoration-none gitlab-social"><i class="fa fa-youtube-play"></i> <span class=sr-only>YouTube</span> </a>
<li>
<a href=https://www.linkedin.com/company/gitlab-com target=_blank class="text-decoration-none gitlab-social"><i class="fa fa-linkedin-square"></i> <span class=sr-only>LinkedIn</span> </a>
</ul>
</div>
</div>
</footer>
</div>
</div>
</div>
<div class="col-3 py-3 d-none d-lg-flex">
<div id=doc-nav class="doc-nav w-100"></div>
</div>
</div>
</section>
<script src=https://cdn.jsdelivr.net/npm/jquery@3.5.1/dist/jquery.min.js integrity="sha256-9/aliU8dGd2tb6OSsuzixeV4y/faTqgFtohetphbbj0=" crossorigin=anonymous></script>
<script src=https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.bundle.min.js integrity=sha384-LtrjvnR4Twt/qOuYxE721u19sVFLVSA4hf/rRt6PrZTmiPltdZcI7q7PXQBYTKyf crossorigin=anonymous></script>
<script src=/assets/javascripts/toggle_popover-v1.js></script>
<script src=https://cdn.jsdelivr.net/npm/clipboard@2/dist/clipboard.min.js></script>
<script src=/assets/javascripts/clipboardjs-v2.js></script>
<script src=/assets/javascripts/badges-v6.js></script>
<script src=https://cdn.jsdelivr.net/npm/docsearch.js@2/dist/cdn/docsearch.min.js></script>
<script src=/assets/javascripts/docsearch-v1.js></script>
<script src=/assets/javascripts/mermaid-v2.js></script>
<script src=/assets/javascripts/facebook_analytics-v1.js></script>
<noscript><img height=1 width=1 style=display:none src="https://www.facebook.com/tr?id=1689559637958103&ev=PageView&noscript=1"></noscript>
<script src=/assets/javascripts/marketo_analytics-v1.js></script>
<script src=https://cdn.bizible.com/scripts/bizible.js async></script>
<script async src="https://www.googletagmanager.com/gtag/js?id=AW-923339191"></script>
<script src=/assets/javascripts/gtag_analytics-v1.js></script>
<script src=/assets/javascripts/linkedin_analytics-v1.js></script>
<noscript>
<img height=1 width=1 style=display:none alt src="https://dc.ads.linkedin.com/collect/?pid=30694&fmt=gif">
</noscript>
<script src=/frontend/header/index.js></script>
<script src=/assets/javascripts/docs-v4.js></script>
<script src=/assets/javascripts/global-nav-v.js></script>
<script src=/assets/javascripts/tables-v1.js></script>
<script src=/frontend/default/default.js data-cookieconsent=ignore></script>
</body>
</html>