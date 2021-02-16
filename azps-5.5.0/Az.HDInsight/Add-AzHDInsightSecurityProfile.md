---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: c44fea946f98c6ac19e77e7012910afac37bff7c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117639"
---
# <span data-ttu-id="585dc-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="585dc-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="585dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="585dc-102">SYNOPSIS</span></span>
<span data-ttu-id="585dc-103">Adiciona um perfil de segurança a um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="585dc-103">Adds a security profile to a cluster configuration object.</span></span>

## <span data-ttu-id="585dc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="585dc-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -DomainResourceId <String>
 -DomainUserCredential <PSCredential> [-OrganizationalUnitDN <String>] -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="585dc-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="585dc-105">DESCRIPTION</span></span>
<span data-ttu-id="585dc-106">O perfil de segurança é usado para criar um cluster seguro, kerberizando-o.</span><span class="sxs-lookup"><span data-stu-id="585dc-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="585dc-107">O perfil de segurança contém configurações relacionadas à junção do cluster ao Domínio do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="585dc-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="585dc-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="585dc-108">EXAMPLES</span></span>

### <span data-ttu-id="585dc-109">Exemplo 1: Adicionar perfil de segurança ao objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="585dc-109">Example 1: Add security profile to the cluster configuration object</span></span>
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

<span data-ttu-id="585dc-110">Esse comando adiciona um valor de perfil de segurança ao cluster chamado seu-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="585dc-110">This command adds a security profile value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="585dc-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="585dc-111">PARAMETERS</span></span>

### <span data-ttu-id="585dc-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="585dc-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="585dc-113">Nomes distintos dos grupos do Active Directory que estarão disponíveis em Ambari e Emo.</span><span class="sxs-lookup"><span data-stu-id="585dc-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

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

### <span data-ttu-id="585dc-114">-Configuração</span><span class="sxs-lookup"><span data-stu-id="585dc-114">-Config</span></span>
<span data-ttu-id="585dc-115">Especifica o objeto de configuração de cluster HDInsight que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="585dc-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="585dc-116">Este objeto é criado pelo cmdlet New-AzHDInsightClusterConfig dados.</span><span class="sxs-lookup"><span data-stu-id="585dc-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="585dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="585dc-117">-DefaultProfile</span></span>
<span data-ttu-id="585dc-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="585dc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="585dc-119">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="585dc-119">-DomainResourceId</span></span>
<span data-ttu-id="585dc-120">ID de recurso de domínio do Active Directory para o cluster.</span><span class="sxs-lookup"><span data-stu-id="585dc-120">Active Directory domain resource id for the cluster.</span></span>

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

### <span data-ttu-id="585dc-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="585dc-121">-DomainUserCredential</span></span>
<span data-ttu-id="585dc-122">Uma credencial de conta de usuário de domínio com permissões suficientes para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="585dc-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="585dc-123">Nome de usuário deve estar no user@domain formato</span><span class="sxs-lookup"><span data-stu-id="585dc-123">Username should be in user@domain format</span></span>

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

### <span data-ttu-id="585dc-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="585dc-124">-LdapsUrls</span></span>
<span data-ttu-id="585dc-125">Urls de um ou vários servidores LDAPS para o Active Directory</span><span class="sxs-lookup"><span data-stu-id="585dc-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

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

### <span data-ttu-id="585dc-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="585dc-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="585dc-127">Nome diferenciado da unidade organizacional no Active directory onde as contas de usuário e computador serão criadas</span><span class="sxs-lookup"><span data-stu-id="585dc-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="585dc-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="585dc-128">-Confirm</span></span>
<span data-ttu-id="585dc-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="585dc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="585dc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="585dc-130">-WhatIf</span></span>
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

### <span data-ttu-id="585dc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="585dc-131">CommonParameters</span></span>
<span data-ttu-id="585dc-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="585dc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="585dc-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="585dc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="585dc-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="585dc-134">INPUTS</span></span>

### <span data-ttu-id="585dc-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="585dc-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
## <span data-ttu-id="585dc-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="585dc-136">OUTPUTS</span></span>

### <span data-ttu-id="585dc-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="585dc-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>
## <span data-ttu-id="585dc-138">Notas</span><span class="sxs-lookup"><span data-stu-id="585dc-138">NOTES</span></span>

## <span data-ttu-id="585dc-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="585dc-139">RELATED LINKS</span></span>
