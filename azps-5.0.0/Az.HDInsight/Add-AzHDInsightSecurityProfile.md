---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: c44fea946f98c6ac19e77e7012910afac37bff7c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115384"
---
# <span data-ttu-id="3cffb-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="3cffb-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="3cffb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3cffb-102">SYNOPSIS</span></span>
<span data-ttu-id="3cffb-103">Adiciona um perfil de segurança a um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="3cffb-103">Adds a security profile to a cluster configuration object.</span></span>

## <span data-ttu-id="3cffb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3cffb-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -DomainResourceId <String>
 -DomainUserCredential <PSCredential> [-OrganizationalUnitDN <String>] -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cffb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3cffb-105">DESCRIPTION</span></span>
<span data-ttu-id="3cffb-106">O perfil de segurança é usado para criar um cluster seguro, kerberizing-lo.</span><span class="sxs-lookup"><span data-stu-id="3cffb-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="3cffb-107">O perfil de segurança contém a configuração relacionada à junção do cluster ao domínio do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3cffb-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="3cffb-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3cffb-108">EXAMPLES</span></span>

### <span data-ttu-id="3cffb-109">Exemplo 1: Adicionar perfil de segurança ao objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="3cffb-109">Example 1: Add security profile to the cluster configuration object</span></span>
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

<span data-ttu-id="3cffb-110">Esse comando adiciona um valor de perfil de segurança ao cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="3cffb-110">This command adds a security profile value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="3cffb-111">OS</span><span class="sxs-lookup"><span data-stu-id="3cffb-111">PARAMETERS</span></span>

### <span data-ttu-id="3cffb-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="3cffb-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="3cffb-113">Nomes distintos dos grupos do Active Directory que estarão disponíveis no Ambari e no Ranger</span><span class="sxs-lookup"><span data-stu-id="3cffb-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

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

### <span data-ttu-id="3cffb-114">-Config</span><span class="sxs-lookup"><span data-stu-id="3cffb-114">-Config</span></span>
<span data-ttu-id="3cffb-115">Especifica o objeto de configuração de cluster HDInsight que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="3cffb-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="3cffb-116">Esse objeto é criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="3cffb-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="3cffb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cffb-117">-DefaultProfile</span></span>
<span data-ttu-id="3cffb-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3cffb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cffb-119">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="3cffb-119">-DomainResourceId</span></span>
<span data-ttu-id="3cffb-120">ID do recurso de domínio do Active Directory para o cluster.</span><span class="sxs-lookup"><span data-stu-id="3cffb-120">Active Directory domain resource id for the cluster.</span></span>

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

### <span data-ttu-id="3cffb-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="3cffb-121">-DomainUserCredential</span></span>
<span data-ttu-id="3cffb-122">Uma credencial de conta de usuário do domínio com permissões suficientes para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="3cffb-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="3cffb-123">O nome de usuário deve estar em user@domain formato</span><span class="sxs-lookup"><span data-stu-id="3cffb-123">Username should be in user@domain format</span></span>

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

### <span data-ttu-id="3cffb-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="3cffb-124">-LdapsUrls</span></span>
<span data-ttu-id="3cffb-125">URLs de um ou vários servidores LDAPs para o Active Directory</span><span class="sxs-lookup"><span data-stu-id="3cffb-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

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

### <span data-ttu-id="3cffb-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="3cffb-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="3cffb-127">Nome diferenciado da unidade organizacional no Active Directory onde as contas de usuário e de computador serão criadas</span><span class="sxs-lookup"><span data-stu-id="3cffb-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="3cffb-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3cffb-128">-Confirm</span></span>
<span data-ttu-id="3cffb-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cffb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cffb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cffb-130">-WhatIf</span></span>
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

### <span data-ttu-id="3cffb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cffb-131">CommonParameters</span></span>
<span data-ttu-id="3cffb-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cffb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cffb-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cffb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cffb-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3cffb-134">INPUTS</span></span>

### <span data-ttu-id="3cffb-135">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3cffb-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
## <span data-ttu-id="3cffb-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3cffb-136">OUTPUTS</span></span>

### <span data-ttu-id="3cffb-137">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="3cffb-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>
## <span data-ttu-id="3cffb-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3cffb-138">NOTES</span></span>

## <span data-ttu-id="3cffb-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3cffb-139">RELATED LINKS</span></span>
