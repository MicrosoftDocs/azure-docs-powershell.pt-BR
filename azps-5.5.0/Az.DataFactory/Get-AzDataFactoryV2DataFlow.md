---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: b4af5eae61e47d8617eb270451f406f349162f50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116438"
---
# <span data-ttu-id="42162-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="42162-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="42162-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42162-102">SYNOPSIS</span></span>
<span data-ttu-id="42162-103">Obtém informações sobre fluxos de dados no Data Factory.</span><span class="sxs-lookup"><span data-stu-id="42162-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="42162-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42162-104">SYNTAX</span></span>

### <span data-ttu-id="42162-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="42162-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42162-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="42162-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42162-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="42162-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42162-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="42162-108">DESCRIPTION</span></span>
<span data-ttu-id="42162-109">O Get-AzDataFactoryV2DataFlow cmdlet obtém informações sobre fluxos de dados no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="42162-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="42162-110">Se você especificar o nome de um fluxo de dados, esse cmdlet obterá informações sobre esse fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="42162-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="42162-111">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os fluxos de dados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="42162-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="42162-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="42162-112">EXAMPLES</span></span>
### <span data-ttu-id="42162-113">Exemplo 1: Obter informações sobre todos os fluxos de dados</span><span class="sxs-lookup"><span data-stu-id="42162-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="42162-114">Este comando obtém informações sobre todos os fluxos de dados na fábrica de dados chamada WikiADF.</span><span class="sxs-lookup"><span data-stu-id="42162-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="42162-115">Exemplo 2: Obter informações sobre um fluxo de dados específico</span><span class="sxs-lookup"><span data-stu-id="42162-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="42162-116">Esse comando obtém informações sobre o fluxo de dados chamado dataflow1 na fábrica de dados chamada WikiADF.</span><span class="sxs-lookup"><span data-stu-id="42162-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="42162-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42162-117">PARAMETERS</span></span>

### <span data-ttu-id="42162-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="42162-118">-DataFactory</span></span>
<span data-ttu-id="42162-119">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="42162-119">The data factory object.</span></span>

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

### <span data-ttu-id="42162-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="42162-120">-DataFactoryName</span></span>
<span data-ttu-id="42162-121">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="42162-121">The data factory name.</span></span>

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

### <span data-ttu-id="42162-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42162-122">-DefaultProfile</span></span>
<span data-ttu-id="42162-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="42162-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42162-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="42162-124">-Name</span></span>
<span data-ttu-id="42162-125">O nome do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="42162-125">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DataFlowName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42162-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42162-126">-ResourceGroupName</span></span>
<span data-ttu-id="42162-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="42162-127">The resource group name.</span></span>

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

### <span data-ttu-id="42162-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42162-128">-ResourceId</span></span>
<span data-ttu-id="42162-129">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="42162-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="42162-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42162-130">CommonParameters</span></span>
<span data-ttu-id="42162-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42162-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42162-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42162-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42162-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="42162-133">INPUTS</span></span>

### <span data-ttu-id="42162-134">System.String</span><span class="sxs-lookup"><span data-stu-id="42162-134">System.String</span></span>

### <span data-ttu-id="42162-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="42162-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="42162-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="42162-136">OUTPUTS</span></span>

### <span data-ttu-id="42162-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="42162-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="42162-138">Notas</span><span class="sxs-lookup"><span data-stu-id="42162-138">NOTES</span></span>
<span data-ttu-id="42162-139">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="42162-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="42162-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42162-140">RELATED LINKS</span></span>

[<span data-ttu-id="42162-141">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="42162-141">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

[<span data-ttu-id="42162-142">Remove-AzDataDataDataFlow</span><span class="sxs-lookup"><span data-stu-id="42162-142">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)