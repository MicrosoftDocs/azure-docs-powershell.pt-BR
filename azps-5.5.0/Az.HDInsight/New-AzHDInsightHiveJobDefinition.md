---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: 4cf45d237d5611d5d9fb0fb1eb178d2c85807354
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116781"
---
# <span data-ttu-id="b4e25-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b4e25-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="b4e25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4e25-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e25-103">Cria um objeto de trabalho de Colmeia.</span><span class="sxs-lookup"><span data-stu-id="b4e25-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="b4e25-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4e25-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4e25-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4e25-105">DESCRIPTION</span></span>
<span data-ttu-id="b4e25-106">O cmdlet **New-AzHDInsightHive JobDefinition** define um objeto de trabalho Desmaio para ser usado com um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4e25-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b4e25-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b4e25-107">EXAMPLES</span></span>

### <span data-ttu-id="b4e25-108">Exemplo 1: Criar uma definição de trabalho de Colmeia</span><span class="sxs-lookup"><span data-stu-id="b4e25-108">Example 1: Create a Hive job definition</span></span>
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

<span data-ttu-id="b4e25-109">Esse comando cria uma definição de trabalho de Colmeia.</span><span class="sxs-lookup"><span data-stu-id="b4e25-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="b4e25-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4e25-110">PARAMETERS</span></span>

### <span data-ttu-id="b4e25-111">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="b4e25-111">-Arguments</span></span>
<span data-ttu-id="b4e25-112">Especifica uma matriz de argumentos para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4e25-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="b4e25-113">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="b4e25-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="b4e25-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e25-114">-DefaultProfile</span></span>
<span data-ttu-id="b4e25-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b4e25-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4e25-116">-Define</span><span class="sxs-lookup"><span data-stu-id="b4e25-116">-Defines</span></span>
<span data-ttu-id="b4e25-117">Especifica valores de configuração hadoop para definir quando o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="b4e25-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="b4e25-118">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="b4e25-118">-File</span></span>
<span data-ttu-id="b4e25-119">Especifica o caminho para um arquivo que contém a consulta a ser executado.</span><span class="sxs-lookup"><span data-stu-id="b4e25-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="b4e25-120">O arquivo deve estar disponível na conta de armazenamento associada ao cluster.</span><span class="sxs-lookup"><span data-stu-id="b4e25-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="b4e25-121">Você pode usar esse parâmetro em vez do *parâmetro Consulta.*</span><span class="sxs-lookup"><span data-stu-id="b4e25-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="b4e25-122">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="b4e25-122">-Files</span></span>
<span data-ttu-id="b4e25-123">Especifica um conjunto de arquivos associados a um trabalho de Colmeia.</span><span class="sxs-lookup"><span data-stu-id="b4e25-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="b4e25-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="b4e25-124">-JobName</span></span>
<span data-ttu-id="b4e25-125">Especifica o nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4e25-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="b4e25-126">-Consulta</span><span class="sxs-lookup"><span data-stu-id="b4e25-126">-Query</span></span>
<span data-ttu-id="b4e25-127">Especifica a consulta Colmeia.</span><span class="sxs-lookup"><span data-stu-id="b4e25-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="b4e25-128">-RunAsFileFileFile</span><span class="sxs-lookup"><span data-stu-id="b4e25-128">-RunAsFileJob</span></span>
<span data-ttu-id="b4e25-129">Indica que esse cmdlet cria um arquivo na conta de armazenamento padrão do Azure para armazenar uma consulta.</span><span class="sxs-lookup"><span data-stu-id="b4e25-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="b4e25-130">Este cmdlet envia o trabalho que faz referência a esse arquivo como um script a ser executado.</span><span class="sxs-lookup"><span data-stu-id="b4e25-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="b4e25-131">Você pode usar essa funcionalidade para lidar com caracteres especiais, como o sinal de porcentagem (%) que falharia em um envio de trabalho por meio de Templeton, porque Templeton interpreta uma consulta com um sinal de porcentagem como um parâmetro de URL.</span><span class="sxs-lookup"><span data-stu-id="b4e25-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="b4e25-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="b4e25-132">-StatusFolder</span></span>
<span data-ttu-id="b4e25-133">Especifica o local da pasta que contém saídas padrão e saídas de erros para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4e25-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="b4e25-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e25-134">CommonParameters</span></span>
<span data-ttu-id="b4e25-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4e25-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e25-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4e25-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e25-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="b4e25-137">INPUTS</span></span>

### <span data-ttu-id="b4e25-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b4e25-138">None</span></span>

## <span data-ttu-id="b4e25-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="b4e25-139">OUTPUTS</span></span>

### <span data-ttu-id="b4e25-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b4e25-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="b4e25-141">Notas</span><span class="sxs-lookup"><span data-stu-id="b4e25-141">NOTES</span></span>

## <span data-ttu-id="b4e25-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4e25-142">RELATED LINKS</span></span>

[<span data-ttu-id="b4e25-143">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b4e25-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


