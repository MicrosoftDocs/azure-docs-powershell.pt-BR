---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
ms.openlocfilehash: 94bd90b644b12723a36266dea34d9b5e9417b45b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430272"
---
# <span data-ttu-id="647b0-101">Get-AzureRmHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="647b0-101">Get-AzureRmHDInsightJobOutput</span></span>

## <span data-ttu-id="647b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="647b0-102">SYNOPSIS</span></span>
<span data-ttu-id="647b0-103">Obtém a saída do log para um trabalho da conta de armazenamento associada a um cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="647b0-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="647b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="647b0-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="647b0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="647b0-105">DESCRIPTION</span></span>
<span data-ttu-id="647b0-106">O cmdlet **Get-AzureRmHDInsightJobOutput** Obtém a saída de log para um trabalho da conta de armazenamento associada a um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="647b0-106">The **Get-AzureRmHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="647b0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="647b0-107">EXAMPLES</span></span>

### <span data-ttu-id="647b0-108">Exemplo 1: obter a saída do log para um trabalho</span><span class="sxs-lookup"><span data-stu-id="647b0-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="647b0-109">Esse comando obtém a saída do log do cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="647b0-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="647b0-110">OS</span><span class="sxs-lookup"><span data-stu-id="647b0-110">PARAMETERS</span></span>

### <span data-ttu-id="647b0-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="647b0-111">-ClusterName</span></span>
<span data-ttu-id="647b0-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="647b0-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="647b0-113">-Defaultcontainer</span><span class="sxs-lookup"><span data-stu-id="647b0-113">-DefaultContainer</span></span>
<span data-ttu-id="647b0-114">Especifica o nome do contêiner padrão.</span><span class="sxs-lookup"><span data-stu-id="647b0-114">Specifies the default container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="647b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="647b0-115">-DefaultProfile</span></span>
<span data-ttu-id="647b0-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="647b0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="647b0-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="647b0-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="647b0-118">Especifica a chave da conta de armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="647b0-118">Specifies the default Storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="647b0-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="647b0-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="647b0-120">Especifica o nome da conta de armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="647b0-120">Specifies the default Storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="647b0-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="647b0-121">-DisplayOutputType</span></span>
<span data-ttu-id="647b0-122">Especifica o tipo de saída do trabalho que está sendo solicitado.</span><span class="sxs-lookup"><span data-stu-id="647b0-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="647b0-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="647b0-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="647b0-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="647b0-124">StandardOutput</span></span>
- <span data-ttu-id="647b0-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="647b0-125">StandardError</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Job.JobDisplayOutputType
Parameter Sets: (All)
Aliases:
Accepted values: StandardOutput, StandardError

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="647b0-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="647b0-126">-HttpCredential</span></span>
<span data-ttu-id="647b0-127">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="647b0-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="647b0-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="647b0-128">-JobId</span></span>
<span data-ttu-id="647b0-129">Especifica a ID do trabalho cuja saída será buscada.</span><span class="sxs-lookup"><span data-stu-id="647b0-129">Specifies the job ID of the job whose output will be fetched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="647b0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="647b0-130">-ResourceGroupName</span></span>
<span data-ttu-id="647b0-131">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="647b0-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="647b0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="647b0-132">CommonParameters</span></span>
<span data-ttu-id="647b0-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="647b0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="647b0-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="647b0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="647b0-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="647b0-135">INPUTS</span></span>

### <span data-ttu-id="647b0-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="647b0-136">None</span></span>

## <span data-ttu-id="647b0-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="647b0-137">OUTPUTS</span></span>

### <span data-ttu-id="647b0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="647b0-138">System.String</span></span>

## <span data-ttu-id="647b0-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="647b0-139">NOTES</span></span>

## <span data-ttu-id="647b0-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="647b0-140">RELATED LINKS</span></span>

[<span data-ttu-id="647b0-141">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="647b0-141">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="647b0-142">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="647b0-142">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


