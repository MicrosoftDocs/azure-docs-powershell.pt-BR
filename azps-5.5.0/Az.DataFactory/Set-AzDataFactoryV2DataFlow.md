---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 44439d49fc89f00abaef904e80112d076121890f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407430"
---
# <span data-ttu-id="01d78-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="01d78-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="01d78-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01d78-102">SYNOPSIS</span></span>
<span data-ttu-id="01d78-103">Cria um fluxo de dados no Data Factory.</span><span class="sxs-lookup"><span data-stu-id="01d78-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="01d78-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01d78-104">SYNTAX</span></span>

### <span data-ttu-id="01d78-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="01d78-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01d78-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="01d78-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01d78-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="01d78-107">DESCRIPTION</span></span>
<span data-ttu-id="01d78-108">O Set-AzDataFactoryV2DataFlow cmdlet cria um fluxo de dados ou atualiza um fluxo de dados existente no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="01d78-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="01d78-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="01d78-109">EXAMPLES</span></span>

### <span data-ttu-id="01d78-110">Exemplo 1: Criar um fluxo de dados</span><span class="sxs-lookup"><span data-stu-id="01d78-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="01d78-111">Esse comando cria um fluxo de dados chamadoDemo1 na fábrica de dados chamada WikiADF.</span><span class="sxs-lookup"><span data-stu-id="01d78-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="01d78-112">O comando baseia o fluxo de dados em informações no TaxiDemo1.jsno arquivo.</span><span class="sxs-lookup"><span data-stu-id="01d78-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="01d78-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01d78-113">PARAMETERS</span></span>

### <span data-ttu-id="01d78-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="01d78-114">-DataFactoryName</span></span>
<span data-ttu-id="01d78-115">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="01d78-115">The data factory name.</span></span>

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

### <span data-ttu-id="01d78-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d78-116">-DefaultProfile</span></span>
<span data-ttu-id="01d78-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01d78-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01d78-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="01d78-118">-DefinitionFile</span></span>
<span data-ttu-id="01d78-119">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="01d78-119">The JSON file path.</span></span>

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

### <span data-ttu-id="01d78-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="01d78-120">-Force</span></span>
<span data-ttu-id="01d78-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="01d78-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="01d78-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="01d78-122">-Name</span></span>
<span data-ttu-id="01d78-123">O nome do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="01d78-123">The data flow name.</span></span>

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

### <span data-ttu-id="01d78-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01d78-124">-ResourceGroupName</span></span>
<span data-ttu-id="01d78-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="01d78-125">The resource group name.</span></span>

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

### <span data-ttu-id="01d78-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01d78-126">-ResourceId</span></span>
<span data-ttu-id="01d78-127">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="01d78-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="01d78-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="01d78-128">-Confirm</span></span>
<span data-ttu-id="01d78-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01d78-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01d78-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01d78-130">-WhatIf</span></span>
<span data-ttu-id="01d78-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="01d78-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01d78-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="01d78-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01d78-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d78-133">CommonParameters</span></span>
<span data-ttu-id="01d78-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01d78-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d78-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01d78-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d78-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="01d78-136">INPUTS</span></span>

### <span data-ttu-id="01d78-137">System.String</span><span class="sxs-lookup"><span data-stu-id="01d78-137">System.String</span></span>

## <span data-ttu-id="01d78-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="01d78-138">OUTPUTS</span></span>

### <span data-ttu-id="01d78-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="01d78-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="01d78-140">Notas</span><span class="sxs-lookup"><span data-stu-id="01d78-140">NOTES</span></span>
<span data-ttu-id="01d78-141">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="01d78-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="01d78-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01d78-142">RELATED LINKS</span></span>


