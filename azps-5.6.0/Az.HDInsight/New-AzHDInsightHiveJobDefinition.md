---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: be8878d338206e1355dc36082d4f9941cf141838
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892777"
---
# <span data-ttu-id="63660-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="63660-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="63660-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63660-102">SYNOPSIS</span></span>
<span data-ttu-id="63660-103">Cria um objeto de trabalho hive.</span><span class="sxs-lookup"><span data-stu-id="63660-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="63660-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="63660-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63660-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="63660-105">DESCRIPTION</span></span>
<span data-ttu-id="63660-106">O cmdlet **New-AzHDInsightHiveJobDefinition** define um objeto de trabalho hive para uso com um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="63660-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="63660-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63660-107">EXAMPLES</span></span>

### <span data-ttu-id="63660-108">Exemplo 1: Criar uma definição de trabalho hive</span><span class="sxs-lookup"><span data-stu-id="63660-108">Example 1: Create a Hive job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="63660-109">Este comando cria uma definição de trabalho hive.</span><span class="sxs-lookup"><span data-stu-id="63660-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="63660-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="63660-110">PARAMETERS</span></span>

### <span data-ttu-id="63660-111">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="63660-111">-Arguments</span></span>
<span data-ttu-id="63660-112">Especifica uma matriz de argumentos para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="63660-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="63660-113">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="63660-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="63660-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63660-114">-DefaultProfile</span></span>
<span data-ttu-id="63660-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="63660-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63660-116">-Define</span><span class="sxs-lookup"><span data-stu-id="63660-116">-Defines</span></span>
<span data-ttu-id="63660-117">Especifica valores de configuração hadoop a ser definidos para quando o trabalho for executado.</span><span class="sxs-lookup"><span data-stu-id="63660-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63660-118">-File</span><span class="sxs-lookup"><span data-stu-id="63660-118">-File</span></span>
<span data-ttu-id="63660-119">Especifica o caminho para um arquivo que contém a consulta a ser executado.</span><span class="sxs-lookup"><span data-stu-id="63660-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="63660-120">O arquivo deve estar disponível na conta de armazenamento associada ao cluster.</span><span class="sxs-lookup"><span data-stu-id="63660-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="63660-121">Você pode usar esse parâmetro em vez do *parâmetro Query.*</span><span class="sxs-lookup"><span data-stu-id="63660-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="63660-122">-Files</span><span class="sxs-lookup"><span data-stu-id="63660-122">-Files</span></span>
<span data-ttu-id="63660-123">Especifica uma coleção de arquivos que estão associados a um trabalho hive.</span><span class="sxs-lookup"><span data-stu-id="63660-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="63660-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="63660-124">-JobName</span></span>
<span data-ttu-id="63660-125">Especifica o nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="63660-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="63660-126">-Query</span><span class="sxs-lookup"><span data-stu-id="63660-126">-Query</span></span>
<span data-ttu-id="63660-127">Especifica a consulta Hive.</span><span class="sxs-lookup"><span data-stu-id="63660-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="63660-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="63660-128">-RunAsFileJob</span></span>
<span data-ttu-id="63660-129">Indica que esse cmdlet cria um arquivo na conta de armazenamento padrão do Azure na qual armazenar uma consulta.</span><span class="sxs-lookup"><span data-stu-id="63660-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="63660-130">Este cmdlet envia o trabalho que faz referência a esse arquivo como um script a ser executado.</span><span class="sxs-lookup"><span data-stu-id="63660-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="63660-131">Você pode usar essa funcionalidade para manipular caracteres especiais, como sinal de porcentagem (%) que falharia em um envio de trabalho por meio de Templeton, porque Templeton interpreta uma consulta com um sinal de porcentagem como um parâmetro URL.</span><span class="sxs-lookup"><span data-stu-id="63660-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63660-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="63660-132">-StatusFolder</span></span>
<span data-ttu-id="63660-133">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="63660-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="63660-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63660-134">CommonParameters</span></span>
<span data-ttu-id="63660-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63660-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63660-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63660-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63660-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63660-137">INPUTS</span></span>

### <span data-ttu-id="63660-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="63660-138">None</span></span>

## <span data-ttu-id="63660-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="63660-139">OUTPUTS</span></span>

### <span data-ttu-id="63660-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="63660-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="63660-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="63660-141">NOTES</span></span>

## <span data-ttu-id="63660-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63660-142">RELATED LINKS</span></span>

[<span data-ttu-id="63660-143">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="63660-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


