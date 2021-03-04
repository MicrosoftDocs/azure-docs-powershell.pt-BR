---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 3fff7a0952f4ace41f76237a8fbf226e9bb58128
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901498"
---
# <span data-ttu-id="73a35-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="73a35-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="73a35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73a35-102">SYNOPSIS</span></span>
<span data-ttu-id="73a35-103">Remove uma replicação de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="73a35-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="73a35-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="73a35-104">SYNTAX</span></span>

### <span data-ttu-id="73a35-105">NameResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="73a35-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73a35-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73a35-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73a35-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73a35-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73a35-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="73a35-108">DESCRIPTION</span></span>
<span data-ttu-id="73a35-109">O Remove-AzContainerRegistryReplication cmdlet remove uma replicação de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="73a35-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="73a35-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73a35-110">EXAMPLES</span></span>

### <span data-ttu-id="73a35-111">Exemplo 1: remove uma replicação de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="73a35-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="73a35-112">Remove uma replicação de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="73a35-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="73a35-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="73a35-113">PARAMETERS</span></span>

### <span data-ttu-id="73a35-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73a35-114">-DefaultProfile</span></span>
<span data-ttu-id="73a35-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="73a35-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73a35-116">-Name</span><span class="sxs-lookup"><span data-stu-id="73a35-116">-Name</span></span>
<span data-ttu-id="73a35-117">Nome da replicação do Registro de Contêiner.</span><span class="sxs-lookup"><span data-stu-id="73a35-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="73a35-118">Padrão para o nome do local.</span><span class="sxs-lookup"><span data-stu-id="73a35-118">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73a35-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73a35-119">-PassThru</span></span>
<span data-ttu-id="73a35-120">Indica que esse cmdlet retornará true se a remoção tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="73a35-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="73a35-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="73a35-121">-RegistryName</span></span>
<span data-ttu-id="73a35-122">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="73a35-122">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73a35-123">-Replication</span><span class="sxs-lookup"><span data-stu-id="73a35-123">-Replication</span></span>
<span data-ttu-id="73a35-124">Objeto Container Registry.</span><span class="sxs-lookup"><span data-stu-id="73a35-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: Replicatoin

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73a35-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73a35-125">-ResourceGroupName</span></span>
<span data-ttu-id="73a35-126">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="73a35-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73a35-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73a35-127">-ResourceId</span></span>
<span data-ttu-id="73a35-128">A ID do recurso de replicação do registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="73a35-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="73a35-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73a35-129">-Confirm</span></span>
<span data-ttu-id="73a35-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73a35-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73a35-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73a35-131">-WhatIf</span></span>
<span data-ttu-id="73a35-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="73a35-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73a35-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="73a35-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73a35-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73a35-134">CommonParameters</span></span>
<span data-ttu-id="73a35-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73a35-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73a35-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73a35-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73a35-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73a35-137">INPUTS</span></span>

### <span data-ttu-id="73a35-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="73a35-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="73a35-139">System.String</span><span class="sxs-lookup"><span data-stu-id="73a35-139">System.String</span></span>

## <span data-ttu-id="73a35-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="73a35-140">OUTPUTS</span></span>

### <span data-ttu-id="73a35-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="73a35-141">System.Boolean</span></span>

## <span data-ttu-id="73a35-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="73a35-142">NOTES</span></span>

## <span data-ttu-id="73a35-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73a35-143">RELATED LINKS</span></span>

[<span data-ttu-id="73a35-144">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="73a35-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="73a35-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="73a35-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

