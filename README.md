##vi .bashrc

alias k=kubectl
alias kn=‘kubectl config set-context --current --namespace’
alias gn=‘cat .kube/config | grep namespace’
alias kg=‘k get’
alias kgd=‘k get deploy -o wide’
alias kgp=‘k get pods -o wide’
alias kgpw=‘k get pods -o wide --watch’
alias kgpa=‘k get pods -o wide -A’
alias kgn=‘k get nodes -o wide’
alias kgs=‘k get svc -o wide’
alias kge=‘k get events --sort-by=’.metadata.creationTimestamp’ | tail -8’
alias ked=‘k edit deploy’
alias kep=‘k edit pods’
alias ken=‘k edit nodes’
alias kes=‘k edit svc’
alias kc=‘k create’
alias kd=‘k describe’
alias kdelp=‘k $now delete po’
alias kdel=‘k delete’
alias ke=‘k edit’
alias kdd=‘k describe deploy’
alias kdp=‘k describe pods’
alias kdn=‘k describe nodes’
alias kds=‘k describe svc’
alias krf=‘k replace --force -f’
alias krpf=‘k replace $now -f’
alias kcf=‘k create -f’
krp() { kubectl run $1 --image=$2 $do;}
kcd() { kubectl create deploy $1 --image=$2 $do;}
export nks=‘-n kube-system’
export do=’ --dry-run=client -o yaml’
export now=’ --force --grace-period=0’
export rb=‘rolebinding’
export crb=‘clusterrolebinding’
