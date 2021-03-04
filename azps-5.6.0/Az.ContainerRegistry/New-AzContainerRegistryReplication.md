---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: a446fe34ba29789e93e8907d3155af654a93ff21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891053"
---
# <span data-ttu-id="b6466-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b6466-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="b6466-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6466-102">SYNOPSIS</span></span>
<span data-ttu-id="b6466-103">Cria uma replicação de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="b6466-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="b6466-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b6466-104">SYNTAX</span></span>

### <span data-ttu-id="b6466-105">NameResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b6466-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6466-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6466-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6466-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6466-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6466-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b6466-108">DESCRIPTION</span></span>
<span data-ttu-id="b6466-109">O New-AzContainerRegistryReplication cmdlet cria uma nova replicação de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="b6466-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="b6466-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6466-110">EXAMPLES</span></span>

### <span data-ttu-id="b6466-111">Exemplo 1: Criar uma nova replicação de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="b6466-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="b6466-112">Crie uma nova replicação de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="b6466-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="b6466-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b6466-113">PARAMETERS</span></span>

### <span data-ttu-id="b6466-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6466-114">-DefaultProfile</span></span>
<span data-ttu-id="b6466-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b6466-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6466-116">-Location</span><span class="sxs-lookup"><span data-stu-id="b6466-116">-Location</span></span>
<span data-ttu-id="b6466-117">Local do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="b6466-117">Container Registry Location.</span></span>
<span data-ttu-id="b6466-118">Padrão para o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b6466-118">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6466-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b6466-119">-Name</span></span>
<span data-ttu-id="b6466-120">Nome da replicação do Registro de Contêiner.</span><span class="sxs-lookup"><span data-stu-id="b6466-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="b6466-121">Padrão para o nome do local.</span><span class="sxs-lookup"><span data-stu-id="b6466-121">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6466-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="b6466-122">-Registry</span></span>
<span data-ttu-id="b6466-123">Objeto Container Registry.</span><span class="sxs-lookup"><span data-stu-id="b6466-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="b6466-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="b6466-124">-RegistryName</span></span>
<span data-ttu-id="b6466-125">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="b6466-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6466-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6466-126">-ResourceGroupName</span></span>
<span data-ttu-id="b6466-127">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="b6466-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="b6466-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6466-128">-ResourceId</span></span>
<span data-ttu-id="b6466-129">A ID de recurso do Registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="b6466-129">The container registry resource id</span></span>

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

### <span data-ttu-id="b6466-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6466-130">-Tag</span></span>
<span data-ttu-id="b6466-131">Marcas de Registro de Contêiner.</span><span class="sxs-lookup"><span data-stu-id="b6466-131">Container Registry Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6466-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6466-132">-Confirm</span></span>
<span data-ttu-id="b6466-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6466-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6466-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6466-134">-WhatIf</span></span>
<span data-ttu-id="b6466-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b6466-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6466-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6466-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6466-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6466-137">CommonParameters</span></span>
<span data-ttu-id="b6466-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6466-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6466-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6466-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6466-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6466-140">INPUTS</span></span>

### <span data-ttu-id="b6466-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b6466-141">System.String</span></span>

## <span data-ttu-id="b6466-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b6466-142">OUTPUTS</span></span>

### <span data-ttu-id="b6466-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b6466-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="b6466-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="b6466-144">NOTES</span></span>

## <span data-ttu-id="b6466-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6466-145">RELATED LINKS</span></span>

[<span data-ttu-id="b6466-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b6466-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="b6466-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b6466-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)