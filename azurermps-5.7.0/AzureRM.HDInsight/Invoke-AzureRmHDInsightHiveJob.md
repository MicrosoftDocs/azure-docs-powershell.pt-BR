---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/invoke-azurermhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
ms.openlocfilehash: 96c8baef5263756cb0c4e58a5b8d03ee08573cea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432124"
---
# <span data-ttu-id="25aa6-101">Invoke-AzureRmHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="25aa6-101">Invoke-AzureRmHDInsightHiveJob</span></span>

## <span data-ttu-id="25aa6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25aa6-102">SYNOPSIS</span></span>
<span data-ttu-id="25aa6-103">Envia uma consulta Hive para um cluster HDInsight e recupera resultados de consulta em uma operação.</span><span class="sxs-lookup"><span data-stu-id="25aa6-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25aa6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25aa6-104">SYNTAX</span></span>

```
Invoke-AzureRmHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25aa6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25aa6-105">DESCRIPTION</span></span>
<span data-ttu-id="25aa6-106">O cmdlet **Invoke-AzureRmHDInsightHiveJob** envia uma consulta Hive para um cluster do Azure HDInsight e recupera resultados de consulta em uma operação.</span><span class="sxs-lookup"><span data-stu-id="25aa6-106">The **Invoke-AzureRmHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="25aa6-107">Use o cmdlet Use-AzureRmHDInsightCluster antes de chamar **Invoke-AzureRmHDInsightHiveJob** para especificar qual cluster será usado para a consulta.</span><span class="sxs-lookup"><span data-stu-id="25aa6-107">Use the Use-AzureRmHDInsightCluster cmdlet before calling **Invoke-AzureRmHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="25aa6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25aa6-108">EXAMPLES</span></span>

### <span data-ttu-id="25aa6-109">Exemplo 1: Enviar uma consulta de Hive para um cluster do Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="25aa6-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzureRmHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzureRmHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageAccountContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="25aa6-110">Esse comando envia a consulta de mostrar tabelas para o cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="25aa6-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="25aa6-111">OS</span><span class="sxs-lookup"><span data-stu-id="25aa6-111">PARAMETERS</span></span>

### <span data-ttu-id="25aa6-112">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="25aa6-112">-Arguments</span></span>
<span data-ttu-id="25aa6-113">Especifica uma matriz de argumentos para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="25aa6-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="25aa6-114">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="25aa6-114">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25aa6-115">-Defaultcontainer</span><span class="sxs-lookup"><span data-stu-id="25aa6-115">-DefaultContainer</span></span>
<span data-ttu-id="25aa6-116">Especifica o nome do contêiner padrão na conta de armazenamento padrão do Azure que um cluster HDInsight usa.</span><span class="sxs-lookup"><span data-stu-id="25aa6-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25aa6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25aa6-117">-DefaultProfile</span></span>
<span data-ttu-id="25aa6-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="25aa6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25aa6-119">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="25aa6-119">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="25aa6-120">Especifica a chave de conta para a conta de armazenamento padrão que o cluster HDInsight usa.</span><span class="sxs-lookup"><span data-stu-id="25aa6-120">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25aa6-121">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="25aa6-121">-DefaultStorageAccountName</span></span>
<span data-ttu-id="25aa6-122">Especifica o nome da conta de armazenamento padrão que o cluster HDInsight usa.</span><span class="sxs-lookup"><span data-stu-id="25aa6-122">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25aa6-123">-Define</span><span class="sxs-lookup"><span data-stu-id="25aa6-123">-Defines</span></span>
<span data-ttu-id="25aa6-124">Especifica os valores de configuração Hadoop a serem definidos quando um trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="25aa6-124">Specifies Hadoop configuration values to set when a job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25aa6-125">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="25aa6-125">-File</span></span>
<span data-ttu-id="25aa6-126">Especifica o caminho para um arquivo no armazenamento do Azure que contém a consulta a ser executada.</span><span class="sxs-lookup"><span data-stu-id="25aa6-126">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="25aa6-127">Você pode usar esse parâmetro em vez do parâmetro de *consulta* .</span><span class="sxs-lookup"><span data-stu-id="25aa6-127">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25aa6-128">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="25aa6-128">-Files</span></span>
<span data-ttu-id="25aa6-129">Especifica uma coleção de arquivos necessários para um trabalho de Hive.</span><span class="sxs-lookup"><span data-stu-id="25aa6-129">Specifies a collection of files that are required for a Hive job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25aa6-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="25aa6-130">-JobName</span></span>
<span data-ttu-id="25aa6-131">Especifica o nome de um trabalho de Hive.</span><span class="sxs-lookup"><span data-stu-id="25aa6-131">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="25aa6-132">Se você não especificar esse parâmetro, esse cmdlet usará o valor padrão: "Hive: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="25aa6-132">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25aa6-133">-Consulta</span><span class="sxs-lookup"><span data-stu-id="25aa6-133">-Query</span></span>
<span data-ttu-id="25aa6-134">Especifica a consulta Hive.</span><span class="sxs-lookup"><span data-stu-id="25aa6-134">Specifies the Hive query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25aa6-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="25aa6-135">-RunAsFileJob</span></span>
<span data-ttu-id="25aa6-136">Indica que esse cmdlet cria um arquivo na conta de armazenamento padrão do Azure para armazenar uma consulta.</span><span class="sxs-lookup"><span data-stu-id="25aa6-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="25aa6-137">Esse cmdlet envia o trabalho que faz referência a esse arquivo como um script para ser executado.</span><span class="sxs-lookup"><span data-stu-id="25aa6-137">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="25aa6-138">Você pode usar essa funcionalidade para manipular caracteres especiais, como o sinal de porcentagem (%) Isso falharia em um envio de trabalho por meio de Templeton, porque Templeton interpreta uma consulta com um sinal de porcentagem como parâmetro de URL.</span><span class="sxs-lookup"><span data-stu-id="25aa6-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25aa6-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="25aa6-139">-StatusFolder</span></span>
<span data-ttu-id="25aa6-140">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="25aa6-140">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25aa6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25aa6-141">CommonParameters</span></span>
<span data-ttu-id="25aa6-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25aa6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25aa6-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25aa6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25aa6-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25aa6-144">INPUTS</span></span>

### <span data-ttu-id="25aa6-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="25aa6-145">None</span></span>
<span data-ttu-id="25aa6-146">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="25aa6-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25aa6-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25aa6-147">OUTPUTS</span></span>

### <span data-ttu-id="25aa6-148">System. String</span><span class="sxs-lookup"><span data-stu-id="25aa6-148">System.String</span></span>

## <span data-ttu-id="25aa6-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25aa6-149">NOTES</span></span>

## <span data-ttu-id="25aa6-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25aa6-150">RELATED LINKS</span></span>

[<span data-ttu-id="25aa6-151">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="25aa6-151">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


