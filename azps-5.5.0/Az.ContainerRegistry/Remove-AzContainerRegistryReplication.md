---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 41bdf9bbc33239590f9d3a6db4ffaa88ddf752a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116497"
---
# <span data-ttu-id="88aca-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="88aca-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="88aca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88aca-102">SYNOPSIS</span></span>
<span data-ttu-id="88aca-103">Remove uma replicação do registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="88aca-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="88aca-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88aca-104">SYNTAX</span></span>

### <span data-ttu-id="88aca-105">NameResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="88aca-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88aca-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88aca-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88aca-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88aca-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88aca-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="88aca-108">DESCRIPTION</span></span>
<span data-ttu-id="88aca-109">O Remove-AzContainerRegistryReplication cmdlet remove uma replicação do registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="88aca-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="88aca-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="88aca-110">EXAMPLES</span></span>

### <span data-ttu-id="88aca-111">Exemplo 1: remove uma replicação de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="88aca-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="88aca-112">Remove uma replicação do registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="88aca-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="88aca-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88aca-113">PARAMETERS</span></span>

### <span data-ttu-id="88aca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88aca-114">-DefaultProfile</span></span>
<span data-ttu-id="88aca-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="88aca-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88aca-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="88aca-116">-Name</span></span>
<span data-ttu-id="88aca-117">Nome de Replicação do Registro de Contêineres.</span><span class="sxs-lookup"><span data-stu-id="88aca-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="88aca-118">Padrão para o nome do local.</span><span class="sxs-lookup"><span data-stu-id="88aca-118">Default to the location name.</span></span>

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

### <span data-ttu-id="88aca-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88aca-119">-PassThru</span></span>
<span data-ttu-id="88aca-120">Indica que esse cmdlet retornará verdadeiro se a remoção tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="88aca-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="88aca-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="88aca-121">-RegistryName</span></span>
<span data-ttu-id="88aca-122">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="88aca-122">Container Registry Name.</span></span>

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

### <span data-ttu-id="88aca-123">-Replicação</span><span class="sxs-lookup"><span data-stu-id="88aca-123">-Replication</span></span>
<span data-ttu-id="88aca-124">Objeto do Registro de Contêineres.</span><span class="sxs-lookup"><span data-stu-id="88aca-124">Container Registry Object.</span></span>

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

### <span data-ttu-id="88aca-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88aca-125">-ResourceGroupName</span></span>
<span data-ttu-id="88aca-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="88aca-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="88aca-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88aca-127">-ResourceId</span></span>
<span data-ttu-id="88aca-128">A ID do recurso de replicação do registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="88aca-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="88aca-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="88aca-129">-Confirm</span></span>
<span data-ttu-id="88aca-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88aca-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88aca-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88aca-131">-WhatIf</span></span>
<span data-ttu-id="88aca-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="88aca-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88aca-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="88aca-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88aca-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88aca-134">CommonParameters</span></span>
<span data-ttu-id="88aca-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88aca-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88aca-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88aca-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88aca-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="88aca-137">INPUTS</span></span>

### <span data-ttu-id="88aca-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="88aca-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="88aca-139">System.String</span><span class="sxs-lookup"><span data-stu-id="88aca-139">System.String</span></span>

## <span data-ttu-id="88aca-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="88aca-140">OUTPUTS</span></span>

### <span data-ttu-id="88aca-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="88aca-141">System.Boolean</span></span>

## <span data-ttu-id="88aca-142">Notas</span><span class="sxs-lookup"><span data-stu-id="88aca-142">NOTES</span></span>

## <span data-ttu-id="88aca-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88aca-143">RELATED LINKS</span></span>

[<span data-ttu-id="88aca-144">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="88aca-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="88aca-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="88aca-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

