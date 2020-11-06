---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 4dda510402b9395db24507f22d90da0f1fb6a44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426342"
---
# <span data-ttu-id="2cef0-101">Remove-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="2cef0-101">Remove-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="2cef0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2cef0-102">SYNOPSIS</span></span>
<span data-ttu-id="2cef0-103">Remover política WAF</span><span class="sxs-lookup"><span data-stu-id="2cef0-103">Remove WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cef0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2cef0-104">SYNTAX</span></span>

### <span data-ttu-id="2cef0-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2cef0-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cef0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cef0-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cef0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cef0-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cef0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2cef0-108">DESCRIPTION</span></span>
<span data-ttu-id="2cef0-109">O cmdlet **Remove-AzureRmFrontDoor** remove uma política WAF sob a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="2cef0-109">The **Remove-AzureRmFrontDoor** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="2cef0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2cef0-110">EXAMPLES</span></span>

### <span data-ttu-id="2cef0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2cef0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup
```

<span data-ttu-id="2cef0-112">Remova a política WAF chamada $name em $resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2cef0-112">Remove the WAF policy called $name in $resourceGroup.</span></span>

### <span data-ttu-id="2cef0-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2cef0-113">Example 2</span></span>
```powershell
PS C:\> Get--AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Remove-AzureRmFrontDoorFireWallPolicy
```

<span data-ttu-id="2cef0-114">Remover toda a política WAF em $resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2cef0-114">Remove all WAF policy in $resourceGroup.</span></span>

## <span data-ttu-id="2cef0-115">OS</span><span class="sxs-lookup"><span data-stu-id="2cef0-115">PARAMETERS</span></span>

### <span data-ttu-id="2cef0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cef0-116">-DefaultProfile</span></span>
<span data-ttu-id="2cef0-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2cef0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cef0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cef0-118">-InputObject</span></span>
<span data-ttu-id="2cef0-119">O objeto de política WAF a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="2cef0-119">The WAF policy object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cef0-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2cef0-120">-Name</span></span>
<span data-ttu-id="2cef0-121">O nome da política WAF a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="2cef0-121">The name of the WAF policy to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cef0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2cef0-122">-PassThru</span></span>
<span data-ttu-id="2cef0-123">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="2cef0-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="2cef0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cef0-124">-ResourceGroupName</span></span>
<span data-ttu-id="2cef0-125">O grupo de recursos ao qual a política de WAF pertence.</span><span class="sxs-lookup"><span data-stu-id="2cef0-125">The resource group to which the WAF policy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cef0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cef0-126">-ResourceId</span></span>
<span data-ttu-id="2cef0-127">ID do recurso da política WAF para excluir</span><span class="sxs-lookup"><span data-stu-id="2cef0-127">Resource Id of the WAF policy to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cef0-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2cef0-128">-Confirm</span></span>
<span data-ttu-id="2cef0-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cef0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cef0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cef0-130">-WhatIf</span></span>
<span data-ttu-id="2cef0-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2cef0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cef0-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2cef0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cef0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cef0-133">CommonParameters</span></span>
<span data-ttu-id="2cef0-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cef0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cef0-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cef0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cef0-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2cef0-136">INPUTS</span></span>

### <span data-ttu-id="2cef0-137">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="2cef0-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="2cef0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2cef0-138">System.String</span></span>

### <span data-ttu-id="2cef0-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2cef0-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2cef0-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2cef0-140">OUTPUTS</span></span>

### <span data-ttu-id="2cef0-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2cef0-141">System.Boolean</span></span>

## <span data-ttu-id="2cef0-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2cef0-142">NOTES</span></span>

## <span data-ttu-id="2cef0-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2cef0-143">RELATED LINKS</span></span>

<span data-ttu-id="2cef0-144">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="2cef0-144">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span></span>
