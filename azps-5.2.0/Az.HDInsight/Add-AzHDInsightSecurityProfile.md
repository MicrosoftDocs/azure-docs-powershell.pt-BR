---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: c44fea946f98c6ac19e77e7012910afac37bff7c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259378"
---
# Add-AzHDInsightSecurityProfile

## Sinopse
Adiciona um perfil de segurança a um objeto de configuração de cluster.

## SYNTAX

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -DomainResourceId <String>
 -DomainUserCredential <PSCredential> [-OrganizationalUnitDN <String>] -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O perfil de segurança é usado para criar um cluster seguro, kerberizing-lo.
O perfil de segurança contém a configuração relacionada à junção do cluster ao domínio do Active Directory.

## EXEMPLOS

### Exemplo 1: Adicionar perfil de segurança ao objeto de configuração de cluster
```
PS C:\> #Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

#Security profile info
PS C:\> $domain="sampledomain.onmicrosoft.com"
PS C:\> $domainUser="sample.user@sampledomain.onmicrosoft.com"
PS C:\> $domainPassword=ConvertTo-SecureString "domainPassword" -AsPlainText -Force
PS C:\> $domainUserCredential=New-Object System.Management.Automation.PSCredential($domainUser, $domainPassword)
PS C:\> $organizationalUnitDN="ou=testunitdn"
PS C:\> $ldapsUrls=("ldaps://sampledomain.onmicrosoft.com:636","ldaps://sampledomain.onmicrosoft.com:389")
PS C:\> $clusterUsersGroupDNs=("groupdn1","groupdn2")

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightSecurityProfile `
                -Domain $domain `
                -DomainUserCredential $domainUserCredential `
                -OrganizationalUnitDN $organizationalUnitDN `
                -LdapsUrls $ldapsUrls `
                -ClusterUsersGroupDNs $clusterUsersGroupDNs `
            | New-AzHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

Esse comando adiciona um valor de perfil de segurança ao cluster chamado seu-Hadoop-001.

## OS

### -ClusterUsersGroupDNs
Nomes distintos dos grupos do Active Directory que estarão disponíveis no Ambari e no Ranger

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
Especifica o objeto de configuração de cluster HDInsight que esse cmdlet modifica.
Esse objeto é criado pelo cmdlet New-AzHDInsightClusterConfig.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainResourceId
ID do recurso de domínio do Active Directory para o cluster.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainUserCredential
Uma credencial de conta de usuário do domínio com permissões suficientes para criar o cluster.
O nome de usuário deve estar em user@domain formato

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LdapsUrls
URLs de um ou vários servidores LDAPs para o Active Directory

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OrganizationalUnitDN
Nome diferenciado da unidade organizacional no Active Directory onde as contas de usuário e de computador serão criadas

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig
## EXIBE

### Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSecurityProfile
## INFORMA

## LINKS RELACIONADOS
