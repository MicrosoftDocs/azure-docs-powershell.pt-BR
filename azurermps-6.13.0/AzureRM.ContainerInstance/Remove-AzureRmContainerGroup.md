---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/remove-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
ms.openlocfilehash: f1971f8bf0e7d8e779743739b8dd041effe3ba5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427251"
---
# <span data-ttu-id="f6311-101">Remove-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="f6311-101">Remove-AzureRmContainerGroup</span></span>

## <span data-ttu-id="f6311-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6311-102">SYNOPSIS</span></span>
<span data-ttu-id="f6311-103">Remove um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="f6311-103">Removes a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6311-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6311-104">SYNTAX</span></span>

### <span data-ttu-id="f6311-105">RemoveContainerGroupByResourceGroupAndNameParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f6311-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6311-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="f6311-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzureRmContainerGroup -InputObject <PSContainerGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6311-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="f6311-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzureRmContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6311-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6311-108">DESCRIPTION</span></span>
<span data-ttu-id="f6311-109">O cmdlet **Remove-AzureRmContainerGroup** remove um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="f6311-109">The **Remove-AzureRmContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="f6311-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6311-110">EXAMPLES</span></span>

### <span data-ttu-id="f6311-111">Exemplo 1: Remove um grupo de contêineres</span><span class="sxs-lookup"><span data-stu-id="f6311-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="f6311-112">Esse comando Remove o grupo de contêineres especificado.</span><span class="sxs-lookup"><span data-stu-id="f6311-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="f6311-113">Exemplo 2: Remove um grupo de contêineres por tubulação</span><span class="sxs-lookup"><span data-stu-id="f6311-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="f6311-114">Esse comando Remove um grupo de contêineres por tubulação.</span><span class="sxs-lookup"><span data-stu-id="f6311-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="f6311-115">Exemplo 3: Remove um grupo de contêineres por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="f6311-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="f6311-116">Esse comando Remove um grupo de contêineres por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="f6311-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="f6311-117">OS</span><span class="sxs-lookup"><span data-stu-id="f6311-117">PARAMETERS</span></span>

### <span data-ttu-id="f6311-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6311-118">-DefaultProfile</span></span>
<span data-ttu-id="f6311-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6311-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6311-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6311-120">-InputObject</span></span>
<span data-ttu-id="f6311-121">O grupo de contêineres a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f6311-121">The container group to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6311-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6311-122">-Name</span></span>
<span data-ttu-id="f6311-123">O nome do grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="f6311-123">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6311-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6311-124">-PassThru</span></span>
<span data-ttu-id="f6311-125">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="f6311-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f6311-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6311-126">-ResourceGroupName</span></span>
<span data-ttu-id="f6311-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f6311-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6311-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6311-128">-ResourceId</span></span>
<span data-ttu-id="f6311-129">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="f6311-129">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6311-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f6311-130">-Confirm</span></span>
<span data-ttu-id="f6311-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6311-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6311-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6311-132">-WhatIf</span></span>
<span data-ttu-id="f6311-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f6311-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6311-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f6311-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6311-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6311-135">CommonParameters</span></span>
<span data-ttu-id="f6311-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6311-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6311-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6311-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6311-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6311-138">INPUTS</span></span>

### <span data-ttu-id="f6311-139">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="f6311-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>
<span data-ttu-id="f6311-140">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f6311-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f6311-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f6311-141">System.String</span></span>

## <span data-ttu-id="f6311-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6311-142">OUTPUTS</span></span>

### <span data-ttu-id="f6311-143">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="f6311-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="f6311-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6311-144">NOTES</span></span>

## <span data-ttu-id="f6311-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6311-145">RELATED LINKS</span></span>
