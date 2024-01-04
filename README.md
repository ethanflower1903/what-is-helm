# what-is-helm
İçerik	
Helm Nedir?
Helm Kurulumu
Helm Cheat Sheet
Install and Uninstall Apps
Add, Remove, and Update Repos
Plugin Management
List and Search Repos
Chart Management
Perform App Upgrade and Rollback
Release Monitoring
Download Release Information
Get Help and Version Info
Helm Nedir?
Helm, Kubernetes üzerinde çalışan ilk uygulama paketi yöneticisidir. Uygulama yapısının uygun helm-charts aracılığıyla tanımlanmasına ve basit komutlarla yönetilmesine olanak tanır. Tüm Helm komutlarını (helm cheat sheet) yazının devamında inceleyebilirsiniz.

Helm neden önemlidir? Çünkü bu, sunucu tarafı uygulamaların tanımlanma, saklanma ve yönetilme biçiminde büyük bir değişimdir. Helm’in benimsenmesi, mikro hizmetlerin toplu olarak benimsenmesinin anahtarı olabilir, çünkü bu paket yöneticisini kullanmak yönetimlerini büyük ölçüde basitleştirir.

Helm Kurulumu
Tek satırda Helm kurulumunu içeren yazıma bu bağlantıdan ulaşabilirsiniz

helm cheat sheet
Helm Cheat Sheet
Install and Uninstall Apps
Name	Command
Install an app	helm install [name] [chart]
Install an app in a specific namespace	helm install [name] [chart] –namespace [namespace]
Override the default values with those specified in a file of your choice	helm install [name] [chart] –values [yaml-file/url]
Run a test install to validate and verify the chart	helm install [name] –dry-run –debug
Uninstall a release	helm uninstall [release] [name]
Add, Remove, and Update Repos
Name	Command
Add a repository from the internet	helm repo add [name] [url]
Remove a repository from your system	helm repo remove [name]
Update repositories	helm repo update
Plugin Management
Name	Command
Install plugins	helm plugin install [path/url1] [path/url2] …
View a list of all the installed plugins	helm plugin list
Update plugins	helm plugin update [plugin1] [plugin2] …
Uninstall a plugin	Helm plugin uninstall [plugin]
List and Search Repos
Name	Command
List chart repositories	helm repo list
Generate an index file containing charts found in the current directory	helm repo index
Search charts for a keyword	helm search [keyword]
Search repositories for a keyword	helm search repo [keyword]
Search Helm Hub	helm search hub [keyword]
Chart Management
Name	Command
Create a directory containing the common chart files and directories (Chart.yaml, values.yaml, charts/ and templates/)	helm create [name]
Package a chart into a chart archive	helm package [chart-path]
Run tests to examine a chart and identify possible issues	helm lint [chart]
Inspect a chart and list its contents	helm show all [chart]
Display the chart’s definition	helm show chart [chart]
Display the chart’s values	helm show values [chart]
Download a chart	helm pull [chart]
Download a chart and extract the archive’s contents into a directory	helm pull [chart] –untar –untardir [directory]
Display a list of a chart’s dependencies	helm dependency list [chart]
Perform App Upgrade and Rollback
Name	Command
Upgrade an app	helm upgrade [release] [chart]
Tell Helm to roll back changes if the upgrade fails	helm upgrade [release] [chart] –atomic
Upgrade a release. If it does not exist on the system, install it	helm upgrade [release] [chart] –install
Upgrade to a version other than the latest one	helm upgrade [release] [chart] –version [version-number]
Roll back a release	helm rollback [release] [revision]
Release Monitoring
Name	Command
List all the available releases in the current namespace	helm list
List all the available releases across all namespaces	helm list –all-namespaces
List all the releases in a specific namespace	helm list –namespace [namespace]
List all the releases in a specific output format	helm list –output [format]
Apply a filter to the list of releases using regular (Pearl compatible) expressions	helm list –filter ‘[expression]’
See the status of a release	helm status [release]
See the release history	helm history [release]
See information about the Helm client environment	helm env
Download Release Information
Name	Command
Download all the release information	helm get all [release]
Download all hooks	helm get hooks [release]
Download the manifest	helm get manifest [release]
Download the notes	helm get notes [release]
Download the values file	helm get values [release]
Fetch release history	helm history [release]
Get Help and Version Info
Name	Command
See the general help for Helm	helm –help
See help for a particular command	helm [command] –help
See the installed version of Helm	helm version....
