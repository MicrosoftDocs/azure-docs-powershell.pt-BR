---
title: Guia de migração para o Az 2.0.0
description: Este guia de migração contém uma lista das alterações da falha feitas no Azure PowerShell no lançamento da versão 2.0 do Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.openlocfilehash: 133769c09f74e1d0d90eff0c6c4bdbb90d1ebe24
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "81445485"
---
# <a name="migration-guide-for-az-200"></a>Guia de migração para o Az 2.0.0

Este documento descreve as alterações entre as versões 1.0.0 e 2.0.0 do Az 

## <a name="table-of-contents"></a>Sumário
- [Alterações de falhas para módulos](#module-breaking-changes)
  - [Az.Compute](#azcompute)
  - [Az.HDInsight](#azhdinsight)
  - [Az.Storage](#azstorage)

## <a name="module-breaking-changes"></a>Alterações de falhas para módulos

### <a name="azcompute"></a>Az.Compute

- Remoção do parâmetro `Managed` dos cmdlets `New-AzAvailabilitySet` e `Update-AzAvailabilitySet` a favor do uso de ```Sku = Aligned```

  #### <a name="before"></a>Antes de

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a>After (após)

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- Para fins de consistência, remoção do parâmetro `Image` dos conjuntos de parâmetros 'ByName' e 'ByResourceId' em `Update-AzImage` 
  
  #### <a name="before"></a>Antes de

  Observe que o código abaixo é funcional, mas o ImageName passado não é usado; portanto, a remoção desse parâmetro não tem nenhum impacto funcional.

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a>After (após)

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- Para fins de consistência, remoção do parâmetro `Name` dos conjuntos de parâmetros 'ByObject' e 'ByResourceId' em `Restart-AzVM`
  
  #### <a name="before"></a>Antes de

  Observe que o código abaixo é funcional, mas o Name passado não é usado; portanto, a remoção desse parâmetro não tem nenhum impacto funcional.
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>After (após)

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- Para fins de consistência, remoção do parâmetro `Name` dos conjuntos de parâmetros 'ByObject' e 'ByResourceId' em `Start-AzVM`
  
  #### <a name="before"></a>Antes de

  Observe que o código abaixo é funcional, mas o Name passado não é usado; portanto, a remoção desse parâmetro não tem nenhum impacto funcional.

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>After (após)

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- Para fins de consistência, remoção do parâmetro `Name` dos conjuntos de parâmetros 'ByObject' e 'ByResourceId' em `Stop-AzVM`
  
  #### <a name="before"></a>Antes de

  Observe que o código abaixo é funcional, mas o Name passado não é usado; portanto, a remoção desse parâmetro não tem nenhum impacto funcional.

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>After (após)

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- Para fins de consistência, remoção do parâmetro `Name` dos conjuntos de parâmetros 'ByObject' e 'ByResourceId' em `Remove-AzVM`
  
  #### <a name="before"></a>Antes de

  Observe que o código abaixo é funcional, mas o Name passado não é usado; portanto, a remoção desse parâmetro não tem nenhum impacto funcional.

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a>After (após)

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- Para fins de consistência, remoção do parâmetro `Name` dos conjuntos de parâmetros 'ByObject' e 'ByResourceId' em `Set-AzVM`
  
  #### <a name="before"></a>Antes de

  Observe que o código abaixo é funcional, mas o Name passado não é usado; portanto, a remoção desse parâmetro não tem nenhum impacto funcional.

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a>After (após)

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- Para fins de consistência, remoção do parâmetro `Name` dos conjuntos de parâmetros 'ByObject' e 'ByResourceId' em `Save-AzVMImage` 
  
  #### <a name="before"></a>Antes de
  Observe que o código abaixo é funcional, mas o Name passado não é usado; portanto, a remoção desse parâmetro não tem nenhum impacto funcional.
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a>After (após)
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- Adição da propriedade ProtectionPolicy para encapsular a propriedade `ProtectFromScaleIn` em `PSVirtualMachineScaleSetVM`

  #### <a name="before"></a>Antes de

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a>After (após)

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- Adição da propriedade ```EncryptionSettingsCollection``` para delimitar a propriedade `EncryptionSettings` em `PSDisk`

  #### <a name="before"></a>Antes de

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a>After (após)

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- Adição da propriedade ```EncryptionSettingsCollection``` para delimitar a propriedade `EncryptionSettings` em `PSSnapshot`

  #### <a name="before"></a>Antes de

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a>After (após)

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- Remoção da propriedade `VirtualMachineProfile` de `PSVirtualMachineScaleSet`

  #### <a name="before"></a>Antes de

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a>After (após)

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- O cmdlet `Set-AzVMBootDiagnostic` removeu o alias para `Set-AzVMBootDiagnostics`

  #### <a name="before"></a>Antes de

  Uso do alias preterido

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a>After (após)

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- O cmdlet `Export-AzLogAnalyticThrottledRequest` removeu o alias para `Export-AzLogAnalyticThrottledRequests`

  #### <a name="before"></a>Antes de

  Uso do alias preterido

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a>After (após)

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a>Az.HDInsight

- Remoção dos cmdlets `Grant-AzHDInsightHttpServicesAccess` e `Revoke-AzHDInsightHttpServicesAccess`. Eles não são mais necessários porque o acesso HTTP está sempre habilitado em todos os clusters do HDInsight.
- Adição de um novo cmdlet `Set-AzHDInsightGatewayCredential`. Use esse cmdlet para alterar o nome de usuário e a senha HTTP do gateway (substitui `Grant-AzHDInsightHttpServicesAccess`).
- Atualização do cmdlet `Get-AzHDInsightJobOutput` para dar suporte ao acesso granular baseado em função à chave de armazenamento.
    - Os usuários com as funções Operador do Cluster HDInsight, Colaborador ou Proprietário não serão afetados.
    - Os usuários com apenas a função Leitor precisarão especificar o parâmetro `DefaultStorageAccountKey` explicitamente.

Para obter mais informações sobre essas alterações de acesso baseado em função, confira [aka.ms/hdi-config-update](https://aka.ms/hdi-config-update)

  #### <a name="before"></a>Antes de

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a>After (após)

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a>Os usuários com apenas a função Leitor para o cmdlet Get-AzHDInsightJobOutput

  ####  <a name="before"></a>Antes de

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a>After (após)

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a>Az.Storage

- Os namespaces para os tipos retornados de cmdlets de Blob, Fila e Arquivo foram alterados de `Microsoft.WindowsAzure.Storage` para `Microsoft.Azure.Storage`.  Embora essa não seja tecnicamente uma alteração da falha de acordo com a política de alteração da falha, ela pode exigir algumas alterações no código que usa os métodos do SDK do .NET de Armazenamento para interagir com os objetos retornados desses cmdlets.

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a>Exemplo 1:  Adicionar uma mensagem a uma fila (alterar o namespace do objeto CloudQueueMessage)

  Antes: 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  Após:

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a>Exemplo 2:  Efetuar fetch de atributos de blob/arquivo com AccessCondition (alterar o namespace do objeto AccessCondition)

  Antes: 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  Após:

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- Embora essa não seja tecnicamente uma alteração da falha, você observará diferenças de saída na propriedade Sku.Name das contas de armazenamento retornadas das alterações em `New/Get/Set-AzStorageAccount` são descritas a seguir. (Após a alteração, o SkuName de saída e de entrada são alinhados.)
  - "StandardLRS" -> "Standard_LRS";
  - "StandardGRS" -> "Standard_GRS";
  - "StandardRAGRS" -> "Standard_RAGRS";
  - "StandardZRS" -> "Standard_ZRS";
  - "PremiumLRS" -> "Premium_LRS";

- O comportamento do serviço padrão ao criar uma conta de armazenamento sem especificar um tipo foi alterado.  Nas versões anteriores, quando uma conta de armazenamento era criada sem nenhum `Kind` especificado, o tipo de conta de armazenamento de `Storage` era usado na nova versão `StorageV2` é o valor `Kind` padrão. Caso você precise criar uma conta de armazenamento V1 com o tipo 'Storage', adicione o parâmetro '-Kind Storage'

  #### <a name="example--create-a-storage-account-default-kind-change"></a>Exemplo: Criar uma conta de armazenamento (alteração de Tipo Padrão)  

  Antes:

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  Após:

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```
