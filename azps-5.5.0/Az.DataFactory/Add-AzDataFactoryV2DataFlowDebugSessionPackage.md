---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2dataflowdebugsessionpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
ms.openlocfilehash: c319ee7fba1bddff8e93e56601c623658094253d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117756"
---
# <span data-ttu-id="749a3-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="749a3-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>

## <span data-ttu-id="749a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="749a3-102">SYNOPSIS</span></span>
<span data-ttu-id="749a3-103">Adicione o recurso de fluxo de dados e suas dependências a uma sessão de depuração de fluxo de dados específica.</span><span class="sxs-lookup"><span data-stu-id="749a3-103">Add data flow resource and its dependencies into specific data flow debug session.</span></span>

## <span data-ttu-id="749a3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="749a3-104">SYNTAX</span></span>

### <span data-ttu-id="749a3-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="749a3-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="749a3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="749a3-106">ByFactoryObject</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="749a3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="749a3-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="749a3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="749a3-108">DESCRIPTION</span></span>
<span data-ttu-id="749a3-109">Este comando anexa o recurso de fluxo de dados e suas dependências à sessão de depuração específica A sequência de comandos do PowerShell para fluxo de trabalho de depuração de fluxo de dados deve ser:</span><span class="sxs-lookup"><span data-stu-id="749a3-109">This command attaches data flow resource and its dependencies to the specific debug session The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="749a3-110">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="749a3-110">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="749a3-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="749a3-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="749a3-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repita esta etapa para diferentes comandos/destinos ou repita a etapa 2 a 3 para alterar o arquivo de pacote)</span><span class="sxs-lookup"><span data-stu-id="749a3-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="749a3-113">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="749a3-113">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="749a3-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="749a3-114">EXAMPLES</span></span>

### <span data-ttu-id="749a3-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="749a3-115">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Add-AzDataFactoryV2DataFlowDebugSessionPackage -ResourceGroupName adf -DataFactoryName WikiADF -PackageFile "D:\dataflowps\addpackage.json" -SessionId 550effe4-93a3-485c-8525-eaf25259efbd
```

<span data-ttu-id="749a3-116">Adicione o pacote de fluxo de dados à sessão de depuração "550effe4-93a3-485c-8525-eaf25259efbd" da fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="749a3-116">Add data flow package into debug session "550effe4-93a3-485c-8525-eaf25259efbd" of "WikiADF" data factory.</span></span>
<span data-ttu-id="749a3-117">O arquivo Pakcage contém o recurso de depuração de fluxo de dados, lista de resouce de depuração de conjuntos de dados, lista de recurso de depuração de serviço vinculado, configuração de depuração e ID de sessão.</span><span class="sxs-lookup"><span data-stu-id="749a3-117">Pakcage file contains data flow debug resource, list of dataset debug resouce, list of linked service debug resource, debug setting and session ID.</span></span> <span data-ttu-id="749a3-118">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="749a3-118">For instance:</span></span>

<span data-ttu-id="749a3-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": " \\ ", "firstRowAsHeader": true, "quoteChar": " \" " }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https; AccountName=name; AccountKey=key; EndpointSuffix=core.windows.net" } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span><span class="sxs-lookup"><span data-stu-id="749a3-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": "\\", "firstRowAsHeader": true, "quoteChar": "\"" }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https;AccountName=name;AccountKey=key;EndpointSuffix=core.windows.net" } } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span></span>

<span data-ttu-id="749a3-120">O parâmetro SessionID é usado para substituir a propriedade sessionId existente no arquivo de pacote.</span><span class="sxs-lookup"><span data-stu-id="749a3-120">SessionID parameter is used to replace the existing sessionId property in the package file.</span></span>

## <span data-ttu-id="749a3-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="749a3-121">PARAMETERS</span></span>

### <span data-ttu-id="749a3-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="749a3-122">-DataFactory</span></span>
<span data-ttu-id="749a3-123">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="749a3-123">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="749a3-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="749a3-124">-DataFactoryName</span></span>
<span data-ttu-id="749a3-125">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="749a3-125">The data factory name.</span></span>

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

### <span data-ttu-id="749a3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="749a3-126">-DefaultProfile</span></span>
<span data-ttu-id="749a3-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="749a3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="749a3-128">-PackageFile</span><span class="sxs-lookup"><span data-stu-id="749a3-128">-PackageFile</span></span>
<span data-ttu-id="749a3-129">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="749a3-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="749a3-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="749a3-130">-PassThru</span></span>
<span data-ttu-id="749a3-131">Se especificado, a gravação será verdadeira caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="749a3-131">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="749a3-132">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="749a3-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="749a3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="749a3-133">-ResourceGroupName</span></span>
<span data-ttu-id="749a3-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="749a3-134">The resource group name.</span></span>

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

### <span data-ttu-id="749a3-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="749a3-135">-ResourceId</span></span>
<span data-ttu-id="749a3-136">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="749a3-136">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="749a3-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="749a3-137">-Confirm</span></span>
<span data-ttu-id="749a3-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="749a3-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="749a3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="749a3-139">-WhatIf</span></span>
<span data-ttu-id="749a3-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="749a3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="749a3-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="749a3-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="749a3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="749a3-142">CommonParameters</span></span>
<span data-ttu-id="749a3-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="749a3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="749a3-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="749a3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="749a3-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="749a3-145">INPUTS</span></span>

### <span data-ttu-id="749a3-146">System.String</span><span class="sxs-lookup"><span data-stu-id="749a3-146">System.String</span></span>

### <span data-ttu-id="749a3-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="749a3-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="749a3-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="749a3-148">OUTPUTS</span></span>

### <span data-ttu-id="749a3-149">System.Void</span><span class="sxs-lookup"><span data-stu-id="749a3-149">System.Void</span></span>

### <span data-ttu-id="749a3-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="749a3-150">System.Boolean</span></span>

## <span data-ttu-id="749a3-151">Notas</span><span class="sxs-lookup"><span data-stu-id="749a3-151">NOTES</span></span>
<span data-ttu-id="749a3-152">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="749a3-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="749a3-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="749a3-153">RELATED LINKS</span></span>

[<span data-ttu-id="749a3-154">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="749a3-154">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="749a3-155">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="749a3-155">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="749a3-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="749a3-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="749a3-157">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="749a3-157">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
