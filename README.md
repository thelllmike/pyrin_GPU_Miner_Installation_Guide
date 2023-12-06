# Pyrinpyi and Pyrin GPU Miner Installation Guide

This guide provides step-by-step instructions for cloning the Pyrinpyi repository, installing Go, setting up the Pyrin GPU Miner, and starting the mining process.

## Cloning Pyrinpyi Repository

First, clone the Pyrinpyi repository:

git clone https://github.com/Pyrinpyi/pyipad.git

## Installing Go

Download and install Go:

wget https://golang.org/dl/go1.18.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.18.linux-amd64.tar.gz
echo 'export PATH=$PATH:/usr/local/go/bin' >> $HOME/.profile
source $HOME/.profile

Verify the Go installation:

go version

## Setting Up Pyrinpyi

Navigate to the Pyrinpyi directory and run the main program:

cd pyipad
go run main.go --utxoindex

## Downloading and Setting Up Pyrin GPU Miner

Download Pyrin GPU Miner:

wget https://github.com/Pyrinpyi/pyrin-gpu-miner/releases/download/1.0.0/pyrin-miner-linux-amd64.tgz
mkdir pyrin-gpu-miner
tar -xvzf pyrin-miner-linux-amd64.tgz -C pyrin-gpu-miner/

Extract and set up the miner:

cd pyrin-gpu-miner
tar -xvf pyrin-miner-linux-amd64.tar
cd pyrin-miner-linux-amd64
chmod +x pyrin-miner

## Starting the Miner

Run the Pyrin Miner with your mining address:

./pyrin-miner --mining-address pyrin:qzag84dece07xtmhnl3u94lk74s3m6d33qy8lw9eq6vxcurrcn4vup9j9e72c

Or use a pool:

e4-pyrin-miner -s stratum+tcp://pyrin.e4pool.com:12100 -a pyrin:qzag84dece07xtmhnl3u94lk74s3m6d33qy8lw9eq6vxcurrcn4vup9j9e72c.%WORKER%

