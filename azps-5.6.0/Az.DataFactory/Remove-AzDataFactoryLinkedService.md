---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
ms.openlocfilehash: 28b2b5b1e2370e78c77178e3ee07056bacf1a896
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887891"
---
# <span data-ttu-id="f96cd-101">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="f96cd-101">Remove-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="f96cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f96cd-102">SYNOPSIS</span></span>
<span data-ttu-id="f96cd-103">Remove um serviço vinculado da Fábrica de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="f96cd-103">Removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="f96cd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f96cd-104">SYNTAX</span></span>

### <span data-ttu-id="f96cd-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f96cd-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f96cd-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f96cd-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f96cd-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f96cd-107">DESCRIPTION</span></span>
<span data-ttu-id="f96cd-108">O cmdlet **Remove-AzDataFactoryLinkedService** remove um serviço vinculado do Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f96cd-108">The **Remove-AzDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="f96cd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f96cd-109">EXAMPLES</span></span>

### <span data-ttu-id="f96cd-110">Exemplo 1: Remover um serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="f96cd-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="f96cd-111">Este comando remove o serviço vinculado chamado LinkedServiceTest do fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="f96cd-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="f96cd-112">Este comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="f96cd-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="f96cd-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f96cd-113">PARAMETERS</span></span>

### <span data-ttu-id="f96cd-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f96cd-114">-DataFactory</span></span>
<span data-ttu-id="f96cd-115">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="f96cd-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f96cd-116">Este cmdlet remove um serviço vinculado do fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f96cd-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f96cd-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f96cd-117">-DataFactoryName</span></span>
<span data-ttu-id="f96cd-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f96cd-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f96cd-119">Este cmdlet remove um serviço vinculado do fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f96cd-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f96cd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f96cd-120">-DefaultProfile</span></span>
<span data-ttu-id="f96cd-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f96cd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f96cd-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f96cd-122">-Force</span></span>
<span data-ttu-id="f96cd-123">Indica que esse cmdlet remove um serviço vinculado sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="f96cd-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f96cd-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f96cd-124">-Name</span></span>
<span data-ttu-id="f96cd-125">Especifica o nome do serviço vinculado a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f96cd-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f96cd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f96cd-126">-ResourceGroupName</span></span>
<span data-ttu-id="f96cd-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f96cd-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f96cd-128">Este cmdlet remove um serviço vinculado do grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f96cd-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f96cd-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f96cd-129">-Confirm</span></span>
<span data-ttu-id="f96cd-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f96cd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f96cd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f96cd-131">-WhatIf</span></span>
<span data-ttu-id="f96cd-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f96cd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f96cd-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f96cd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f96cd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f96cd-134">CommonParameters</span></span>
<span data-ttu-id="f96cd-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f96cd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f96cd-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f96cd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f96cd-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f96cd-137">INPUTS</span></span>

### <span data-ttu-id="f96cd-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f96cd-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="f96cd-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f96cd-139">System.String</span></span>

## <span data-ttu-id="f96cd-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f96cd-140">OUTPUTS</span></span>

### <span data-ttu-id="f96cd-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="f96cd-141">System.Void</span></span>

## <span data-ttu-id="f96cd-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="f96cd-142">NOTES</span></span>
* <span data-ttu-id="f96cd-143">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="f96cd-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f96cd-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f96cd-144">RELATED LINKS</span></span>

[<span data-ttu-id="f96cd-145">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="f96cd-145">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="f96cd-146">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="f96cd-146">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)


