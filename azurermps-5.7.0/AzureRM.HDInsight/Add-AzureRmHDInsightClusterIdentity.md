---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
ms.openlocfilehash: e4e481a7ee26be966abda3d996575ab1bbd03b42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429786"
---
# <span data-ttu-id="121de-101">Add-AzureRmHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="121de-101">Add-AzureRmHDInsightClusterIdentity</span></span>

## <span data-ttu-id="121de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="121de-102">SYNOPSIS</span></span>
<span data-ttu-id="121de-103">Adiciona uma identidade de cluster a um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="121de-103">Adds a cluster identity to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="121de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="121de-104">SYNTAX</span></span>

### <span data-ttu-id="121de-105">CertificateFilePath (padrão)</span><span class="sxs-lookup"><span data-stu-id="121de-105">CertificateFilePath (Default)</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="121de-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="121de-106">CertificateFileContents</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="121de-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="121de-107">DESCRIPTION</span></span>
<span data-ttu-id="121de-108">O cmdlet **Add-AzureRmHDInsightClusterIdentity** adiciona uma identidade de cluster ao objeto de configuração do Azure HDInsight criado pelo cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="121de-108">The **Add-AzureRmHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="121de-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="121de-109">EXAMPLES</span></span>

### <span data-ttu-id="121de-110">Exemplo 1: adicionar informações de identidade do cluster ao objeto de configuração do cluster</span><span class="sxs-lookup"><span data-stu-id="121de-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzureRmContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="121de-111">Esse comando adiciona informações de identidade de cluster ao cluster chamado seu-Hadoop-001, permitindo que o cluster acesse o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="121de-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="121de-112">OS</span><span class="sxs-lookup"><span data-stu-id="121de-112">PARAMETERS</span></span>

### <span data-ttu-id="121de-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="121de-113">-AadTenantId</span></span>
<span data-ttu-id="121de-114">Especifica a ID de locatário do Azure AD que será usada ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="121de-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="121de-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="121de-115">-CertificateFileContents</span></span>
<span data-ttu-id="121de-116">Especifica o conteúdo do arquivo do certificado que será usado ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="121de-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Byte[]
Parameter Sets: CertificateFileContents
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="121de-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="121de-117">-CertificateFilePath</span></span>
<span data-ttu-id="121de-118">Especifica o caminho do arquivo para o certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="121de-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="121de-119">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="121de-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: CertificateFilePath
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="121de-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="121de-120">-CertificatePassword</span></span>
<span data-ttu-id="121de-121">Especifica a senha do certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="121de-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="121de-122">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="121de-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="121de-123">-Config</span><span class="sxs-lookup"><span data-stu-id="121de-123">-Config</span></span>
<span data-ttu-id="121de-124">Especifica o objeto de configuração de cluster HDInsight que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="121de-124">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="121de-125">Esse objeto é criado pelo cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="121de-125">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="121de-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="121de-126">-DefaultProfile</span></span>
<span data-ttu-id="121de-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="121de-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="121de-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="121de-128">-ObjectId</span></span>
<span data-ttu-id="121de-129">Especifica a ID do objeto do AD do Azure (um GUID) da entidade de serviço do Azure AD que representa o cluster.</span><span class="sxs-lookup"><span data-stu-id="121de-129">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="121de-130">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="121de-130">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="121de-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="121de-131">CommonParameters</span></span>
<span data-ttu-id="121de-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="121de-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="121de-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="121de-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="121de-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="121de-134">INPUTS</span></span>

### <span data-ttu-id="121de-135">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="121de-135">AzureHDInsightConfig</span></span>
<span data-ttu-id="121de-136">O parâmetro ' config ' aceita o valor do tipo ' AzureHDInsightConfig ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="121de-136">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

### <span data-ttu-id="121de-137">#C0</span><span class="sxs-lookup"><span data-stu-id="121de-137">Guid</span></span>
<span data-ttu-id="121de-138">O parâmetro ' ObjectId ' aceita o valor do tipo ' GUID ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="121de-138">Parameter 'ObjectId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="121de-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="121de-139">OUTPUTS</span></span>

### <span data-ttu-id="121de-140">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="121de-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="121de-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="121de-141">NOTES</span></span>

## <span data-ttu-id="121de-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="121de-142">RELATED LINKS</span></span>

[<span data-ttu-id="121de-143">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="121de-143">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

