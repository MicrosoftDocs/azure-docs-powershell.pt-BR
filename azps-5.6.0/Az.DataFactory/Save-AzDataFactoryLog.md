---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: eb2e3c9acd93e8b20c7bdf6f4ee04ef2910a3cbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892523"
---
# <span data-ttu-id="b2d11-101">Save-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="b2d11-101">Save-AzDataFactoryLog</span></span>

## <span data-ttu-id="b2d11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2d11-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d11-103">Baixa arquivos de log do processamento HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="b2d11-103">Downloads log files from Azure HDInsight processing.</span></span>

## <span data-ttu-id="b2d11-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b2d11-104">SYNTAX</span></span>

### <span data-ttu-id="b2d11-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b2d11-105">ByFactoryName (Default)</span></span>
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2d11-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b2d11-106">ByFactoryObject</span></span>
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2d11-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b2d11-107">DESCRIPTION</span></span>
<span data-ttu-id="b2d11-108">O cmdlet **Save-AzDataFactoryLog** baixa arquivos de log associados ao processamento HDInsight do Azure de projetos De Porquinho ou Hive ou para atividades personalizadas no disco rígido local.</span><span class="sxs-lookup"><span data-stu-id="b2d11-108">The **Save-AzDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="b2d11-109">Primeiro, execute o cmdlet Get-AzDataFactoryRun para obter uma ID de uma atividade em uma fatia de dados e, em seguida, use essa ID para recuperar arquivos de log do armazenamento blob (objeto grande binário) associado ao cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b2d11-109">You first run the Get-AzDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="b2d11-110">Se você não especificar o parâmetro *DownloadLogs,* o cmdlet retornará apenas o local dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="b2d11-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="b2d11-111">Se você especificar *DownloadLogs* sem especificar um diretório de saída (*parâmetro Output),* os arquivos de log serão baixados para a pasta Documentos padrão.</span><span class="sxs-lookup"><span data-stu-id="b2d11-111">If you specify *DownloadLogs* without specifying an output directory (*Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="b2d11-112">Se você especificar *DownloadLogs* juntamente com uma pasta de saída (*Saída*), os arquivos de log serão baixados para a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="b2d11-112">If you specify *DownloadLogs* along with an output folder (*Output*), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="b2d11-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2d11-113">EXAMPLES</span></span>

### <span data-ttu-id="b2d11-114">Exemplo 1: Salvar arquivos de log em uma pasta específica</span><span class="sxs-lookup"><span data-stu-id="b2d11-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="b2d11-115">Este comando salva arquivos de log para a atividade executado com a ID de 841b77c9-d56c-48d1-99a3-8c16c3e777d39 onde a atividade pertence a um pipeline no fábrica de dados chamado LogProcessingFactory no grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="b2d11-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="b2d11-116">Os arquivos de log são salvos na pasta C:\Test.</span><span class="sxs-lookup"><span data-stu-id="b2d11-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="b2d11-117">Exemplo 2: Salvar arquivos de log na pasta Documentos padrão</span><span class="sxs-lookup"><span data-stu-id="b2d11-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="b2d11-118">Este comando salva arquivos de log na pasta Documentos (padrão).</span><span class="sxs-lookup"><span data-stu-id="b2d11-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="b2d11-119">Exemplo 3: Obter o local dos arquivos de log</span><span class="sxs-lookup"><span data-stu-id="b2d11-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="b2d11-120">Este comando retorna o local dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="b2d11-120">This command returns the location of log files.</span></span>
<span data-ttu-id="b2d11-121">Observe que *DownloadLogs* não é especificado.</span><span class="sxs-lookup"><span data-stu-id="b2d11-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="b2d11-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b2d11-122">PARAMETERS</span></span>

### <span data-ttu-id="b2d11-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b2d11-123">-DataFactory</span></span>
<span data-ttu-id="b2d11-124">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="b2d11-124">Specifies a **PSDataFactory** object.</span></span>

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

### <span data-ttu-id="b2d11-125">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b2d11-125">-DataFactoryName</span></span>
<span data-ttu-id="b2d11-126">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b2d11-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b2d11-127">Este cmdlet baixa arquivos de log para o fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b2d11-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b2d11-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d11-128">-DefaultProfile</span></span>
<span data-ttu-id="b2d11-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b2d11-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2d11-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="b2d11-130">-DownloadLogs</span></span>
<span data-ttu-id="b2d11-131">Indica que esse cmdlet baixa arquivos de log no computador local.</span><span class="sxs-lookup"><span data-stu-id="b2d11-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="b2d11-132">Se *a pasta* Saída não for especificada, os arquivos serão salvos na pasta Documentos em uma subpasta.</span><span class="sxs-lookup"><span data-stu-id="b2d11-132">If *Output* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="b2d11-133">-Id</span><span class="sxs-lookup"><span data-stu-id="b2d11-133">-Id</span></span>
<span data-ttu-id="b2d11-134">Especifica a ID da atividade executado para a fatia de dados.</span><span class="sxs-lookup"><span data-stu-id="b2d11-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="b2d11-135">Use o cmdlet Get-AzDataFactoryRun para obter uma ID.</span><span class="sxs-lookup"><span data-stu-id="b2d11-135">Use the Get-AzDataFactoryRun cmdlet to get an ID.</span></span>

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

### <span data-ttu-id="b2d11-136">-Output</span><span class="sxs-lookup"><span data-stu-id="b2d11-136">-Output</span></span>
<span data-ttu-id="b2d11-137">Especifica a pasta de saída na qual os arquivos de log baixados são salvos.</span><span class="sxs-lookup"><span data-stu-id="b2d11-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

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

### <span data-ttu-id="b2d11-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2d11-138">-ResourceGroupName</span></span>
<span data-ttu-id="b2d11-139">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b2d11-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b2d11-140">Este cmdlet cria um fábrica de dados que pertence ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b2d11-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b2d11-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d11-141">CommonParameters</span></span>
<span data-ttu-id="b2d11-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2d11-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d11-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2d11-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d11-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2d11-144">INPUTS</span></span>

### <span data-ttu-id="b2d11-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b2d11-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="b2d11-146">System.String</span><span class="sxs-lookup"><span data-stu-id="b2d11-146">System.String</span></span>

## <span data-ttu-id="b2d11-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b2d11-147">OUTPUTS</span></span>

### <span data-ttu-id="b2d11-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="b2d11-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="b2d11-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="b2d11-149">NOTES</span></span>
* <span data-ttu-id="b2d11-150">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="b2d11-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b2d11-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2d11-151">RELATED LINKS</span></span>

[<span data-ttu-id="b2d11-152">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="b2d11-152">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="b2d11-153">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b2d11-153">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="b2d11-154">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b2d11-154">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="b2d11-155">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b2d11-155">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="b2d11-156">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="b2d11-156">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="b2d11-157">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b2d11-157">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


