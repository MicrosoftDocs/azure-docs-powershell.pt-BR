---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: d36e362f1782e3566bc0d2febd65aebd4c68220d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116498"
---
# <span data-ttu-id="00d8e-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="00d8e-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="00d8e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00d8e-102">SYNOPSIS</span></span>
<span data-ttu-id="00d8e-103">Remove um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="00d8e-103">Removes a container registry.</span></span>

## <span data-ttu-id="00d8e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00d8e-104">SYNTAX</span></span>

### <span data-ttu-id="00d8e-105">NameResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="00d8e-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00d8e-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00d8e-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00d8e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00d8e-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00d8e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="00d8e-108">DESCRIPTION</span></span>
<span data-ttu-id="00d8e-109">O Remove-AzContainerRegistry cmdlet remove um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="00d8e-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="00d8e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="00d8e-110">EXAMPLES</span></span>

### <span data-ttu-id="00d8e-111">Exemplo 1: Remover um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="00d8e-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="00d8e-112">Esse comando remove o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="00d8e-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="00d8e-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00d8e-113">PARAMETERS</span></span>

### <span data-ttu-id="00d8e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00d8e-114">-DefaultProfile</span></span>
<span data-ttu-id="00d8e-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="00d8e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00d8e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="00d8e-116">-Name</span></span>
<span data-ttu-id="00d8e-117">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="00d8e-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="00d8e-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00d8e-118">-PassThru</span></span>
<span data-ttu-id="00d8e-119">Indica que esse cmdlet retornará verdadeiro se a remoção tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="00d8e-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="00d8e-120">-Registro</span><span class="sxs-lookup"><span data-stu-id="00d8e-120">-Registry</span></span>
<span data-ttu-id="00d8e-121">Objeto do Registro de Contêineres.</span><span class="sxs-lookup"><span data-stu-id="00d8e-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="00d8e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00d8e-122">-ResourceGroupName</span></span>
<span data-ttu-id="00d8e-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="00d8e-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="00d8e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00d8e-124">-ResourceId</span></span>
<span data-ttu-id="00d8e-125">A ID do recurso de registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="00d8e-125">The container registry resource id</span></span>

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

### <span data-ttu-id="00d8e-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="00d8e-126">-Confirm</span></span>
<span data-ttu-id="00d8e-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00d8e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00d8e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00d8e-128">-WhatIf</span></span>
<span data-ttu-id="00d8e-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="00d8e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00d8e-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="00d8e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00d8e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00d8e-131">CommonParameters</span></span>
<span data-ttu-id="00d8e-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00d8e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00d8e-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00d8e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00d8e-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="00d8e-134">INPUTS</span></span>

### <span data-ttu-id="00d8e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="00d8e-135">System.String</span></span>

## <span data-ttu-id="00d8e-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="00d8e-136">OUTPUTS</span></span>

### <span data-ttu-id="00d8e-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00d8e-137">System.Boolean</span></span>

## <span data-ttu-id="00d8e-138">Notas</span><span class="sxs-lookup"><span data-stu-id="00d8e-138">NOTES</span></span>

## <span data-ttu-id="00d8e-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00d8e-139">RELATED LINKS</span></span>

[<span data-ttu-id="00d8e-140">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="00d8e-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="00d8e-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="00d8e-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="00d8e-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="00d8e-142">Update-AzContainerRegistry</span></span>]()

