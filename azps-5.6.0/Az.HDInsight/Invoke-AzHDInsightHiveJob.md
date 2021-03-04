---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/invoke-azhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
ms.openlocfilehash: 2846848394cf6f376bd6b4064e193640806f81b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886341"
---
# <span data-ttu-id="aeeab-101">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="aeeab-101">Invoke-AzHDInsightHiveJob</span></span>

## <span data-ttu-id="aeeab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeeab-102">SYNOPSIS</span></span>
<span data-ttu-id="aeeab-103">Envia uma consulta Hive a um cluster HDInsight e recupera os resultados da consulta em uma operação.</span><span class="sxs-lookup"><span data-stu-id="aeeab-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

## <span data-ttu-id="aeeab-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aeeab-104">SYNTAX</span></span>

```
Invoke-AzHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aeeab-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aeeab-105">DESCRIPTION</span></span>
<span data-ttu-id="aeeab-106">O cmdlet **Invoke-AzHDInsightHiveJob** envia uma consulta hive a um cluster HDInsight do Azure e recupera os resultados da consulta em uma operação.</span><span class="sxs-lookup"><span data-stu-id="aeeab-106">The **Invoke-AzHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="aeeab-107">Use o cmdlet Use-AzHDInsightCluster antes de chamar **Invoke-AzHDInsightHiveJob** para especificar qual cluster será usado para a consulta.</span><span class="sxs-lookup"><span data-stu-id="aeeab-107">Use the Use-AzHDInsightCluster cmdlet before calling **Invoke-AzHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="aeeab-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aeeab-108">EXAMPLES</span></span>

### <span data-ttu-id="aeeab-109">Exemplo 1: Enviar uma consulta hive a um cluster HDInsight do Azure</span><span class="sxs-lookup"><span data-stu-id="aeeab-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="aeeab-110">Este comando envia as tabelas show de consulta para o cluster chamado your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="aeeab-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="aeeab-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aeeab-111">PARAMETERS</span></span>

### <span data-ttu-id="aeeab-112">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="aeeab-112">-Arguments</span></span>
<span data-ttu-id="aeeab-113">Especifica uma matriz de argumentos para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="aeeab-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="aeeab-114">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="aeeab-114">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="aeeab-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="aeeab-115">-DefaultContainer</span></span>
<span data-ttu-id="aeeab-116">Especifica o nome do contêiner padrão na conta padrão de Armazenamento do Azure que um cluster HDInsight usa.</span><span class="sxs-lookup"><span data-stu-id="aeeab-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="aeeab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeeab-117">-DefaultProfile</span></span>
<span data-ttu-id="aeeab-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="aeeab-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aeeab-119">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="aeeab-119">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="aeeab-120">Especifica a chave de conta da conta de armazenamento padrão que o cluster HDInsight usa.</span><span class="sxs-lookup"><span data-stu-id="aeeab-120">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="aeeab-121">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="aeeab-121">-DefaultStorageAccountName</span></span>
<span data-ttu-id="aeeab-122">Especifica o nome da conta de armazenamento padrão que o cluster HDInsight usa.</span><span class="sxs-lookup"><span data-stu-id="aeeab-122">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="aeeab-123">-Define</span><span class="sxs-lookup"><span data-stu-id="aeeab-123">-Defines</span></span>
<span data-ttu-id="aeeab-124">Especifica valores de configuração hadoop a ser definidos quando um trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="aeeab-124">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="aeeab-125">-File</span><span class="sxs-lookup"><span data-stu-id="aeeab-125">-File</span></span>
<span data-ttu-id="aeeab-126">Especifica o caminho para um arquivo no Armazenamento do Azure que contém a consulta a ser executado.</span><span class="sxs-lookup"><span data-stu-id="aeeab-126">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="aeeab-127">Você pode usar esse parâmetro em vez do *parâmetro Query.*</span><span class="sxs-lookup"><span data-stu-id="aeeab-127">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="aeeab-128">-Files</span><span class="sxs-lookup"><span data-stu-id="aeeab-128">-Files</span></span>
<span data-ttu-id="aeeab-129">Especifica uma coleção de arquivos que são necessários para um trabalho hive.</span><span class="sxs-lookup"><span data-stu-id="aeeab-129">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="aeeab-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="aeeab-130">-JobName</span></span>
<span data-ttu-id="aeeab-131">Especifica o nome de um trabalho hive.</span><span class="sxs-lookup"><span data-stu-id="aeeab-131">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="aeeab-132">Se você não especificar esse parâmetro, este cmdlet usará o valor padrão: "Hive: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="aeeab-132">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="aeeab-133">-Query</span><span class="sxs-lookup"><span data-stu-id="aeeab-133">-Query</span></span>
<span data-ttu-id="aeeab-134">Especifica a consulta Hive.</span><span class="sxs-lookup"><span data-stu-id="aeeab-134">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="aeeab-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="aeeab-135">-RunAsFileJob</span></span>
<span data-ttu-id="aeeab-136">Indica que esse cmdlet cria um arquivo na conta de armazenamento padrão do Azure na qual armazenar uma consulta.</span><span class="sxs-lookup"><span data-stu-id="aeeab-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="aeeab-137">Este cmdlet envia o trabalho que faz referência a esse arquivo como um script a ser executado.</span><span class="sxs-lookup"><span data-stu-id="aeeab-137">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="aeeab-138">Você pode usar essa funcionalidade para manipular caracteres especiais, como sinal de porcentagem (%) que falharia em um envio de trabalho por meio de Templeton, porque Templeton interpreta uma consulta com um sinal de porcentagem como um parâmetro URL.</span><span class="sxs-lookup"><span data-stu-id="aeeab-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="aeeab-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="aeeab-139">-StatusFolder</span></span>
<span data-ttu-id="aeeab-140">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="aeeab-140">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="aeeab-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeeab-141">CommonParameters</span></span>
<span data-ttu-id="aeeab-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeeab-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeeab-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aeeab-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeeab-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aeeab-144">INPUTS</span></span>

### <span data-ttu-id="aeeab-145">Nenhum</span><span class="sxs-lookup"><span data-stu-id="aeeab-145">None</span></span>

## <span data-ttu-id="aeeab-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aeeab-146">OUTPUTS</span></span>

### <span data-ttu-id="aeeab-147">System.String</span><span class="sxs-lookup"><span data-stu-id="aeeab-147">System.String</span></span>

## <span data-ttu-id="aeeab-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="aeeab-148">NOTES</span></span>

## <span data-ttu-id="aeeab-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aeeab-149">RELATED LINKS</span></span>

[<span data-ttu-id="aeeab-150">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="aeeab-150">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


