---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 42d9de3f23f1aca904aa0f42722217d0b9bf8a3a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429865"
---
# <span data-ttu-id="e7c09-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="e7c09-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="e7c09-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7c09-102">SYNOPSIS</span></span>
<span data-ttu-id="e7c09-103">Cria um fluxo de dados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e7c09-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="e7c09-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7c09-104">SYNTAX</span></span>

### <span data-ttu-id="e7c09-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e7c09-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7c09-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7c09-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7c09-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7c09-107">DESCRIPTION</span></span>
<span data-ttu-id="e7c09-108">O cmdlet Set-AzDataFactoryV2DataFlow cria um fluxo de dados ou atualiza um fluxo de dados existente no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="e7c09-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="e7c09-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7c09-109">EXAMPLES</span></span>

### <span data-ttu-id="e7c09-110">Exemplo 1: criar um fluxo de dados</span><span class="sxs-lookup"><span data-stu-id="e7c09-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="e7c09-111">Esse comando cria um fluxo de dados denominado TaxiDemo1 no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e7c09-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="e7c09-112">O comando baseia o fluxo de dados nas informações na TaxiDemo1.jsem arquivo.</span><span class="sxs-lookup"><span data-stu-id="e7c09-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="e7c09-113">OS</span><span class="sxs-lookup"><span data-stu-id="e7c09-113">PARAMETERS</span></span>

### <span data-ttu-id="e7c09-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e7c09-114">-DataFactoryName</span></span>
<span data-ttu-id="e7c09-115">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="e7c09-115">The data factory name.</span></span>

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

### <span data-ttu-id="e7c09-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7c09-116">-DefaultProfile</span></span>
<span data-ttu-id="e7c09-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7c09-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7c09-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e7c09-118">-DefinitionFile</span></span>
<span data-ttu-id="e7c09-119">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="e7c09-119">The JSON file path.</span></span>

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

### <span data-ttu-id="e7c09-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e7c09-120">-Force</span></span>
<span data-ttu-id="e7c09-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="e7c09-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e7c09-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7c09-122">-Name</span></span>
<span data-ttu-id="e7c09-123">O nome do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="e7c09-123">The data flow name.</span></span>

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

### <span data-ttu-id="e7c09-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7c09-124">-ResourceGroupName</span></span>
<span data-ttu-id="e7c09-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e7c09-125">The resource group name.</span></span>

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

### <span data-ttu-id="e7c09-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7c09-126">-ResourceId</span></span>
<span data-ttu-id="e7c09-127">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="e7c09-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e7c09-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e7c09-128">-Confirm</span></span>
<span data-ttu-id="e7c09-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7c09-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7c09-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7c09-130">-WhatIf</span></span>
<span data-ttu-id="e7c09-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7c09-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7c09-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7c09-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7c09-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7c09-133">CommonParameters</span></span>
<span data-ttu-id="e7c09-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7c09-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7c09-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7c09-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7c09-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7c09-136">INPUTS</span></span>

### <span data-ttu-id="e7c09-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e7c09-137">System.String</span></span>

## <span data-ttu-id="e7c09-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7c09-138">OUTPUTS</span></span>

### <span data-ttu-id="e7c09-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="e7c09-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="e7c09-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7c09-140">NOTES</span></span>
<span data-ttu-id="e7c09-141">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="e7c09-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e7c09-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7c09-142">RELATED LINKS</span></span>

[<span data-ttu-id="e7c09-143">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="e7c09-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="e7c09-144">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="e7c09-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)
