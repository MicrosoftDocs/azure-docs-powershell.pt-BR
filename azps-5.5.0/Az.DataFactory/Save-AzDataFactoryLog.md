---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: cf1e0738a01d2b8f3219f2732995182fe7f6959d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111006"
---
# <span data-ttu-id="fbbaa-101">Save-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="fbbaa-101">Save-AzDataFactoryLog</span></span>

## <span data-ttu-id="fbbaa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fbbaa-102">SYNOPSIS</span></span>
<span data-ttu-id="fbbaa-103">Baixa arquivos de log do processamento HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-103">Downloads log files from Azure HDInsight processing.</span></span>

## <span data-ttu-id="fbbaa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbbaa-104">SYNTAX</span></span>

### <span data-ttu-id="fbbaa-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="fbbaa-105">ByFactoryName (Default)</span></span>
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbbaa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fbbaa-106">ByFactoryObject</span></span>
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbbaa-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fbbaa-107">DESCRIPTION</span></span>
<span data-ttu-id="fbbaa-108">O cmdlet **Save-AzDataFactoryLog** baixa arquivos de log associados ao processamento do Azure HDInsight de projetos de Porão ou Colagem ou para atividades personalizadas no disco rígido local.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-108">The **Save-AzDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="fbbaa-109">Primeiro, execute o cmdlet Get-AzDataFactoryRun para obter uma ID de uma atividade em uma fatia de dados e use essa ID para recuperar arquivos de log do armazenamento de objeto binário grande (BLOB) associado ao cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-109">You first run the Get-AzDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="fbbaa-110">Se você não especificar o parâmetro *DownloadLogs,* o cmdlet retornará apenas o local dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="fbbaa-111">Se você especificar *DownloadLogs* sem especificar um diretório de saída *(* parâmetro saída), os arquivos de log serão baixados para a pasta Documentos padrão.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-111">If you specify *DownloadLogs* without specifying an output directory (*Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="fbbaa-112">Se você especificar *DownloadLogs* juntamente com uma pasta de saída (*Saída),* os arquivos de log serão baixados para a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-112">If you specify *DownloadLogs* along with an output folder (*Output*), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="fbbaa-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fbbaa-113">EXAMPLES</span></span>

### <span data-ttu-id="fbbaa-114">Exemplo 1: Salvar arquivos de log em uma pasta específica</span><span class="sxs-lookup"><span data-stu-id="fbbaa-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="fbbaa-115">Esse comando salva arquivos de log para a atividade executado com a ID de 841b77c9-d56c-48d1-99a3-8c16c3e77d39 onde a atividade pertence a um pipeline no fábrica de dados chamado LogProcessingFactory no grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="fbbaa-116">Os arquivos de log são salvos na pasta C:\Teste.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="fbbaa-117">Exemplo 2: Salvar arquivos de log na pasta Documentos padrão</span><span class="sxs-lookup"><span data-stu-id="fbbaa-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="fbbaa-118">Esse comando salva arquivos de log na pasta Documentos (padrão).</span><span class="sxs-lookup"><span data-stu-id="fbbaa-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="fbbaa-119">Exemplo 3: Obter o local dos arquivos de log</span><span class="sxs-lookup"><span data-stu-id="fbbaa-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="fbbaa-120">Esse comando retorna o local dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-120">This command returns the location of log files.</span></span>
<span data-ttu-id="fbbaa-121">Observe que *DownloadLogs* não está especificado.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="fbbaa-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbbaa-122">PARAMETERS</span></span>

### <span data-ttu-id="fbbaa-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fbbaa-123">-DataFactory</span></span>
<span data-ttu-id="fbbaa-124">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="fbbaa-124">Specifies a **PSDataFactory** object.</span></span>

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

### <span data-ttu-id="fbbaa-125">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fbbaa-125">-DataFactoryName</span></span>
<span data-ttu-id="fbbaa-126">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fbbaa-127">Este cmdlet baixa arquivos de log para o fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fbbaa-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbbaa-128">-DefaultProfile</span></span>
<span data-ttu-id="fbbaa-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="fbbaa-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbbaa-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="fbbaa-130">-DownloadLogs</span></span>
<span data-ttu-id="fbbaa-131">Indica que esse cmdlet baixa arquivos de log para seu computador local.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="fbbaa-132">Se *a pasta* Saída não for especificada, os arquivos serão salvos na pasta Documentos em uma subpasta.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-132">If *Output* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="fbbaa-133">-ID</span><span class="sxs-lookup"><span data-stu-id="fbbaa-133">-Id</span></span>
<span data-ttu-id="fbbaa-134">Especifica a ID da atividade executado para a fatia de dados.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="fbbaa-135">Use o Get-AzDataFactoryRun cmdlet para obter uma ID.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-135">Use the Get-AzDataFactoryRun cmdlet to get an ID.</span></span>

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

### <span data-ttu-id="fbbaa-136">-Saída</span><span class="sxs-lookup"><span data-stu-id="fbbaa-136">-Output</span></span>
<span data-ttu-id="fbbaa-137">Especifica a pasta de saída na qual os arquivos de log baixados são salvos.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

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

### <span data-ttu-id="fbbaa-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbbaa-138">-ResourceGroupName</span></span>
<span data-ttu-id="fbbaa-139">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fbbaa-140">Esse cmdlet cria uma fábrica de dados que pertence ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fbbaa-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbbaa-141">CommonParameters</span></span>
<span data-ttu-id="fbbaa-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbbaa-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbbaa-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbbaa-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbbaa-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="fbbaa-144">INPUTS</span></span>

### <span data-ttu-id="fbbaa-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fbbaa-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="fbbaa-146">System.String</span><span class="sxs-lookup"><span data-stu-id="fbbaa-146">System.String</span></span>

## <span data-ttu-id="fbbaa-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="fbbaa-147">OUTPUTS</span></span>

### <span data-ttu-id="fbbaa-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="fbbaa-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="fbbaa-149">Notas</span><span class="sxs-lookup"><span data-stu-id="fbbaa-149">NOTES</span></span>
* <span data-ttu-id="fbbaa-150">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="fbbaa-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fbbaa-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fbbaa-151">RELATED LINKS</span></span>

[<span data-ttu-id="fbbaa-152">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="fbbaa-152">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="fbbaa-153">Get-AzDataFactoryFactline</span><span class="sxs-lookup"><span data-stu-id="fbbaa-153">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="fbbaa-154">New-AzDataFactoryFactline</span><span class="sxs-lookup"><span data-stu-id="fbbaa-154">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="fbbaa-155">Remove-AzDataFactoryDataDataLine</span><span class="sxs-lookup"><span data-stu-id="fbbaa-155">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="fbbaa-156">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="fbbaa-156">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="fbbaa-157">Suspend-AzDataFactoryFactline</span><span class="sxs-lookup"><span data-stu-id="fbbaa-157">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


