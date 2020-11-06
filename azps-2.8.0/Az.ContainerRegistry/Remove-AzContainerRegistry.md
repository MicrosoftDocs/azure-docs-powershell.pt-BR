---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: c389f62f6f9b76f0ebdab30ddf600d333263a87c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597121"
---
# <span data-ttu-id="f4857-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f4857-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="f4857-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4857-102">SYNOPSIS</span></span>
<span data-ttu-id="f4857-103">Remove um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f4857-103">Removes a container registry.</span></span>

## <span data-ttu-id="f4857-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4857-104">SYNTAX</span></span>

### <span data-ttu-id="f4857-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f4857-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4857-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4857-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4857-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4857-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4857-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f4857-108">DESCRIPTION</span></span>
<span data-ttu-id="f4857-109">O cmdlet Remove-AzContainerRegistry remove um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f4857-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="f4857-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4857-110">EXAMPLES</span></span>

### <span data-ttu-id="f4857-111">Exemplo 1: remover um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="f4857-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="f4857-112">Esse comando Remove o registro do contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="f4857-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="f4857-113">OS</span><span class="sxs-lookup"><span data-stu-id="f4857-113">PARAMETERS</span></span>

### <span data-ttu-id="f4857-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4857-114">-DefaultProfile</span></span>
<span data-ttu-id="f4857-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f4857-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4857-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4857-116">-Name</span></span>
<span data-ttu-id="f4857-117">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f4857-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="f4857-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4857-118">-PassThru</span></span>
<span data-ttu-id="f4857-119">Indica que esse cmdlet retorna true se a remoção tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f4857-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="f4857-120">-Registro</span><span class="sxs-lookup"><span data-stu-id="f4857-120">-Registry</span></span>
<span data-ttu-id="f4857-121">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f4857-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="f4857-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4857-122">-ResourceGroupName</span></span>
<span data-ttu-id="f4857-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f4857-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="f4857-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4857-124">-ResourceId</span></span>
<span data-ttu-id="f4857-125">A ID do recurso do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="f4857-125">The container registry resource id</span></span>

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

### <span data-ttu-id="f4857-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f4857-126">-Confirm</span></span>
<span data-ttu-id="f4857-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4857-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4857-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4857-128">-WhatIf</span></span>
<span data-ttu-id="f4857-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f4857-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4857-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4857-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4857-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4857-131">CommonParameters</span></span>
<span data-ttu-id="f4857-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4857-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4857-133">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4857-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4857-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f4857-134">INPUTS</span></span>

### <span data-ttu-id="f4857-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f4857-135">System.String</span></span>

## <span data-ttu-id="f4857-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f4857-136">OUTPUTS</span></span>

### <span data-ttu-id="f4857-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4857-137">System.Boolean</span></span>

## <span data-ttu-id="f4857-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f4857-138">NOTES</span></span>

## <span data-ttu-id="f4857-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4857-139">RELATED LINKS</span></span>

[<span data-ttu-id="f4857-140">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f4857-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="f4857-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f4857-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="f4857-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f4857-142">Update-AzContainerRegistry</span></span>]()

