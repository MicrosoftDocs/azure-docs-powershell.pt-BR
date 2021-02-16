---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
ms.openlocfilehash: 6d3924f3613d01e515e58e1b35c3640b0447ca06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126942"
---
# <span data-ttu-id="a9585-101">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="a9585-101">Add-AzHDInsightClusterIdentity</span></span>

## <span data-ttu-id="a9585-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9585-102">SYNOPSIS</span></span>
<span data-ttu-id="a9585-103">Adiciona uma identidade de cluster a um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="a9585-103">Adds a cluster identity to a cluster configuration object.</span></span>

## <span data-ttu-id="a9585-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9585-104">SYNTAX</span></span>

### <span data-ttu-id="a9585-105">CertificateFilePath (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a9585-105">CertificateFilePath (Default)</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [[-ApplicationId] <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9585-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="a9585-106">CertificateFileContents</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [[-ApplicationId] <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9585-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9585-107">DESCRIPTION</span></span>
<span data-ttu-id="a9585-108">O cmdlet **Add-AzHDInsightClusterIdentity** adiciona uma identidade de cluster ao objeto de configuração HDInsight do Azure criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="a9585-108">The **Add-AzHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="a9585-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a9585-109">EXAMPLES</span></span>

### <span data-ttu-id="a9585-110">Exemplo 1: Adicionar informações de Identidade de Cluster ao objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="a9585-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
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

<span data-ttu-id="a9585-111">Esse comando adiciona informações de Identidade de Cluster ao cluster chamado seu-hadoop-001, permitindo que o cluster acesse o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a9585-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="a9585-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9585-112">PARAMETERS</span></span>

### <span data-ttu-id="a9585-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="a9585-113">-AadTenantId</span></span>
<span data-ttu-id="a9585-114">Especifica a ID de Locatário do Azure AD que será usada ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a9585-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a9585-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a9585-115">-ApplicationId</span></span>
<span data-ttu-id="a9585-116">A ID do Aplicativo Principal de Serviço para acessar o Lago de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9585-116">The Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="a9585-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="a9585-117">-CertificateFileContents</span></span>
<span data-ttu-id="a9585-118">Especifica o conteúdo do arquivo do certificado que será usado ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a9585-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a9585-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="a9585-119">-CertificateFilePath</span></span>
<span data-ttu-id="a9585-120">Especifica o caminho do arquivo para o certificado que será usado para autenticar como Entidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="a9585-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="a9585-121">O cluster usará isso ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a9585-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a9585-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a9585-122">-CertificatePassword</span></span>
<span data-ttu-id="a9585-123">Especifica a senha do certificado que será usado para autenticar como Entidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="a9585-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="a9585-124">O cluster usará isso ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a9585-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a9585-125">-Configuração</span><span class="sxs-lookup"><span data-stu-id="a9585-125">-Config</span></span>
<span data-ttu-id="a9585-126">Especifica o objeto de configuração de cluster HDInsight que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="a9585-126">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="a9585-127">Este objeto é criado pelo cmdlet New-AzHDInsightClusterConfig dados.</span><span class="sxs-lookup"><span data-stu-id="a9585-127">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="a9585-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9585-128">-DefaultProfile</span></span>
<span data-ttu-id="a9585-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a9585-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9585-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a9585-130">-ObjectId</span></span>
<span data-ttu-id="a9585-131">Especifica a ID de objeto do Azure AD (um GUID) da Entidade de Serviço do Azure AD que representa o cluster.</span><span class="sxs-lookup"><span data-stu-id="a9585-131">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="a9585-132">O cluster usará isso ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a9585-132">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a9585-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9585-133">CommonParameters</span></span>
<span data-ttu-id="a9585-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9585-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9585-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9585-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9585-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="a9585-136">INPUTS</span></span>

### <span data-ttu-id="a9585-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="a9585-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

### <span data-ttu-id="a9585-138">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a9585-138">System.Guid</span></span>

## <span data-ttu-id="a9585-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="a9585-139">OUTPUTS</span></span>

### <span data-ttu-id="a9585-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="a9585-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="a9585-141">Notas</span><span class="sxs-lookup"><span data-stu-id="a9585-141">NOTES</span></span>

## <span data-ttu-id="a9585-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9585-142">RELATED LINKS</span></span>

[<span data-ttu-id="a9585-143">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="a9585-143">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


