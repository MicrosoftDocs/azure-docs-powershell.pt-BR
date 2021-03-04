---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: 49da6e1efbd1bb0e6b0ac4dc693d51fe5b58bfac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901499"
---
# <span data-ttu-id="69305-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="69305-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="69305-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69305-102">SYNOPSIS</span></span>
<span data-ttu-id="69305-103">Remove um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="69305-103">Removes a container registry.</span></span>

## <span data-ttu-id="69305-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="69305-104">SYNTAX</span></span>

### <span data-ttu-id="69305-105">NameResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="69305-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69305-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69305-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69305-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69305-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69305-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="69305-108">DESCRIPTION</span></span>
<span data-ttu-id="69305-109">O Remove-AzContainerRegistry cmdlet remove um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="69305-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="69305-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69305-110">EXAMPLES</span></span>

### <span data-ttu-id="69305-111">Exemplo 1: Remover um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="69305-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="69305-112">Este comando remove o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="69305-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="69305-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="69305-113">PARAMETERS</span></span>

### <span data-ttu-id="69305-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69305-114">-DefaultProfile</span></span>
<span data-ttu-id="69305-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="69305-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69305-116">-Name</span><span class="sxs-lookup"><span data-stu-id="69305-116">-Name</span></span>
<span data-ttu-id="69305-117">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="69305-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69305-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69305-118">-PassThru</span></span>
<span data-ttu-id="69305-119">Indica que esse cmdlet retornará true se a remoção tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="69305-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="69305-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="69305-120">-Registry</span></span>
<span data-ttu-id="69305-121">Objeto Container Registry.</span><span class="sxs-lookup"><span data-stu-id="69305-121">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69305-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69305-122">-ResourceGroupName</span></span>
<span data-ttu-id="69305-123">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="69305-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69305-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69305-124">-ResourceId</span></span>
<span data-ttu-id="69305-125">A ID de recurso do Registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="69305-125">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69305-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69305-126">-Confirm</span></span>
<span data-ttu-id="69305-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69305-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69305-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69305-128">-WhatIf</span></span>
<span data-ttu-id="69305-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="69305-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69305-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="69305-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69305-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69305-131">CommonParameters</span></span>
<span data-ttu-id="69305-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69305-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69305-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69305-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69305-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69305-134">INPUTS</span></span>

### <span data-ttu-id="69305-135">System.String</span><span class="sxs-lookup"><span data-stu-id="69305-135">System.String</span></span>

## <span data-ttu-id="69305-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="69305-136">OUTPUTS</span></span>

### <span data-ttu-id="69305-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69305-137">System.Boolean</span></span>

## <span data-ttu-id="69305-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="69305-138">NOTES</span></span>

## <span data-ttu-id="69305-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69305-139">RELATED LINKS</span></span>

[<span data-ttu-id="69305-140">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="69305-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="69305-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="69305-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="69305-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="69305-142">Update-AzContainerRegistry</span></span>]()

