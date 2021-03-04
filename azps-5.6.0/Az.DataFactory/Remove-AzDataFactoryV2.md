---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
ms.openlocfilehash: 99033646aac6f41397a7097afc8d78626d905a95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892982"
---
# <span data-ttu-id="166fd-101">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="166fd-101">Remove-AzDataFactoryV2</span></span>

## <span data-ttu-id="166fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="166fd-102">SYNOPSIS</span></span>
<span data-ttu-id="166fd-103">Remove um fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="166fd-103">Removes a data factory.</span></span>

## <span data-ttu-id="166fd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="166fd-104">SYNTAX</span></span>

### <span data-ttu-id="166fd-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="166fd-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="166fd-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="166fd-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="166fd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="166fd-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="166fd-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="166fd-108">DESCRIPTION</span></span>
<span data-ttu-id="166fd-109">O Remove-AzDataFactoryV2 cmdlet remove um fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="166fd-109">The Remove-AzDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="166fd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="166fd-110">EXAMPLES</span></span>

### <span data-ttu-id="166fd-111">Exemplo 1: Remover um fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="166fd-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="166fd-112">Este comando remove o fábrica de dados chamado WikiADF do grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="166fd-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="166fd-113">Este comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="166fd-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="166fd-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="166fd-114">PARAMETERS</span></span>

### <span data-ttu-id="166fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="166fd-115">-DefaultProfile</span></span>
<span data-ttu-id="166fd-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="166fd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="166fd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="166fd-117">-Force</span></span>
<span data-ttu-id="166fd-118">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="166fd-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="166fd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="166fd-119">-InputObject</span></span>
<span data-ttu-id="166fd-120">Especifica o objeto DataFactory a ser removido.</span><span class="sxs-lookup"><span data-stu-id="166fd-120">Specifies the DataFactory object to remove.</span></span>

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

### <span data-ttu-id="166fd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="166fd-121">-Name</span></span>
<span data-ttu-id="166fd-122">Especifica o nome do fábrica de dados a ser removido.</span><span class="sxs-lookup"><span data-stu-id="166fd-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="166fd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="166fd-123">-ResourceGroupName</span></span>
<span data-ttu-id="166fd-124">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="166fd-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="166fd-125">Este cmdlet remove um fábrica de dados do grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="166fd-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="166fd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="166fd-126">-ResourceId</span></span>
<span data-ttu-id="166fd-127">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="166fd-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="166fd-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="166fd-128">-Confirm</span></span>
<span data-ttu-id="166fd-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="166fd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="166fd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="166fd-130">-WhatIf</span></span>
<span data-ttu-id="166fd-131">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="166fd-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="166fd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="166fd-132">CommonParameters</span></span>
<span data-ttu-id="166fd-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="166fd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="166fd-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="166fd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="166fd-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="166fd-135">INPUTS</span></span>

### <span data-ttu-id="166fd-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="166fd-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="166fd-137">System.String</span><span class="sxs-lookup"><span data-stu-id="166fd-137">System.String</span></span>

## <span data-ttu-id="166fd-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="166fd-138">OUTPUTS</span></span>

### <span data-ttu-id="166fd-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="166fd-139">System.Void</span></span>

## <span data-ttu-id="166fd-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="166fd-140">NOTES</span></span>
<span data-ttu-id="166fd-141">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="166fd-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="166fd-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="166fd-142">RELATED LINKS</span></span>

[<span data-ttu-id="166fd-143">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="166fd-143">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="166fd-144">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="166fd-144">Set-AzDataFactoryV2</span></span>]()
