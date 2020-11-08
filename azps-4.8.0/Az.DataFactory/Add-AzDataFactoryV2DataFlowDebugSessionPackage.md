---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2dataflowdebugsessionpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
ms.openlocfilehash: c319ee7fba1bddff8e93e56601c623658094253d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94115051"
---
# <span data-ttu-id="3e87c-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="3e87c-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>

## <span data-ttu-id="3e87c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e87c-102">SYNOPSIS</span></span>
<span data-ttu-id="3e87c-103">Adicione o recurso de fluxo de dados e suas dependências a uma sessão de depuração de fluxo de dados específica.</span><span class="sxs-lookup"><span data-stu-id="3e87c-103">Add data flow resource and its dependencies into specific data flow debug session.</span></span>

## <span data-ttu-id="3e87c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e87c-104">SYNTAX</span></span>

### <span data-ttu-id="3e87c-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="3e87c-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e87c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3e87c-106">ByFactoryObject</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e87c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3e87c-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e87c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e87c-108">DESCRIPTION</span></span>
<span data-ttu-id="3e87c-109">Esse comando anexa o recurso de fluxo de dados e suas dependências à sessão de depuração específica a sequência de comandos do PowerShell para o fluxo de trabalho de depuração do fluxo de dados deve ser:</span><span class="sxs-lookup"><span data-stu-id="3e87c-109">This command attaches data flow resource and its dependencies to the specific debug session The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="3e87c-110">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="3e87c-110">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="3e87c-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="3e87c-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="3e87c-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repita esta etapa para diferentes comandos/destinos ou repita a etapa 2-3 para alterar o arquivo de pacote)</span><span class="sxs-lookup"><span data-stu-id="3e87c-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="3e87c-113">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="3e87c-113">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="3e87c-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e87c-114">EXAMPLES</span></span>

### <span data-ttu-id="3e87c-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3e87c-115">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Add-AzDataFactoryV2DataFlowDebugSessionPackage -ResourceGroupName adf -DataFactoryName WikiADF -PackageFile "D:\dataflowps\addpackage.json" -SessionId 550effe4-93a3-485c-8525-eaf25259efbd
```

<span data-ttu-id="3e87c-116">Adicionar pacote de fluxo de dados à sessão de depuração "550effe4-93a3-485c-8525-eaf25259efbd" da fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="3e87c-116">Add data flow package into debug session "550effe4-93a3-485c-8525-eaf25259efbd" of "WikiADF" data factory.</span></span>
<span data-ttu-id="3e87c-117">Pakcage arquivo contém o recurso de depuração do fluxo de dados, lista de recursos de depuração do conjunto de dados, lista de recursos de depuração do serviço vinculado, configuração de depuração e ID da sessão.</span><span class="sxs-lookup"><span data-stu-id="3e87c-117">Pakcage file contains data flow debug resource, list of dataset debug resouce, list of linked service debug resource, debug setting and session ID.</span></span> <span data-ttu-id="3e87c-118">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="3e87c-118">For instance:</span></span>

<span data-ttu-id="3e87c-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": " \\ ", "firstRowAsHeader": true, "quoteChar": " \" " }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https; AccountName = nome; AccountKey = tecla; EndpointSuffix = Core. Windows. net "}}]," debugSettings ": {" sourceSettings ": [{" sourceName ":" source1 "," translimit ": 1000}]}," Identificação_da_sessão ":" 4f988caf-e765-47d2-82cd-430334a6b135 "</span><span class="sxs-lookup"><span data-stu-id="3e87c-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": "\\", "firstRowAsHeader": true, "quoteChar": "\"" }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https;AccountName=name;AccountKey=key;EndpointSuffix=core.windows.net" } } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span></span>

<span data-ttu-id="3e87c-120">O parâmetro SessionID é usado para substituir a propriedade sessionId existente no arquivo do pacote.</span><span class="sxs-lookup"><span data-stu-id="3e87c-120">SessionID parameter is used to replace the existing sessionId property in the package file.</span></span>

## <span data-ttu-id="3e87c-121">OS</span><span class="sxs-lookup"><span data-stu-id="3e87c-121">PARAMETERS</span></span>

### <span data-ttu-id="3e87c-122">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="3e87c-122">-DataFactory</span></span>
<span data-ttu-id="3e87c-123">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="3e87c-123">The data factory object.</span></span>

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

### <span data-ttu-id="3e87c-124">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3e87c-124">-DataFactoryName</span></span>
<span data-ttu-id="3e87c-125">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="3e87c-125">The data factory name.</span></span>

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

### <span data-ttu-id="3e87c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e87c-126">-DefaultProfile</span></span>
<span data-ttu-id="3e87c-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e87c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e87c-128">-PackageFile</span><span class="sxs-lookup"><span data-stu-id="3e87c-128">-PackageFile</span></span>
<span data-ttu-id="3e87c-129">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="3e87c-129">The JSON file path.</span></span>

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

### <span data-ttu-id="3e87c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e87c-130">-PassThru</span></span>
<span data-ttu-id="3e87c-131">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3e87c-131">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="3e87c-132">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="3e87c-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="3e87c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e87c-133">-ResourceGroupName</span></span>
<span data-ttu-id="3e87c-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3e87c-134">The resource group name.</span></span>

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

### <span data-ttu-id="3e87c-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e87c-135">-ResourceId</span></span>
<span data-ttu-id="3e87c-136">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e87c-136">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3e87c-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3e87c-137">-Confirm</span></span>
<span data-ttu-id="3e87c-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e87c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e87c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e87c-139">-WhatIf</span></span>
<span data-ttu-id="3e87c-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3e87c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e87c-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e87c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e87c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e87c-142">CommonParameters</span></span>
<span data-ttu-id="3e87c-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e87c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e87c-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e87c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e87c-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e87c-145">INPUTS</span></span>

### <span data-ttu-id="3e87c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3e87c-146">System.String</span></span>

### <span data-ttu-id="3e87c-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3e87c-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="3e87c-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e87c-148">OUTPUTS</span></span>

### <span data-ttu-id="3e87c-149">System. void</span><span class="sxs-lookup"><span data-stu-id="3e87c-149">System.Void</span></span>

### <span data-ttu-id="3e87c-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3e87c-150">System.Boolean</span></span>

## <span data-ttu-id="3e87c-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e87c-151">NOTES</span></span>
<span data-ttu-id="3e87c-152">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="3e87c-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3e87c-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e87c-153">RELATED LINKS</span></span>

[<span data-ttu-id="3e87c-154">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="3e87c-154">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="3e87c-155">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="3e87c-155">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="3e87c-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="3e87c-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="3e87c-157">Parar-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="3e87c-157">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
