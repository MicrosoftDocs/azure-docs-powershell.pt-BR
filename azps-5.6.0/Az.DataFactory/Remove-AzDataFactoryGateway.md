---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
ms.openlocfilehash: eb9100bf4843d7213d2fbb89ac1827ba7ee1e509
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886060"
---
# <span data-ttu-id="b22c3-101">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b22c3-101">Remove-AzDataFactoryGateway</span></span>

## <span data-ttu-id="b22c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b22c3-102">SYNOPSIS</span></span>
<span data-ttu-id="b22c3-103">Remove um gateway da Fábrica de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="b22c3-103">Removes a gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="b22c3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b22c3-104">SYNTAX</span></span>

### <span data-ttu-id="b22c3-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b22c3-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b22c3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b22c3-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b22c3-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b22c3-107">DESCRIPTION</span></span>
<span data-ttu-id="b22c3-108">O cmdlet **Remove-AzDataFactoryGateway** remove o gateway especificado do Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b22c3-108">The **Remove-AzDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="b22c3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b22c3-109">EXAMPLES</span></span>

### <span data-ttu-id="b22c3-110">Exemplo 1: Remover um gateway</span><span class="sxs-lookup"><span data-stu-id="b22c3-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="b22c3-111">Este comando remove o gateway chamado ContosoGateway do fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b22c3-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="b22c3-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b22c3-112">PARAMETERS</span></span>

### <span data-ttu-id="b22c3-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b22c3-113">-DataFactory</span></span>
<span data-ttu-id="b22c3-114">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="b22c3-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b22c3-115">Este cmdlet remove um gateway do fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b22c3-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b22c3-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b22c3-116">-DataFactoryName</span></span>
<span data-ttu-id="b22c3-117">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b22c3-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b22c3-118">Este cmdlet remove um gateway do fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b22c3-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b22c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b22c3-119">-DefaultProfile</span></span>
<span data-ttu-id="b22c3-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b22c3-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b22c3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b22c3-121">-Force</span></span>
<span data-ttu-id="b22c3-122">Indica que esse cmdlet remove um gateway sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="b22c3-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="b22c3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b22c3-123">-Name</span></span>
<span data-ttu-id="b22c3-124">Especifica o nome do gateway a ser removido.</span><span class="sxs-lookup"><span data-stu-id="b22c3-124">Specifies the name of the gateway to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b22c3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b22c3-125">-ResourceGroupName</span></span>
<span data-ttu-id="b22c3-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b22c3-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b22c3-127">Este cmdlet remove um gateway que pertence ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b22c3-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b22c3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b22c3-128">-Confirm</span></span>
<span data-ttu-id="b22c3-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b22c3-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22c3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b22c3-130">-WhatIf</span></span>
<span data-ttu-id="b22c3-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b22c3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b22c3-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b22c3-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22c3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b22c3-133">CommonParameters</span></span>
<span data-ttu-id="b22c3-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b22c3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b22c3-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b22c3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b22c3-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b22c3-136">INPUTS</span></span>

### <span data-ttu-id="b22c3-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b22c3-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="b22c3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b22c3-138">System.String</span></span>

## <span data-ttu-id="b22c3-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b22c3-139">OUTPUTS</span></span>

### <span data-ttu-id="b22c3-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b22c3-140">System.Boolean</span></span>

## <span data-ttu-id="b22c3-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="b22c3-141">NOTES</span></span>
* <span data-ttu-id="b22c3-142">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="b22c3-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b22c3-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b22c3-143">RELATED LINKS</span></span>

[<span data-ttu-id="b22c3-144">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b22c3-144">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="b22c3-145">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b22c3-145">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="b22c3-146">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b22c3-146">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


