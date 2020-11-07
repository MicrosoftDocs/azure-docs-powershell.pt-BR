---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
ms.openlocfilehash: 035b21684c3d8fc64cee7ee78b7b4cb2adf21f01
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770829"
---
# <span data-ttu-id="6d932-101">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="6d932-101">Add-AzHDInsightClusterIdentity</span></span>

## <span data-ttu-id="6d932-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d932-102">SYNOPSIS</span></span>
<span data-ttu-id="6d932-103">Adiciona uma identidade de cluster a um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="6d932-103">Adds a cluster identity to a cluster configuration object.</span></span>

## <span data-ttu-id="6d932-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d932-104">SYNTAX</span></span>

### <span data-ttu-id="6d932-105">CertificateFilePath (padrão)</span><span class="sxs-lookup"><span data-stu-id="6d932-105">CertificateFilePath (Default)</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d932-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="6d932-106">CertificateFileContents</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d932-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d932-107">DESCRIPTION</span></span>
<span data-ttu-id="6d932-108">O cmdlet **Add-AzHDInsightClusterIdentity** adiciona uma identidade de cluster ao objeto de configuração do Azure HDInsight criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="6d932-108">The **Add-AzHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="6d932-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d932-109">EXAMPLES</span></span>

### <span data-ttu-id="6d932-110">Exemplo 1: adicionar informações de identidade do cluster ao objeto de configuração do cluster</span><span class="sxs-lookup"><span data-stu-id="6d932-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="6d932-111">Esse comando adiciona informações de identidade de cluster ao cluster chamado seu-Hadoop-001, permitindo que o cluster acesse o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6d932-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="6d932-112">OS</span><span class="sxs-lookup"><span data-stu-id="6d932-112">PARAMETERS</span></span>

### <span data-ttu-id="6d932-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="6d932-113">-AadTenantId</span></span>
<span data-ttu-id="6d932-114">Especifica a ID de locatário do Azure AD que será usada ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6d932-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="6d932-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="6d932-115">-CertificateFileContents</span></span>
<span data-ttu-id="6d932-116">Especifica o conteúdo do arquivo do certificado que será usado ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6d932-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="6d932-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="6d932-117">-CertificateFilePath</span></span>
<span data-ttu-id="6d932-118">Especifica o caminho do arquivo para o certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="6d932-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="6d932-119">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6d932-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="6d932-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="6d932-120">-CertificatePassword</span></span>
<span data-ttu-id="6d932-121">Especifica a senha do certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="6d932-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="6d932-122">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6d932-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="6d932-123">-Config</span><span class="sxs-lookup"><span data-stu-id="6d932-123">-Config</span></span>
<span data-ttu-id="6d932-124">Especifica o objeto de configuração de cluster HDInsight que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="6d932-124">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="6d932-125">Esse objeto é criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="6d932-125">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="6d932-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d932-126">-DefaultProfile</span></span>
<span data-ttu-id="6d932-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6d932-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d932-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6d932-128">-ObjectId</span></span>
<span data-ttu-id="6d932-129">Especifica a ID do objeto do AD do Azure (um GUID) da entidade de serviço do Azure AD que representa o cluster.</span><span class="sxs-lookup"><span data-stu-id="6d932-129">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="6d932-130">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6d932-130">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="6d932-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d932-131">CommonParameters</span></span>
<span data-ttu-id="6d932-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d932-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d932-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d932-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d932-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d932-134">INPUTS</span></span>

### <span data-ttu-id="6d932-135">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="6d932-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

### <span data-ttu-id="6d932-136">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6d932-136">System.Guid</span></span>

## <span data-ttu-id="6d932-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d932-137">OUTPUTS</span></span>

### <span data-ttu-id="6d932-138">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="6d932-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="6d932-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d932-139">NOTES</span></span>

## <span data-ttu-id="6d932-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d932-140">RELATED LINKS</span></span>

[<span data-ttu-id="6d932-141">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="6d932-141">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


