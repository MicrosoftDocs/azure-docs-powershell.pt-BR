---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 35acbbaeb4983def89711049fc3284a63611bbec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888296"
---
# <span data-ttu-id="67945-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="67945-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="67945-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67945-102">SYNOPSIS</span></span>
<span data-ttu-id="67945-103">Obter todas as sessões de depuração de fluxo de dados ativos pelo Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="67945-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="67945-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="67945-104">SYNTAX</span></span>

### <span data-ttu-id="67945-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="67945-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67945-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="67945-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67945-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="67945-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67945-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="67945-108">DESCRIPTION</span></span>
<span data-ttu-id="67945-109">Listar todas as sessões de depuração de fluxo de dados ativos pelo Azure Data Factory com detalhes.</span><span class="sxs-lookup"><span data-stu-id="67945-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="67945-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67945-110">EXAMPLES</span></span>

### <span data-ttu-id="67945-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="67945-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="67945-112">Obter todas as sessões de depuração de fluxo de dados ativos no Azure Data Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="67945-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="67945-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="67945-113">PARAMETERS</span></span>

### <span data-ttu-id="67945-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="67945-114">-DataFactory</span></span>
<span data-ttu-id="67945-115">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="67945-115">The data factory object.</span></span>

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

### <span data-ttu-id="67945-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="67945-116">-DataFactoryName</span></span>
<span data-ttu-id="67945-117">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="67945-117">The data factory name.</span></span>

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

### <span data-ttu-id="67945-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67945-118">-DefaultProfile</span></span>
<span data-ttu-id="67945-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67945-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67945-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67945-120">-ResourceGroupName</span></span>
<span data-ttu-id="67945-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="67945-121">The resource group name.</span></span>

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

### <span data-ttu-id="67945-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67945-122">-ResourceId</span></span>
<span data-ttu-id="67945-123">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="67945-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="67945-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67945-124">CommonParameters</span></span>
<span data-ttu-id="67945-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67945-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67945-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67945-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67945-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67945-127">INPUTS</span></span>

### <span data-ttu-id="67945-128">System.String</span><span class="sxs-lookup"><span data-stu-id="67945-128">System.String</span></span>

### <span data-ttu-id="67945-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="67945-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="67945-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="67945-130">OUTPUTS</span></span>

### <span data-ttu-id="67945-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span><span class="sxs-lookup"><span data-stu-id="67945-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="67945-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="67945-132">NOTES</span></span>
<span data-ttu-id="67945-133">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="67945-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="67945-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67945-134">RELATED LINKS</span></span>

[<span data-ttu-id="67945-135">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="67945-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="67945-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="67945-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="67945-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="67945-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="67945-138">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="67945-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)