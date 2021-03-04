---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: 87a50c69449437401ff26b76b87cf0f334ab8d71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888372"
---
# <span data-ttu-id="12605-101">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="12605-101">Remove-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="12605-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12605-102">SYNOPSIS</span></span>
<span data-ttu-id="12605-103">Remove um serviço vinculado da Fábrica de Dados.</span><span class="sxs-lookup"><span data-stu-id="12605-103">Removes a linked service from Data Factory.</span></span>

## <span data-ttu-id="12605-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="12605-104">SYNTAX</span></span>

### <span data-ttu-id="12605-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="12605-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12605-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="12605-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12605-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="12605-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12605-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="12605-108">DESCRIPTION</span></span>
<span data-ttu-id="12605-109">O Remove-AzDataFactoryV2LinkedService cmdlet remove um serviço vinculado da Fábrica de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="12605-109">The Remove-AzDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="12605-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12605-110">EXAMPLES</span></span>

### <span data-ttu-id="12605-111">Exemplo 1: Remover um serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="12605-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="12605-112">Este comando remove o serviço vinculado chamado LinkedServiceTest do fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="12605-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="12605-113">Este comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="12605-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="12605-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="12605-114">PARAMETERS</span></span>

### <span data-ttu-id="12605-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="12605-115">-DataFactoryName</span></span>
<span data-ttu-id="12605-116">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="12605-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="12605-117">Este cmdlet remove um serviço vinculado do fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="12605-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="12605-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12605-118">-DefaultProfile</span></span>
<span data-ttu-id="12605-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="12605-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12605-120">-Force</span><span class="sxs-lookup"><span data-stu-id="12605-120">-Force</span></span>
<span data-ttu-id="12605-121">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="12605-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="12605-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12605-122">-InputObject</span></span>
<span data-ttu-id="12605-123">Especifica o objeto LinkedService a ser removido.</span><span class="sxs-lookup"><span data-stu-id="12605-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12605-124">-Name</span><span class="sxs-lookup"><span data-stu-id="12605-124">-Name</span></span>
<span data-ttu-id="12605-125">Especifica o nome do serviço vinculado a ser removido.</span><span class="sxs-lookup"><span data-stu-id="12605-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="12605-126">Nome do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="12605-126">Name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12605-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12605-127">-ResourceGroupName</span></span>
<span data-ttu-id="12605-128">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="12605-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="12605-129">Este cmdlet remove um serviço vinculado do grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="12605-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="12605-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12605-130">-ResourceId</span></span>
<span data-ttu-id="12605-131">A ID de recurso do Azure do serviço vinculado a ser removido.</span><span class="sxs-lookup"><span data-stu-id="12605-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="12605-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12605-132">-Confirm</span></span>
<span data-ttu-id="12605-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12605-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12605-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12605-134">-WhatIf</span></span>
<span data-ttu-id="12605-135">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12605-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="12605-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12605-136">CommonParameters</span></span>
<span data-ttu-id="12605-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12605-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12605-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12605-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12605-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12605-139">INPUTS</span></span>

### <span data-ttu-id="12605-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="12605-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

### <span data-ttu-id="12605-141">System.String</span><span class="sxs-lookup"><span data-stu-id="12605-141">System.String</span></span>

## <span data-ttu-id="12605-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="12605-142">OUTPUTS</span></span>

### <span data-ttu-id="12605-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="12605-143">System.Void</span></span>

## <span data-ttu-id="12605-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="12605-144">NOTES</span></span>
<span data-ttu-id="12605-145">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="12605-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="12605-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12605-146">RELATED LINKS</span></span>

[<span data-ttu-id="12605-147">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="12605-147">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="12605-148">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="12605-148">Set-AzDataFactoryV2LinkedService</span></span>]()

