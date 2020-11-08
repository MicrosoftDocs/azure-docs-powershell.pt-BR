---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: cf1e0738a01d2b8f3219f2732995182fe7f6959d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112525"
---
# <span data-ttu-id="e5080-101">Save-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="e5080-101">Save-AzDataFactoryLog</span></span>

## <span data-ttu-id="e5080-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5080-102">SYNOPSIS</span></span>
<span data-ttu-id="e5080-103">Baixa os arquivos de log do processamento do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e5080-103">Downloads log files from Azure HDInsight processing.</span></span>

## <span data-ttu-id="e5080-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5080-104">SYNTAX</span></span>

### <span data-ttu-id="e5080-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e5080-105">ByFactoryName (Default)</span></span>
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5080-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e5080-106">ByFactoryObject</span></span>
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5080-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5080-107">DESCRIPTION</span></span>
<span data-ttu-id="e5080-108">O cmdlet **Save-AzDataFactoryLog** baixa os arquivos de log associados ao processamento do Azure HDInsight de projetos porco ou Hive ou para atividades personalizadas em seu disco rígido local.</span><span class="sxs-lookup"><span data-stu-id="e5080-108">The **Save-AzDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="e5080-109">Primeiro, você executa o cmdlet Get-AzDataFactoryRun para obter uma ID de uma atividade executada para uma fatia de dados e, em seguida, usa essa ID para recuperar arquivos de log do armazenamento de objeto binário grande (BLOB) associado ao cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e5080-109">You first run the Get-AzDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="e5080-110">Se você não especificar o parâmetro *DownloadLogs* , o cmdlet retornará apenas o local dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="e5080-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="e5080-111">Se você especificar *DownloadLogs* sem especificar um diretório de saída (parâmetro de *saída* ), os arquivos de log serão baixados para a pasta documentos padrão.</span><span class="sxs-lookup"><span data-stu-id="e5080-111">If you specify *DownloadLogs* without specifying an output directory ( *Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="e5080-112">Se você especificar *DownloadLogs* junto com uma pasta de saída ( *saída* ), os arquivos de log serão baixados para a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="e5080-112">If you specify *DownloadLogs* along with an output folder ( *Output* ), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="e5080-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5080-113">EXAMPLES</span></span>

### <span data-ttu-id="e5080-114">Exemplo 1: salvar arquivos de log em uma pasta específica</span><span class="sxs-lookup"><span data-stu-id="e5080-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="e5080-115">Esse comando salva os arquivos de log para a atividade executar com a ID de 841b77c9-d56c-48d1-99a3-8c16c3e77d39 em que a atividade pertence a um pipeline na fábrica de dados chamado LogProcessingFactory no grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="e5080-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="e5080-116">Os arquivos de log são salvos na pasta C:\Test.</span><span class="sxs-lookup"><span data-stu-id="e5080-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="e5080-117">Exemplo 2: salvar arquivos de log na pasta documentos padrão</span><span class="sxs-lookup"><span data-stu-id="e5080-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="e5080-118">Esse comando salva arquivos de log na pasta documentos (padrão).</span><span class="sxs-lookup"><span data-stu-id="e5080-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="e5080-119">Exemplo 3: obter o local dos arquivos de log</span><span class="sxs-lookup"><span data-stu-id="e5080-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="e5080-120">Esse comando retorna o local dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="e5080-120">This command returns the location of log files.</span></span>
<span data-ttu-id="e5080-121">Observe que *DownloadLogs* não está especificado.</span><span class="sxs-lookup"><span data-stu-id="e5080-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="e5080-122">OS</span><span class="sxs-lookup"><span data-stu-id="e5080-122">PARAMETERS</span></span>

### <span data-ttu-id="e5080-123">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="e5080-123">-DataFactory</span></span>
<span data-ttu-id="e5080-124">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="e5080-124">Specifies a **PSDataFactory** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5080-125">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e5080-125">-DataFactoryName</span></span>
<span data-ttu-id="e5080-126">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e5080-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e5080-127">Esse cmdlet baixa arquivos de log para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e5080-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5080-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5080-128">-DefaultProfile</span></span>
<span data-ttu-id="e5080-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e5080-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5080-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="e5080-130">-DownloadLogs</span></span>
<span data-ttu-id="e5080-131">Indica que esse cmdlet baixa os arquivos de log para seu computador local.</span><span class="sxs-lookup"><span data-stu-id="e5080-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="e5080-132">Se a pasta de *saída* não for especificada, os arquivos serão salvos na pasta documentos em uma subpasta.</span><span class="sxs-lookup"><span data-stu-id="e5080-132">If *Output* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="e5080-133">-ID</span><span class="sxs-lookup"><span data-stu-id="e5080-133">-Id</span></span>
<span data-ttu-id="e5080-134">Especifica a ID da atividade executada para a fatia de dados.</span><span class="sxs-lookup"><span data-stu-id="e5080-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="e5080-135">Use o cmdlet Get-AzDataFactoryRun para obter uma ID.</span><span class="sxs-lookup"><span data-stu-id="e5080-135">Use the Get-AzDataFactoryRun cmdlet to get an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5080-136">-Saída</span><span class="sxs-lookup"><span data-stu-id="e5080-136">-Output</span></span>
<span data-ttu-id="e5080-137">Especifica a pasta de saída na qual os arquivos de log baixados são salvos.</span><span class="sxs-lookup"><span data-stu-id="e5080-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

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

### <span data-ttu-id="e5080-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5080-138">-ResourceGroupName</span></span>
<span data-ttu-id="e5080-139">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5080-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e5080-140">Esse cmdlet cria uma fábrica de dados que pertence ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e5080-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5080-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5080-141">CommonParameters</span></span>
<span data-ttu-id="e5080-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5080-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5080-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5080-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5080-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5080-144">INPUTS</span></span>

### <span data-ttu-id="e5080-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e5080-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="e5080-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e5080-146">System.String</span></span>

## <span data-ttu-id="e5080-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5080-147">OUTPUTS</span></span>

### <span data-ttu-id="e5080-148">Microsoft. Azure. Commands. datafactorings. Models. PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="e5080-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="e5080-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5080-149">NOTES</span></span>
* <span data-ttu-id="e5080-150">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="e5080-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e5080-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5080-151">RELATED LINKS</span></span>

[<span data-ttu-id="e5080-152">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="e5080-152">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="e5080-153">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e5080-153">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="e5080-154">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e5080-154">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="e5080-155">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e5080-155">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="e5080-156">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="e5080-156">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="e5080-157">Suspender-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e5080-157">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


