---
sidebar_label: 'Apply a Config Change'
title: 'Apply a Software Platform Configuration Change'
id: apply-platform-config
description: Apply platform-wide configuration changes to Astronomer via Helm.
---

## Overview

When you install Astronomer, a number of platform-level settings will be set by default. If you'd like to change any of those settings based on the needs of your organization, you can do so at any time using Helm.

For example, you can:

* [Integrate an Auth system](integrate-auth-system.md)
* [Add a registry backend](registry-backend.md)
* [Change resource allocation limits](configure-platform-resources.md)
* Update any other key-value pair specified in the [default configuration file](https://github.com/astronomer/astronomer/blob/master/values.yaml)

To configure these settings, follow the steps below.

> **Note:** If you're interested in upgrading Astronomer to a new patch version of the platform, read [Upgrade to a Patch Version](upgrade-astronomer-stable.md).

## Step 1: Open Your config.yaml File

This file was created when you installed Astronomer using one of the following guides:

* [AWS EKS Installation Guide](install-aws-standard.md#step-8-configure-your-helm-chart)
* [GCP GKE Installation Guide](install-gcp-standard.md#step-7-configure-your-helm-chart)
* [Azure AKS Installation Guide](install-azure-standard.md#step-7-configure-your-helm-chart)

## Step 2: Update Key-Value Pairs

To update any of your existing settings, modify them directly in your `config.yaml` file. To update a setting you haven't already specified, copy the corresponding key-value pair from the [default configuration file](https://github.com/astronomer/docs/blob/main/software_configs/0.26/default.yaml) into your `config.yaml` file and modify the value from there.

When you have finished updating the key-value pairs, ensure that they have the same relative order and indentation as they do in the default configuration file. If they don't, your changes might not be properly applied.

## Step 3: Push Changes to Astronomer

1. Identify your platform namespace and release name. Your platform release name can be found in your list of active namespaces. To show this list, run:
```sh
kubectl get ns
```
To identify the value for your platform release name, run:
```sh
helm ls -n <your-platform-namespace>
```
2. Save your config.yaml file and run a helm upgrade by running:
```sh
helm upgrade <your-platform-release-name> astronomer/astronomer -f config.yaml -n <your-platform-namespace> --version=<your-platform-version>
```
3. Confirm that the key-value pairs were successfully updated by running:
```sh
helm get values <your-platform-release-name> -n <your-platform-namespace>
```
