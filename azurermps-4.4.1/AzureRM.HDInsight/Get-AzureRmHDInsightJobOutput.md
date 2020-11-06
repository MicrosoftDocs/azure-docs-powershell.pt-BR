---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
ms.openlocfilehash: eebbe6fb233b0d6117411973e841cf39f2ae377d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432210"
---
# <span data-ttu-id="47162-101">Get-AzureRmHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="47162-101">Get-AzureRmHDInsightJobOutput</span></span>

## <span data-ttu-id="47162-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47162-102">SYNOPSIS</span></span>
<span data-ttu-id="47162-103">Obtém a saída do log para um trabalho da conta de armazenamento associada a um cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="47162-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47162-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47162-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47162-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47162-105">DESCRIPTION</span></span>
<span data-ttu-id="47162-106">O cmdlet **Get-AzureRmHDInsightJobOutput** Obtém a saída de log para um trabalho da conta de armazenamento associada a um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="47162-106">The **Get-AzureRmHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="47162-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47162-107">EXAMPLES</span></span>

### <span data-ttu-id="47162-108">Exemplo 1: obter a saída do log para um trabalho</span><span class="sxs-lookup"><span data-stu-id="47162-108">Example 1: Get the log output for a job</span></span>
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

<span data-ttu-id="47162-109">Esse comando obtém a saída do log do cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="47162-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="47162-110">OS</span><span class="sxs-lookup"><span data-stu-id="47162-110">PARAMETERS</span></span>

### <span data-ttu-id="47162-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="47162-111">-ClusterName</span></span>
<span data-ttu-id="47162-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="47162-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="47162-113">-Defaultcontainer</span><span class="sxs-lookup"><span data-stu-id="47162-113">-DefaultContainer</span></span>
<span data-ttu-id="47162-114">Especifica o nome do contêiner padrão.</span><span class="sxs-lookup"><span data-stu-id="47162-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="47162-115">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="47162-115">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="47162-116">Especifica a chave da conta de armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="47162-116">Specifies the default Storage account key.</span></span>

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

### <span data-ttu-id="47162-117">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="47162-117">-DefaultStorageAccountName</span></span>
<span data-ttu-id="47162-118">Especifica o nome da conta de armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="47162-118">Specifies the default Storage account name.</span></span>

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

### <span data-ttu-id="47162-119">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="47162-119">-DisplayOutputType</span></span>
<span data-ttu-id="47162-120">Especifica o tipo de saída do trabalho que está sendo solicitado.</span><span class="sxs-lookup"><span data-stu-id="47162-120">Specifies the job output type being requested.</span></span>
<span data-ttu-id="47162-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="47162-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47162-122">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="47162-122">StandardOutput</span></span>
- <span data-ttu-id="47162-123">StandardError</span><span class="sxs-lookup"><span data-stu-id="47162-123">StandardError</span></span>

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

### <span data-ttu-id="47162-124">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="47162-124">-HttpCredential</span></span>
<span data-ttu-id="47162-125">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="47162-125">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="47162-126">-JobId</span><span class="sxs-lookup"><span data-stu-id="47162-126">-JobId</span></span>
<span data-ttu-id="47162-127">Especifica a ID do trabalho cuja saída será buscada.</span><span class="sxs-lookup"><span data-stu-id="47162-127">Specifies the job ID of the job whose output will be fetched.</span></span>

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

### <span data-ttu-id="47162-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47162-128">-ResourceGroupName</span></span>
<span data-ttu-id="47162-129">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="47162-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="47162-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47162-130">-DefaultProfile</span></span>
<span data-ttu-id="47162-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47162-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47162-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47162-132">CommonParameters</span></span>
<span data-ttu-id="47162-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47162-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47162-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47162-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47162-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47162-135">INPUTS</span></span>

## <span data-ttu-id="47162-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47162-136">OUTPUTS</span></span>

### <span data-ttu-id="47162-137">System. String</span><span class="sxs-lookup"><span data-stu-id="47162-137">System.String</span></span>

## <span data-ttu-id="47162-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47162-138">NOTES</span></span>

## <span data-ttu-id="47162-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47162-139">RELATED LINKS</span></span>

[<span data-ttu-id="47162-140">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="47162-140">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="47162-141">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="47162-141">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


