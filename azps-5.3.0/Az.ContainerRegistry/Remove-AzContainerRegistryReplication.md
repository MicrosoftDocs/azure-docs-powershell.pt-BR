---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 41bdf9bbc33239590f9d3a6db4ffaa88ddf752a1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430105"
---
# <span data-ttu-id="7e128-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="7e128-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="7e128-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e128-102">SYNOPSIS</span></span>
<span data-ttu-id="7e128-103">Remove a replicação do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7e128-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="7e128-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e128-104">SYNTAX</span></span>

### <span data-ttu-id="7e128-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7e128-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e128-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e128-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e128-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e128-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e128-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e128-108">DESCRIPTION</span></span>
<span data-ttu-id="7e128-109">O cmdlet Remove-AzContainerRegistryReplication remove a replicação do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7e128-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="7e128-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e128-110">EXAMPLES</span></span>

### <span data-ttu-id="7e128-111">Exemplo 1: Remove uma replicação de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="7e128-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="7e128-112">Remove a replicação do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7e128-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="7e128-113">OS</span><span class="sxs-lookup"><span data-stu-id="7e128-113">PARAMETERS</span></span>

### <span data-ttu-id="7e128-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e128-114">-DefaultProfile</span></span>
<span data-ttu-id="7e128-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e128-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e128-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e128-116">-Name</span></span>
<span data-ttu-id="7e128-117">Nome de replicação do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7e128-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="7e128-118">Padrão para o nome do local.</span><span class="sxs-lookup"><span data-stu-id="7e128-118">Default to the location name.</span></span>

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

### <span data-ttu-id="7e128-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e128-119">-PassThru</span></span>
<span data-ttu-id="7e128-120">Indica que esse cmdlet retorna true se a remoção tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7e128-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="7e128-121">-Registryname</span><span class="sxs-lookup"><span data-stu-id="7e128-121">-RegistryName</span></span>
<span data-ttu-id="7e128-122">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7e128-122">Container Registry Name.</span></span>

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

### <span data-ttu-id="7e128-123">-Replicação</span><span class="sxs-lookup"><span data-stu-id="7e128-123">-Replication</span></span>
<span data-ttu-id="7e128-124">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7e128-124">Container Registry Object.</span></span>

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

### <span data-ttu-id="7e128-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e128-125">-ResourceGroupName</span></span>
<span data-ttu-id="7e128-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7e128-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="7e128-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e128-127">-ResourceId</span></span>
<span data-ttu-id="7e128-128">A ID do recurso de replicação do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="7e128-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="7e128-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7e128-129">-Confirm</span></span>
<span data-ttu-id="7e128-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e128-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e128-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e128-131">-WhatIf</span></span>
<span data-ttu-id="7e128-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7e128-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e128-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7e128-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e128-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e128-134">CommonParameters</span></span>
<span data-ttu-id="7e128-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e128-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e128-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e128-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e128-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e128-137">INPUTS</span></span>

### <span data-ttu-id="7e128-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="7e128-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="7e128-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7e128-139">System.String</span></span>

## <span data-ttu-id="7e128-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e128-140">OUTPUTS</span></span>

### <span data-ttu-id="7e128-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e128-141">System.Boolean</span></span>

## <span data-ttu-id="7e128-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e128-142">NOTES</span></span>

## <span data-ttu-id="7e128-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e128-143">RELATED LINKS</span></span>

[<span data-ttu-id="7e128-144">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="7e128-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="7e128-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="7e128-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

