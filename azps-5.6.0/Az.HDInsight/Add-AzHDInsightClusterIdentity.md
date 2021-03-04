---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
ms.openlocfilehash: b154ab0bbcf10c0fb1d68b7634e5e2d1bf97a45d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890264"
---
# <span data-ttu-id="ec8af-101">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="ec8af-101">Add-AzHDInsightClusterIdentity</span></span>

## <span data-ttu-id="ec8af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec8af-102">SYNOPSIS</span></span>
<span data-ttu-id="ec8af-103">Adiciona uma identidade de cluster a um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="ec8af-103">Adds a cluster identity to a cluster configuration object.</span></span>

## <span data-ttu-id="ec8af-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ec8af-104">SYNTAX</span></span>

### <span data-ttu-id="ec8af-105">CertificateFilePath (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ec8af-105">CertificateFilePath (Default)</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [[-ApplicationId] <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec8af-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="ec8af-106">CertificateFileContents</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [[-ApplicationId] <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec8af-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ec8af-107">DESCRIPTION</span></span>
<span data-ttu-id="ec8af-108">O cmdlet **Add-AzHDInsightClusterIdentity** adiciona uma identidade de cluster ao objeto de configuração HDInsight do Azure criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="ec8af-108">The **Add-AzHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="ec8af-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec8af-109">EXAMPLES</span></span>

### <span data-ttu-id="ec8af-110">Exemplo 1: Adicionar informações de Identidade de Cluster ao objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="ec8af-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
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

# Cluster Identity values
PS C:\> $tenantId = (Get-AzContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $applicationId = "<Azure AD Service Principal Application ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -Application $applicationId
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageAccountContainer
```

<span data-ttu-id="ec8af-111">Este comando adiciona informações de Identidade de Cluster ao cluster chamado your-hadoop-001, permitindo que o cluster acesse o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec8af-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="ec8af-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ec8af-112">PARAMETERS</span></span>

### <span data-ttu-id="ec8af-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="ec8af-113">-AadTenantId</span></span>
<span data-ttu-id="ec8af-114">Especifica a ID de locatário do Azure AD que será usada ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec8af-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8af-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ec8af-115">-ApplicationId</span></span>
<span data-ttu-id="ec8af-116">A ID do Aplicativo Principal de Serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="ec8af-116">The Service Principal Application Id for accessing Azure Data Lake.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8af-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="ec8af-117">-CertificateFileContents</span></span>
<span data-ttu-id="ec8af-118">Especifica o conteúdo do arquivo do certificado que será usado ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec8af-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8af-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="ec8af-119">-CertificateFilePath</span></span>
<span data-ttu-id="ec8af-120">Especifica o caminho do arquivo para o certificado que será usado para autenticar como a Entidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="ec8af-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="ec8af-121">O cluster usará isso ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec8af-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8af-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="ec8af-122">-CertificatePassword</span></span>
<span data-ttu-id="ec8af-123">Especifica a senha do certificado que será usado para autenticar como Entidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="ec8af-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="ec8af-124">O cluster usará isso ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec8af-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8af-125">-Config</span><span class="sxs-lookup"><span data-stu-id="ec8af-125">-Config</span></span>
<span data-ttu-id="ec8af-126">Especifica o objeto de configuração de cluster HDInsight que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="ec8af-126">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="ec8af-127">Esse objeto é criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="ec8af-127">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="ec8af-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec8af-128">-DefaultProfile</span></span>
<span data-ttu-id="ec8af-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ec8af-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec8af-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ec8af-130">-ObjectId</span></span>
<span data-ttu-id="ec8af-131">Especifica a ID do objeto do Azure AD (um GUID) da Entidade de Serviço do Azure AD que representa o cluster.</span><span class="sxs-lookup"><span data-stu-id="ec8af-131">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="ec8af-132">O cluster usará isso ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec8af-132">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec8af-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec8af-133">CommonParameters</span></span>
<span data-ttu-id="ec8af-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec8af-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec8af-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec8af-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec8af-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec8af-136">INPUTS</span></span>

### <span data-ttu-id="ec8af-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ec8af-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

### <span data-ttu-id="ec8af-138">System.Guid</span><span class="sxs-lookup"><span data-stu-id="ec8af-138">System.Guid</span></span>

## <span data-ttu-id="ec8af-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ec8af-139">OUTPUTS</span></span>

### <span data-ttu-id="ec8af-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ec8af-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="ec8af-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="ec8af-141">NOTES</span></span>

## <span data-ttu-id="ec8af-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec8af-142">RELATED LINKS</span></span>

[<span data-ttu-id="ec8af-143">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="ec8af-143">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


