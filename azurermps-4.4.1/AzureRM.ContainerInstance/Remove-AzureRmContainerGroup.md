---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
ms.openlocfilehash: be9a289e7d3aca0bc0a4cc4e2ae8e23dbe5b1ae7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609718"
---
# <span data-ttu-id="75146-101">Remove-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="75146-101">Remove-AzureRmContainerGroup</span></span>

## <span data-ttu-id="75146-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75146-102">SYNOPSIS</span></span>
<span data-ttu-id="75146-103">Remove um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="75146-103">Removes a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75146-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75146-104">SYNTAX</span></span>

### <span data-ttu-id="75146-105">RemoveContainerGroupByResourceGroupAndNameParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="75146-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75146-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="75146-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzureRmContainerGroup -InputObject <PSContainerGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75146-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="75146-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzureRmContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75146-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75146-108">DESCRIPTION</span></span>
<span data-ttu-id="75146-109">O cmdlet **Remove-AzureRmContainerGroup** remove um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="75146-109">The **Remove-AzureRmContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="75146-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75146-110">EXAMPLES</span></span>

### <span data-ttu-id="75146-111">Exemplo 1: Remove um grupo de contêineres</span><span class="sxs-lookup"><span data-stu-id="75146-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="75146-112">Esse comando Remove o grupo de contêineres especificado.</span><span class="sxs-lookup"><span data-stu-id="75146-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="75146-113">Exemplo 2: Remove um grupo de contêineres por tubulação</span><span class="sxs-lookup"><span data-stu-id="75146-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="75146-114">Esse comando Remove um grupo de contêineres por tubulação.</span><span class="sxs-lookup"><span data-stu-id="75146-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="75146-115">Exemplo 3: Remove um grupo de contêineres por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="75146-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="75146-116">Esse comando Remove um grupo de contêineres por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="75146-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="75146-117">OS</span><span class="sxs-lookup"><span data-stu-id="75146-117">PARAMETERS</span></span>

### <span data-ttu-id="75146-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="75146-118">-Confirm</span></span>
<span data-ttu-id="75146-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75146-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75146-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75146-120">-InputObject</span></span>
<span data-ttu-id="75146-121">O grupo de contêineres a ser removido.</span><span class="sxs-lookup"><span data-stu-id="75146-121">The container group to remove.</span></span>

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

### <span data-ttu-id="75146-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="75146-122">-Name</span></span>
<span data-ttu-id="75146-123">O nome do grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="75146-123">The container group name.</span></span>

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

### <span data-ttu-id="75146-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75146-124">-PassThru</span></span>
<span data-ttu-id="75146-125">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="75146-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="75146-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75146-126">-ResourceGroupName</span></span>
<span data-ttu-id="75146-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="75146-127">The resource group name.</span></span>

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

### <span data-ttu-id="75146-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75146-128">-ResourceId</span></span>
<span data-ttu-id="75146-129">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="75146-129">The resource id.</span></span>

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

### <span data-ttu-id="75146-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75146-130">-WhatIf</span></span>
<span data-ttu-id="75146-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75146-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75146-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75146-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75146-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75146-133">-DefaultProfile</span></span>
<span data-ttu-id="75146-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75146-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75146-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75146-135">CommonParameters</span></span>
<span data-ttu-id="75146-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75146-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75146-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75146-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75146-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75146-138">INPUTS</span></span>

### <span data-ttu-id="75146-139">System. String</span><span class="sxs-lookup"><span data-stu-id="75146-139">System.String</span></span>
<span data-ttu-id="75146-140">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="75146-140">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="75146-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75146-141">OUTPUTS</span></span>

### <span data-ttu-id="75146-142">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="75146-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="75146-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75146-143">NOTES</span></span>

## <span data-ttu-id="75146-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75146-144">RELATED LINKS</span></span>

