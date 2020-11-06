---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: ad27587e52533af1ef7989d4b52de3319137640d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597071"
---
# <span data-ttu-id="5d54e-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="5d54e-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="5d54e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d54e-102">SYNOPSIS</span></span>
<span data-ttu-id="5d54e-103">Obtém informações sobre fluxos de dados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="5d54e-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="5d54e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d54e-104">SYNTAX</span></span>

### <span data-ttu-id="5d54e-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="5d54e-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d54e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5d54e-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d54e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5d54e-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d54e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5d54e-108">DESCRIPTION</span></span>
<span data-ttu-id="5d54e-109">O cmdlet Get-AzDataFactoryV2DataFlow Obtém informações sobre fluxos de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="5d54e-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="5d54e-110">Se você especificar o nome de um fluxo de dados, esse cmdlet obterá informações sobre esse fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="5d54e-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="5d54e-111">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os fluxos de dados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="5d54e-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="5d54e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d54e-112">EXAMPLES</span></span>
### <span data-ttu-id="5d54e-113">Exemplo 1: obter informações sobre todos os fluxos de dados</span><span class="sxs-lookup"><span data-stu-id="5d54e-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="5d54e-114">Esse comando obtém informações sobre todos os fluxos de dados na fábrica de dados chamada WikiADF.</span><span class="sxs-lookup"><span data-stu-id="5d54e-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="5d54e-115">Exemplo 2: obter informações sobre um fluxo de dados específico</span><span class="sxs-lookup"><span data-stu-id="5d54e-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="5d54e-116">Esse comando obtém informações sobre o fluxo de dados chamado dataflow1 no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="5d54e-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="5d54e-117">OS</span><span class="sxs-lookup"><span data-stu-id="5d54e-117">PARAMETERS</span></span>

### <span data-ttu-id="5d54e-118">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="5d54e-118">-DataFactory</span></span>
<span data-ttu-id="5d54e-119">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="5d54e-119">The data factory object.</span></span>

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

### <span data-ttu-id="5d54e-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="5d54e-120">-DataFactoryName</span></span>
<span data-ttu-id="5d54e-121">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="5d54e-121">The data factory name.</span></span>

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

### <span data-ttu-id="5d54e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d54e-122">-DefaultProfile</span></span>
<span data-ttu-id="5d54e-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5d54e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d54e-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d54e-124">-Name</span></span>
<span data-ttu-id="5d54e-125">O nome do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="5d54e-125">The data flow name.</span></span>

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

### <span data-ttu-id="5d54e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d54e-126">-ResourceGroupName</span></span>
<span data-ttu-id="5d54e-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5d54e-127">The resource group name.</span></span>

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

### <span data-ttu-id="5d54e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d54e-128">-ResourceId</span></span>
<span data-ttu-id="5d54e-129">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="5d54e-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5d54e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d54e-130">CommonParameters</span></span>
<span data-ttu-id="5d54e-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d54e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d54e-132">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d54e-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d54e-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5d54e-133">INPUTS</span></span>

### <span data-ttu-id="5d54e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5d54e-134">System.String</span></span>

### <span data-ttu-id="5d54e-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5d54e-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="5d54e-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5d54e-136">OUTPUTS</span></span>

### <span data-ttu-id="5d54e-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="5d54e-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="5d54e-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5d54e-138">NOTES</span></span>
<span data-ttu-id="5d54e-139">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="5d54e-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5d54e-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d54e-140">RELATED LINKS</span></span>

[<span data-ttu-id="5d54e-141">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="5d54e-141">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

[<span data-ttu-id="5d54e-142">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="5d54e-142">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)