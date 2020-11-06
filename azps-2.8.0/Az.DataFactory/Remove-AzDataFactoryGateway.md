---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
ms.openlocfilehash: 0f8bd59f6215a2f9cc2bdbcc993da0cb373f70af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597007"
---
# <span data-ttu-id="b9b68-101">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b9b68-101">Remove-AzDataFactoryGateway</span></span>

## <span data-ttu-id="b9b68-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9b68-102">SYNOPSIS</span></span>
<span data-ttu-id="b9b68-103">Remove um gateway do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="b9b68-103">Removes a gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="b9b68-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9b68-104">SYNTAX</span></span>

### <span data-ttu-id="b9b68-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="b9b68-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9b68-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b9b68-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9b68-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9b68-107">DESCRIPTION</span></span>
<span data-ttu-id="b9b68-108">O cmdlet **Remove-AzDataFactoryGateway** remove o gateway especificado do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="b9b68-108">The **Remove-AzDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="b9b68-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9b68-109">EXAMPLES</span></span>

### <span data-ttu-id="b9b68-110">Exemplo 1: remover um gateway</span><span class="sxs-lookup"><span data-stu-id="b9b68-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="b9b68-111">Esse comando Remove o gateway chamado ContosoGateway da fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b9b68-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="b9b68-112">OS</span><span class="sxs-lookup"><span data-stu-id="b9b68-112">PARAMETERS</span></span>

### <span data-ttu-id="b9b68-113">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="b9b68-113">-DataFactory</span></span>
<span data-ttu-id="b9b68-114">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="b9b68-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b9b68-115">Esse cmdlet Remove um gateway da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b9b68-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b9b68-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b9b68-116">-DataFactoryName</span></span>
<span data-ttu-id="b9b68-117">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b9b68-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b9b68-118">Esse cmdlet Remove um gateway da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b9b68-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b9b68-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9b68-119">-DefaultProfile</span></span>
<span data-ttu-id="b9b68-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b9b68-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9b68-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b9b68-121">-Force</span></span>
<span data-ttu-id="b9b68-122">Indica que esse cmdlet Remove um gateway sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="b9b68-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="b9b68-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9b68-123">-Name</span></span>
<span data-ttu-id="b9b68-124">Especifica o nome do gateway a ser removido.</span><span class="sxs-lookup"><span data-stu-id="b9b68-124">Specifies the name of the gateway to remove.</span></span>

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

### <span data-ttu-id="b9b68-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9b68-125">-ResourceGroupName</span></span>
<span data-ttu-id="b9b68-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9b68-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b9b68-127">Esse cmdlet Remove um gateway que pertence ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b9b68-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b9b68-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b9b68-128">-Confirm</span></span>
<span data-ttu-id="b9b68-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9b68-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9b68-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9b68-130">-WhatIf</span></span>
<span data-ttu-id="b9b68-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b9b68-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9b68-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9b68-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9b68-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9b68-133">CommonParameters</span></span>
<span data-ttu-id="b9b68-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9b68-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9b68-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9b68-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9b68-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9b68-136">INPUTS</span></span>

### <span data-ttu-id="b9b68-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b9b68-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="b9b68-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b9b68-138">System.String</span></span>

## <span data-ttu-id="b9b68-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9b68-139">OUTPUTS</span></span>

### <span data-ttu-id="b9b68-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9b68-140">System.Boolean</span></span>

## <span data-ttu-id="b9b68-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9b68-141">NOTES</span></span>
* <span data-ttu-id="b9b68-142">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="b9b68-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b9b68-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9b68-143">RELATED LINKS</span></span>

[<span data-ttu-id="b9b68-144">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b9b68-144">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="b9b68-145">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b9b68-145">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="b9b68-146">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b9b68-146">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


