---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
ms.openlocfilehash: 6831395c4f3d63dc056729b22573a16d863013e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118813"
---
# <span data-ttu-id="bfc0a-101">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="bfc0a-101">Remove-AzDataFactoryGateway</span></span>

## <span data-ttu-id="bfc0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfc0a-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc0a-103">Remove um gateway do Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="bfc0a-103">Removes a gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="bfc0a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bfc0a-104">SYNTAX</span></span>

### <span data-ttu-id="bfc0a-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="bfc0a-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc0a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bfc0a-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfc0a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bfc0a-107">DESCRIPTION</span></span>
<span data-ttu-id="bfc0a-108">O cmdlet **Remove-AzDataFactoryGateway** remove o gateway especificado do Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="bfc0a-108">The **Remove-AzDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="bfc0a-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bfc0a-109">EXAMPLES</span></span>

### <span data-ttu-id="bfc0a-110">Exemplo 1: Remover um gateway</span><span class="sxs-lookup"><span data-stu-id="bfc0a-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="bfc0a-111">Esse comando remove o gateway chamado ContosoGateway da fábrica de dados chamada WikiADF.</span><span class="sxs-lookup"><span data-stu-id="bfc0a-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="bfc0a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfc0a-112">PARAMETERS</span></span>

### <span data-ttu-id="bfc0a-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bfc0a-113">-DataFactory</span></span>
<span data-ttu-id="bfc0a-114">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="bfc0a-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="bfc0a-115">Este cmdlet remove um gateway do fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bfc0a-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bfc0a-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bfc0a-116">-DataFactoryName</span></span>
<span data-ttu-id="bfc0a-117">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="bfc0a-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="bfc0a-118">Este cmdlet remove um gateway do fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bfc0a-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bfc0a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc0a-119">-DefaultProfile</span></span>
<span data-ttu-id="bfc0a-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="bfc0a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfc0a-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="bfc0a-121">-Force</span></span>
<span data-ttu-id="bfc0a-122">Indica que esse cmdlet remove um gateway sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="bfc0a-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="bfc0a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfc0a-123">-Name</span></span>
<span data-ttu-id="bfc0a-124">Especifica o nome do gateway a ser removido.</span><span class="sxs-lookup"><span data-stu-id="bfc0a-124">Specifies the name of the gateway to remove.</span></span>

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

### <span data-ttu-id="bfc0a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfc0a-125">-ResourceGroupName</span></span>
<span data-ttu-id="bfc0a-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfc0a-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bfc0a-127">Esse cmdlet remove um gateway que pertence ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bfc0a-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bfc0a-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bfc0a-128">-Confirm</span></span>
<span data-ttu-id="bfc0a-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfc0a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfc0a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfc0a-130">-WhatIf</span></span>
<span data-ttu-id="bfc0a-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bfc0a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfc0a-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bfc0a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfc0a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc0a-133">CommonParameters</span></span>
<span data-ttu-id="bfc0a-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfc0a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc0a-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfc0a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc0a-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="bfc0a-136">INPUTS</span></span>

### <span data-ttu-id="bfc0a-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bfc0a-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="bfc0a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bfc0a-138">System.String</span></span>

## <span data-ttu-id="bfc0a-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="bfc0a-139">OUTPUTS</span></span>

### <span data-ttu-id="bfc0a-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bfc0a-140">System.Boolean</span></span>

## <span data-ttu-id="bfc0a-141">Notas</span><span class="sxs-lookup"><span data-stu-id="bfc0a-141">NOTES</span></span>
* <span data-ttu-id="bfc0a-142">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="bfc0a-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bfc0a-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfc0a-143">RELATED LINKS</span></span>

[<span data-ttu-id="bfc0a-144">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="bfc0a-144">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="bfc0a-145">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="bfc0a-145">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="bfc0a-146">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="bfc0a-146">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


