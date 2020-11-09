---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 951f1b6a03c621e0dd8bc5d559eaf317cfd43a2c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281062"
---
# <span data-ttu-id="1b93a-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1b93a-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="1b93a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b93a-102">SYNOPSIS</span></span>
<span data-ttu-id="1b93a-103">Obter todas as sessões de depuração do fluxo de dados ativos pelo Azure data Factory</span><span class="sxs-lookup"><span data-stu-id="1b93a-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="1b93a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b93a-104">SYNTAX</span></span>

### <span data-ttu-id="1b93a-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1b93a-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b93a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1b93a-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b93a-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1b93a-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b93a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b93a-108">DESCRIPTION</span></span>
<span data-ttu-id="1b93a-109">Liste todas as sessões de depuração de fluxo de dados ativos pelo Azure data Factory com detalhes.</span><span class="sxs-lookup"><span data-stu-id="1b93a-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="1b93a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b93a-110">EXAMPLES</span></span>

### <span data-ttu-id="1b93a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1b93a-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="1b93a-112">Obter todas as sessões de depuração de fluxo de dados ativas no Azure data Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="1b93a-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="1b93a-113">OS</span><span class="sxs-lookup"><span data-stu-id="1b93a-113">PARAMETERS</span></span>

### <span data-ttu-id="1b93a-114">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="1b93a-114">-DataFactory</span></span>
<span data-ttu-id="1b93a-115">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="1b93a-115">The data factory object.</span></span>

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

### <span data-ttu-id="1b93a-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1b93a-116">-DataFactoryName</span></span>
<span data-ttu-id="1b93a-117">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="1b93a-117">The data factory name.</span></span>

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

### <span data-ttu-id="1b93a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b93a-118">-DefaultProfile</span></span>
<span data-ttu-id="1b93a-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b93a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b93a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b93a-120">-ResourceGroupName</span></span>
<span data-ttu-id="1b93a-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1b93a-121">The resource group name.</span></span>

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

### <span data-ttu-id="1b93a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b93a-122">-ResourceId</span></span>
<span data-ttu-id="1b93a-123">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b93a-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1b93a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b93a-124">CommonParameters</span></span>
<span data-ttu-id="1b93a-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b93a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b93a-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b93a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b93a-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b93a-127">INPUTS</span></span>

### <span data-ttu-id="1b93a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1b93a-128">System.String</span></span>

### <span data-ttu-id="1b93a-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1b93a-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="1b93a-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b93a-130">OUTPUTS</span></span>

### <span data-ttu-id="1b93a-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span><span class="sxs-lookup"><span data-stu-id="1b93a-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="1b93a-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b93a-132">NOTES</span></span>
<span data-ttu-id="1b93a-133">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="1b93a-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1b93a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b93a-134">RELATED LINKS</span></span>

[<span data-ttu-id="1b93a-135">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1b93a-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="1b93a-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="1b93a-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="1b93a-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="1b93a-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="1b93a-138">Parar-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1b93a-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)