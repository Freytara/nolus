           
#Nolus snapshot


```
systemctl stop nolusd
```

```
cp $HOME/.nolusd/data/priv_validator_state.json $HOME/.nolusd/priv_validator_state.json.backup
```

```
rm -rf ~/.nolusd/data; \
mkdir -p ~/.nolusd/data; \
cd ~/.nolusd/data
```

```
wget -O $HOME/.nolus http://195.201.237.185/nolus/nolus-rila_latest.tar | tar xf -
```

```
mv $HOME/.nolusd/priv_validator_state.json.backup $HOME/.nolusd/data/priv_validator_state.json
```


```
systemctl start nolusd \
journalctl -u nolusd -f --no-hostname
```


