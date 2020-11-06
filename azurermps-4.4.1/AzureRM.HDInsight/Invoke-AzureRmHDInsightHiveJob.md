---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
ms.openlocfilehash: 127e949bfaa9d54644f7f690cfefbf095d477374
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441074"
---
# <span data-ttu-id="a4c33-101">Invoke-AzureRmHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="a4c33-101">Invoke-AzureRmHDInsightHiveJob</span></span>

## <span data-ttu-id="a4c33-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4c33-102">SYNOPSIS</span></span>
<span data-ttu-id="a4c33-103">Envia uma consulta Hive para um cluster HDInsight e recupera resultados de consulta em uma operação.</span><span class="sxs-lookup"><span data-stu-id="a4c33-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4c33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4c33-104">SYNTAX</span></span>

```
Invoke-AzureRmHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4c33-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a4c33-105">DESCRIPTION</span></span>
<span data-ttu-id="a4c33-106">O cmdlet **Invoke-AzureRmHDInsightHiveJob** envia uma consulta Hive para um cluster do Azure HDInsight e recupera resultados de consulta em uma operação.</span><span class="sxs-lookup"><span data-stu-id="a4c33-106">The **Invoke-AzureRmHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="a4c33-107">Use o cmdlet Use-AzureRmHDInsightCluster antes de chamar **Invoke-AzureRmHDInsightHiveJob** para especificar qual cluster será usado para a consulta.</span><span class="sxs-lookup"><span data-stu-id="a4c33-107">Use the Use-AzureRmHDInsightCluster cmdlet before calling **Invoke-AzureRmHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="a4c33-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4c33-108">EXAMPLES</span></span>

### <span data-ttu-id="a4c33-109">Exemplo 1: Enviar uma consulta de Hive para um cluster do Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="a4c33-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
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

<span data-ttu-id="a4c33-110">Esse comando envia a consulta de mostrar tabelas para o cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="a4c33-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a4c33-111">OS</span><span class="sxs-lookup"><span data-stu-id="a4c33-111">PARAMETERS</span></span>

### <span data-ttu-id="a4c33-112">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="a4c33-112">-Arguments</span></span>
<span data-ttu-id="a4c33-113">Especifica uma matriz de argumentos para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="a4c33-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="a4c33-114">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="a4c33-114">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="a4c33-115">-Defaultcontainer</span><span class="sxs-lookup"><span data-stu-id="a4c33-115">-DefaultContainer</span></span>
<span data-ttu-id="a4c33-116">Especifica o nome do contêiner padrão na conta de armazenamento padrão do Azure que um cluster HDInsight usa.</span><span class="sxs-lookup"><span data-stu-id="a4c33-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="a4c33-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a4c33-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="a4c33-118">Especifica a chave de conta para a conta de armazenamento padrão que o cluster HDInsight usa.</span><span class="sxs-lookup"><span data-stu-id="a4c33-118">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="a4c33-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a4c33-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="a4c33-120">Especifica o nome da conta de armazenamento padrão que o cluster HDInsight usa.</span><span class="sxs-lookup"><span data-stu-id="a4c33-120">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="a4c33-121">-Define</span><span class="sxs-lookup"><span data-stu-id="a4c33-121">-Defines</span></span>
<span data-ttu-id="a4c33-122">Especifica os valores de configuração Hadoop a serem definidos quando um trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="a4c33-122">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="a4c33-123">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="a4c33-123">-File</span></span>
<span data-ttu-id="a4c33-124">Especifica o caminho para um arquivo no armazenamento do Azure que contém a consulta a ser executada.</span><span class="sxs-lookup"><span data-stu-id="a4c33-124">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="a4c33-125">Você pode usar esse parâmetro em vez do parâmetro de *consulta* .</span><span class="sxs-lookup"><span data-stu-id="a4c33-125">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="a4c33-126">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="a4c33-126">-Files</span></span>
<span data-ttu-id="a4c33-127">Especifica uma coleção de arquivos necessários para um trabalho de Hive.</span><span class="sxs-lookup"><span data-stu-id="a4c33-127">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="a4c33-128">-JobName</span><span class="sxs-lookup"><span data-stu-id="a4c33-128">-JobName</span></span>
<span data-ttu-id="a4c33-129">Especifica o nome de um trabalho de Hive.</span><span class="sxs-lookup"><span data-stu-id="a4c33-129">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="a4c33-130">Se você não especificar esse parâmetro, esse cmdlet usará o valor padrão: "Hive: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="a4c33-130">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="a4c33-131">-Consulta</span><span class="sxs-lookup"><span data-stu-id="a4c33-131">-Query</span></span>
<span data-ttu-id="a4c33-132">Especifica a consulta Hive.</span><span class="sxs-lookup"><span data-stu-id="a4c33-132">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="a4c33-133">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="a4c33-133">-RunAsFileJob</span></span>
<span data-ttu-id="a4c33-134">Indica que esse cmdlet cria um arquivo na conta de armazenamento padrão do Azure para armazenar uma consulta.</span><span class="sxs-lookup"><span data-stu-id="a4c33-134">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="a4c33-135">Esse cmdlet envia o trabalho que faz referência a esse arquivo como um script para ser executado.</span><span class="sxs-lookup"><span data-stu-id="a4c33-135">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="a4c33-136">Você pode usar essa funcionalidade para manipular caracteres especiais, como o sinal de porcentagem (%) Isso falharia em um envio de trabalho por meio de Templeton, porque Templeton interpreta uma consulta com um sinal de porcentagem como parâmetro de URL.</span><span class="sxs-lookup"><span data-stu-id="a4c33-136">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="a4c33-137">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="a4c33-137">-StatusFolder</span></span>
<span data-ttu-id="a4c33-138">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="a4c33-138">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="a4c33-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4c33-139">-DefaultProfile</span></span>
<span data-ttu-id="a4c33-140">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a4c33-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4c33-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c33-141">CommonParameters</span></span>
<span data-ttu-id="a4c33-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4c33-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c33-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4c33-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c33-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a4c33-144">INPUTS</span></span>

## <span data-ttu-id="a4c33-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a4c33-145">OUTPUTS</span></span>

### <span data-ttu-id="a4c33-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a4c33-146">System.String</span></span>

## <span data-ttu-id="a4c33-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a4c33-147">NOTES</span></span>

## <span data-ttu-id="a4c33-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4c33-148">RELATED LINKS</span></span>

[<span data-ttu-id="a4c33-149">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a4c33-149">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


