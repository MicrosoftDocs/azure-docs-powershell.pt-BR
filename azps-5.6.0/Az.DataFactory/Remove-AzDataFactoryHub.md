---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
ms.openlocfilehash: 8144d1989f6bec9c1342613cf4776a6dae0a9c27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887893"
---
# <span data-ttu-id="f7d68-101">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="f7d68-101">Remove-AzDataFactoryHub</span></span>

## <span data-ttu-id="f7d68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7d68-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d68-103">Remove um hub da Fábrica de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7d68-103">Removes a hub from Azure Data Factory.</span></span>

## <span data-ttu-id="f7d68-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f7d68-104">SYNTAX</span></span>

### <span data-ttu-id="f7d68-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f7d68-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7d68-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f7d68-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7d68-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f7d68-107">DESCRIPTION</span></span>
<span data-ttu-id="f7d68-108">O cmdlet **Remove-AzDataFactoryHub** remove um hub do Azure Data Factory no grupo de recursos especificado do Azure e no fábrica de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="f7d68-108">The **Remove-AzDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="f7d68-109">Se você remover um hub, todos os serviços e pipelines vinculados no hub também serão removidos.</span><span class="sxs-lookup"><span data-stu-id="f7d68-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="f7d68-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7d68-110">EXAMPLES</span></span>

### <span data-ttu-id="f7d68-111">Exemplo 1: Remover um hub</span><span class="sxs-lookup"><span data-stu-id="f7d68-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="f7d68-112">Este comando remove o hub chamado ContosoDataHub do grupo de recursos do Azure chamado ADFResourceGroup e do fábrica de dados chamado ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="f7d68-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="f7d68-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f7d68-113">PARAMETERS</span></span>

### <span data-ttu-id="f7d68-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7d68-114">-DataFactory</span></span>
<span data-ttu-id="f7d68-115">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="f7d68-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f7d68-116">Este cmdlet remove um hub do fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f7d68-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f7d68-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f7d68-117">-DataFactoryName</span></span>
<span data-ttu-id="f7d68-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f7d68-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f7d68-119">Este cmdlet remove um hub do fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f7d68-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f7d68-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d68-120">-DefaultProfile</span></span>
<span data-ttu-id="f7d68-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f7d68-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7d68-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f7d68-122">-Force</span></span>
<span data-ttu-id="f7d68-123">Indica que esse cmdlet remove um hub sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="f7d68-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f7d68-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f7d68-124">-Name</span></span>
<span data-ttu-id="f7d68-125">Especifica o nome do hub a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f7d68-125">Specifies the name of the hub to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d68-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7d68-126">-ResourceGroupName</span></span>
<span data-ttu-id="f7d68-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7d68-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f7d68-128">Este cmdlet remove um hub do grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f7d68-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f7d68-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7d68-129">-Confirm</span></span>
<span data-ttu-id="f7d68-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7d68-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7d68-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7d68-131">-WhatIf</span></span>
<span data-ttu-id="f7d68-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f7d68-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7d68-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f7d68-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7d68-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d68-134">CommonParameters</span></span>
<span data-ttu-id="f7d68-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7d68-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d68-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7d68-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d68-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7d68-137">INPUTS</span></span>

### <span data-ttu-id="f7d68-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f7d68-138">System.String</span></span>

### <span data-ttu-id="f7d68-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f7d68-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="f7d68-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f7d68-140">OUTPUTS</span></span>

### <span data-ttu-id="f7d68-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f7d68-141">System.Boolean</span></span>

## <span data-ttu-id="f7d68-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="f7d68-142">NOTES</span></span>
* <span data-ttu-id="f7d68-143">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="f7d68-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f7d68-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7d68-144">RELATED LINKS</span></span>

[<span data-ttu-id="f7d68-145">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="f7d68-145">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="f7d68-146">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="f7d68-146">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)


