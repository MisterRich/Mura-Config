# Documented

## settings.ini.cfm Reference
http://docs.getmura.com/v6/installation-setup/settingsinicfm-reference/

	admindomain=
	adminemail=
	adminssl=0
	assetdir=
	assetpath=
	autoresetpasswords=true
	clientmanagement=false // Note: Presume this is a CF setting.
	clientstorage= // Note: Presume this is a CF setting.
	confirmsaveasdraft=true
	context=
	customtagpaths= // Note: Presume this is a CF setting.
	dashboard=true
	datasource=
	dbtype=
	debuggingenabled=true
	enablemuratag=true
	filedir=
	filestore=filedir
	indexfileinurls=1
	imageinterpolation=highestQuality
	locale=Server
	logevents=0
	loginStrikes=4 // Note: references as loginstrike in reference
	mailserverip=
	mailserverpassword=
	mailserverpopport=110
	mailserversmtpport=25
	mailserverssl=false
	mailservertls=false
	mailserverusername=
	notifywithversionlink=true
	ping=0
	plugindir=
	port=${cgi.SERVER_PORT}
	proxypassword=
	proxyport=${cgi.SERVER_PORT}
	proxyserver=
	proxyuser=
	purgeDrafts=true
	sessionhistory=1
	sessiontimeout=180 // Note: Does this conflict with CF value? Presume this is in seconds.
	siteidinurls=false
	sortpermission=editor
	strictextendeddata=1
	stub=
	tempdir=
	title=Mura CMS
	usedefaultsmtpserver=1
	usefilemode=false
	webrootmap=muraWRM

## Deprecated
	mapdir=mura
	stub=

## In reference but not in config/templates/settings.template.cfm 
	clusterlist
	dbUsername
	dbPassword
	encryptionkey
	fileStoreAccessInfo
	htmleditortype
	productiondatasource
	productionassetpath
	productionWebroot
	productionFiledir

# Undocumented

## Cannot be changed
	allowlocalfiles=false
	bcryptlogrounds=10
	bcryptpasswords=true
	bcryptreseedfrequency=60
	dashboardcomments=true
	dbcasesensitive=false
	forceadminssl=true
	hashurls=false
	javasettingsreloadonchage=false
	scriptprotect=true // Note: Is hard coded as false in config/applicationSettings.cfm
	scriptprotectexceptions=Body
	sendfrommailserverusername=true
	sourceimagescale=3000
	sourceimagescaleby=x
	strictfactory=true // Note: Is hard coded as false in requirements/mura/configBean.cfc 
	tracksessioninnewthread=1
	windowdocumentdomain=

## Can be changed 

### Has Setter
	allowautoupdates=1
	dbtablespace=USERS
	maxarchivedversions=50
	maxsourceimagewidth=4000
	sharableremotesessions=1

### application.configBean.getValue
	autodiscoverplugins=false
	autopreviewimages=true
	defaultfilemode=777 // Also as variables.configBean.getValue in requirements/mura/content/file/processImgCfimage.cfc
	editablecomments=0
	fmshowapplicationroot=1
	fmshowsitefiles=1
	rendermuraalerts=true
	showadminloginhelp=true
	uselegacysessions=0 // Also as variables.configBean.getValue in requirements/mura/user/userUtility.cfc and set to true in requirements/mura/configBean.cfc 

### variables.configBean.getValue
	autoupdatemode=default
	secureCookies=false // Also as application.configBean.getValue in various files
	strongpasswordregex=(?=^.{7,15}$)(?=.*\d)(?![.\n])(?=.*[a-zA-Z]).*$
	strongpasswords=0

### $.siteConfig
	haslockablenodes=false
	recaptchasitekey=
	recaptchasecret=
	recaptchalanguage=en

### $.globalConfig
	accesscontrolheaders=false
	accesscontrolcredentials=false
	maxportalitems=1000

### getINIProperty
	donottrackagents=
	javaenabled=true // Also as $.globalConfig in admin/common/layouts/includes/header.cfm 
	javasettingsloadcoldfusionclasspath=true
	;javasettingsloadpaths=/requirements/lib
	javasettingswatchextensions=jar,class
	javasettingswatchinterval=60
	ormautomanagesession=false
	ormcfclocation=
	ormdbcreate=update
	ormdatasource=
	ormenabled=true
	ormeventhandling=true
	ormflushatrequestend=false
	ormlogsql=false
	ormsavemapping=false
	ormskipcfcwitherror=false
	ormusedbformapping=true
	requesttimeout=1000 // Also hard coded in various files
	s3accesskeyid=
	s3awssecretkey=
	sameformfieldsasarray=false