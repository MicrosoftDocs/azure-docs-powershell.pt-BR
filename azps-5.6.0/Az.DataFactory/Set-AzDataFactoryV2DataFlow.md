---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 6827fb627a3d393c8971886cee869c330f7d4099
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891450"
---
# <span data-ttu-id="0bf1d-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="0bf1d-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="0bf1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bf1d-102">SYNOPSIS</span></span>
<span data-ttu-id="0bf1d-103">Cria um fluxo de dados na Fábrica de Dados.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="0bf1d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0bf1d-104">SYNTAX</span></span>

### <span data-ttu-id="0bf1d-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0bf1d-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bf1d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0bf1d-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bf1d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0bf1d-107">DESCRIPTION</span></span>
<span data-ttu-id="0bf1d-108">O Set-AzDataFactoryV2DataFlow cmdlet cria um fluxo de dados ou atualiza um fluxo de dados existente no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="0bf1d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0bf1d-109">EXAMPLES</span></span>

### <span data-ttu-id="0bf1d-110">Exemplo 1: Criar um fluxo de dados</span><span class="sxs-lookup"><span data-stu-id="0bf1d-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="0bf1d-111">Este comando cria um fluxo de dados chamado TaxiDemo1 no fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="0bf1d-112">O comando baseia o fluxo de dados em informações no arquivo TaxiDemo1.json.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="0bf1d-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0bf1d-113">PARAMETERS</span></span>

### <span data-ttu-id="0bf1d-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0bf1d-114">-DataFactoryName</span></span>
<span data-ttu-id="0bf1d-115">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-115">The data factory name.</span></span>

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

### <span data-ttu-id="0bf1d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bf1d-116">-DefaultProfile</span></span>
<span data-ttu-id="0bf1d-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bf1d-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="0bf1d-118">-DefinitionFile</span></span>
<span data-ttu-id="0bf1d-119">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bf1d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0bf1d-120">-Force</span></span>
<span data-ttu-id="0bf1d-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0bf1d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0bf1d-122">-Name</span></span>
<span data-ttu-id="0bf1d-123">O nome do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bf1d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bf1d-124">-ResourceGroupName</span></span>
<span data-ttu-id="0bf1d-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-125">The resource group name.</span></span>

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

### <span data-ttu-id="0bf1d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bf1d-126">-ResourceId</span></span>
<span data-ttu-id="0bf1d-127">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0bf1d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0bf1d-128">-Confirm</span></span>
<span data-ttu-id="0bf1d-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bf1d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bf1d-130">-WhatIf</span></span>
<span data-ttu-id="0bf1d-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bf1d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bf1d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bf1d-133">CommonParameters</span></span>
<span data-ttu-id="0bf1d-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bf1d-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bf1d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bf1d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0bf1d-136">INPUTS</span></span>

### <span data-ttu-id="0bf1d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0bf1d-137">System.String</span></span>

## <span data-ttu-id="0bf1d-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0bf1d-138">OUTPUTS</span></span>

### <span data-ttu-id="0bf1d-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="0bf1d-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="0bf1d-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="0bf1d-140">NOTES</span></span>
<span data-ttu-id="0bf1d-141">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="0bf1d-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0bf1d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0bf1d-142">RELATED LINKS</span></span>

[<span data-ttu-id="0bf1d-143">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="0bf1d-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="0bf1d-144">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="0bf1d-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)
