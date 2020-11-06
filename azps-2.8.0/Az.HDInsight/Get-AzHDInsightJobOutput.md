---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
ms.openlocfilehash: 3d4ffa7a3172921b8aba7d73fc2c468c0e3117f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596367"
---
# <span data-ttu-id="bb3a6-101">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="bb3a6-101">Get-AzHDInsightJobOutput</span></span>

## <span data-ttu-id="bb3a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb3a6-102">SYNOPSIS</span></span>
<span data-ttu-id="bb3a6-103">Obtém a saída do log para um trabalho da conta de armazenamento associada a um cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="bb3a6-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

## <span data-ttu-id="bb3a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb3a6-104">SYNTAX</span></span>

```
Get-AzHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb3a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb3a6-105">DESCRIPTION</span></span>
<span data-ttu-id="bb3a6-106">O cmdlet **Get-AzHDInsightJobOutput** Obtém a saída de log para um trabalho da conta de armazenamento associada a um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bb3a6-106">The **Get-AzHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="bb3a6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb3a6-107">EXAMPLES</span></span>

### <span data-ttu-id="bb3a6-108">Exemplo 1: obter a saída do log para um trabalho</span><span class="sxs-lookup"><span data-stu-id="bb3a6-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="bb3a6-109">Esse comando obtém a saída do log do cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="bb3a6-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="bb3a6-110">OS</span><span class="sxs-lookup"><span data-stu-id="bb3a6-110">PARAMETERS</span></span>

### <span data-ttu-id="bb3a6-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bb3a6-111">-ClusterName</span></span>
<span data-ttu-id="bb3a6-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="bb3a6-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="bb3a6-113">-Defaultcontainer</span><span class="sxs-lookup"><span data-stu-id="bb3a6-113">-DefaultContainer</span></span>
<span data-ttu-id="bb3a6-114">Especifica o nome do contêiner padrão.</span><span class="sxs-lookup"><span data-stu-id="bb3a6-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="bb3a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb3a6-115">-DefaultProfile</span></span>
<span data-ttu-id="bb3a6-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bb3a6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb3a6-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bb3a6-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="bb3a6-118">Especifica a chave da conta de armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="bb3a6-118">Specifies the default Storage account key.</span></span>

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

### <span data-ttu-id="bb3a6-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bb3a6-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="bb3a6-120">Especifica o nome da conta de armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="bb3a6-120">Specifies the default Storage account name.</span></span>

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

### <span data-ttu-id="bb3a6-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="bb3a6-121">-DisplayOutputType</span></span>
<span data-ttu-id="bb3a6-122">Especifica o tipo de saída do trabalho que está sendo solicitado.</span><span class="sxs-lookup"><span data-stu-id="bb3a6-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="bb3a6-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bb3a6-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bb3a6-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="bb3a6-124">StandardOutput</span></span>
- <span data-ttu-id="bb3a6-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="bb3a6-125">StandardError</span></span>

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

### <span data-ttu-id="bb3a6-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="bb3a6-126">-HttpCredential</span></span>
<span data-ttu-id="bb3a6-127">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="bb3a6-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="bb3a6-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="bb3a6-128">-JobId</span></span>
<span data-ttu-id="bb3a6-129">Especifica a ID do trabalho cuja saída será buscada.</span><span class="sxs-lookup"><span data-stu-id="bb3a6-129">Specifies the job ID of the job whose output will be fetched.</span></span>

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

### <span data-ttu-id="bb3a6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb3a6-130">-ResourceGroupName</span></span>
<span data-ttu-id="bb3a6-131">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb3a6-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bb3a6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb3a6-132">CommonParameters</span></span>
<span data-ttu-id="bb3a6-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb3a6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb3a6-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb3a6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb3a6-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb3a6-135">INPUTS</span></span>

### <span data-ttu-id="bb3a6-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bb3a6-136">None</span></span>

## <span data-ttu-id="bb3a6-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb3a6-137">OUTPUTS</span></span>

### <span data-ttu-id="bb3a6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bb3a6-138">System.String</span></span>

## <span data-ttu-id="bb3a6-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb3a6-139">NOTES</span></span>

## <span data-ttu-id="bb3a6-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb3a6-140">RELATED LINKS</span></span>

[<span data-ttu-id="bb3a6-141">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="bb3a6-141">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="bb3a6-142">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="bb3a6-142">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


