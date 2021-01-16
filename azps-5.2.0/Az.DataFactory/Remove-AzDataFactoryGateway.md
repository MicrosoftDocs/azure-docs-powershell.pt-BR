---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
ms.openlocfilehash: 6831395c4f3d63dc056729b22573a16d863013e1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257316"
---
# <span data-ttu-id="bb4cd-101">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="bb4cd-101">Remove-AzDataFactoryGateway</span></span>

## <span data-ttu-id="bb4cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb4cd-102">SYNOPSIS</span></span>
<span data-ttu-id="bb4cd-103">Remove um gateway do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="bb4cd-103">Removes a gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="bb4cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb4cd-104">SYNTAX</span></span>

### <span data-ttu-id="bb4cd-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb4cd-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb4cd-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bb4cd-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb4cd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb4cd-107">DESCRIPTION</span></span>
<span data-ttu-id="bb4cd-108">O cmdlet **Remove-AzDataFactoryGateway** remove o gateway especificado do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="bb4cd-108">The **Remove-AzDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="bb4cd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb4cd-109">EXAMPLES</span></span>

### <span data-ttu-id="bb4cd-110">Exemplo 1: remover um gateway</span><span class="sxs-lookup"><span data-stu-id="bb4cd-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="bb4cd-111">Esse comando Remove o gateway chamado ContosoGateway da fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="bb4cd-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="bb4cd-112">OS</span><span class="sxs-lookup"><span data-stu-id="bb4cd-112">PARAMETERS</span></span>

### <span data-ttu-id="bb4cd-113">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="bb4cd-113">-DataFactory</span></span>
<span data-ttu-id="bb4cd-114">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="bb4cd-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="bb4cd-115">Esse cmdlet Remove um gateway da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="bb4cd-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bb4cd-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="bb4cd-116">-DataFactoryName</span></span>
<span data-ttu-id="bb4cd-117">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="bb4cd-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="bb4cd-118">Esse cmdlet Remove um gateway da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="bb4cd-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bb4cd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb4cd-119">-DefaultProfile</span></span>
<span data-ttu-id="bb4cd-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bb4cd-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb4cd-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bb4cd-121">-Force</span></span>
<span data-ttu-id="bb4cd-122">Indica que esse cmdlet Remove um gateway sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="bb4cd-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="bb4cd-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb4cd-123">-Name</span></span>
<span data-ttu-id="bb4cd-124">Especifica o nome do gateway a ser removido.</span><span class="sxs-lookup"><span data-stu-id="bb4cd-124">Specifies the name of the gateway to remove.</span></span>

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

### <span data-ttu-id="bb4cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb4cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="bb4cd-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb4cd-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bb4cd-127">Esse cmdlet Remove um gateway que pertence ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="bb4cd-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bb4cd-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bb4cd-128">-Confirm</span></span>
<span data-ttu-id="bb4cd-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb4cd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb4cd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb4cd-130">-WhatIf</span></span>
<span data-ttu-id="bb4cd-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bb4cd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb4cd-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb4cd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb4cd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb4cd-133">CommonParameters</span></span>
<span data-ttu-id="bb4cd-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb4cd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb4cd-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb4cd-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb4cd-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb4cd-136">INPUTS</span></span>

### <span data-ttu-id="bb4cd-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bb4cd-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="bb4cd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bb4cd-138">System.String</span></span>

## <span data-ttu-id="bb4cd-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb4cd-139">OUTPUTS</span></span>

### <span data-ttu-id="bb4cd-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb4cd-140">System.Boolean</span></span>

## <span data-ttu-id="bb4cd-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb4cd-141">NOTES</span></span>
* <span data-ttu-id="bb4cd-142">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="bb4cd-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bb4cd-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb4cd-143">RELATED LINKS</span></span>

[<span data-ttu-id="bb4cd-144">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="bb4cd-144">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="bb4cd-145">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="bb4cd-145">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="bb4cd-146">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="bb4cd-146">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


