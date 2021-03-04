---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 3054c6ed8083d1108c853ab188903cc3b2ebd380
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892203"
---
# <span data-ttu-id="55bc0-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="55bc0-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="55bc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="55bc0-103">Obtém uma replicação de um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="55bc0-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="55bc0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="55bc0-104">SYNTAX</span></span>

### <span data-ttu-id="55bc0-105">ListReplicationByNameResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="55bc0-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55bc0-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="55bc0-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55bc0-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55bc0-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55bc0-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55bc0-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55bc0-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55bc0-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55bc0-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="55bc0-110">DESCRIPTION</span></span>
<span data-ttu-id="55bc0-111">O Get-AzContainerRegistryReplication cmdlet obtém uma replicação especificada de um registro de contêiner ou todas as replicação de um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="55bc0-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="55bc0-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55bc0-112">EXAMPLES</span></span>

### <span data-ttu-id="55bc0-113">Exemplo 1: obtém uma replicação especificada de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="55bc0-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="55bc0-114">Obtém uma replicação especificada de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="55bc0-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="55bc0-115">Exemplo 2: obtém todas as replicaçãos de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="55bc0-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="55bc0-116">Obtém todas as replicação de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="55bc0-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="55bc0-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="55bc0-117">PARAMETERS</span></span>

### <span data-ttu-id="55bc0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55bc0-118">-DefaultProfile</span></span>
<span data-ttu-id="55bc0-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="55bc0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55bc0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="55bc0-120">-Name</span></span>
<span data-ttu-id="55bc0-121">Nome da replicação do Registro de Contêiner.</span><span class="sxs-lookup"><span data-stu-id="55bc0-121">Container Registry Replication Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowReplicationByNameResourceGroupParameterSet, ShowReplicationByRegistryObjectParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55bc0-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="55bc0-122">-Registry</span></span>
<span data-ttu-id="55bc0-123">Objeto Container Registry.</span><span class="sxs-lookup"><span data-stu-id="55bc0-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowReplicationByRegistryObjectParameterSet, ListReplicationByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55bc0-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="55bc0-124">-RegistryName</span></span>
<span data-ttu-id="55bc0-125">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="55bc0-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55bc0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55bc0-126">-ResourceGroupName</span></span>
<span data-ttu-id="55bc0-127">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="55bc0-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55bc0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55bc0-128">-ResourceId</span></span>
<span data-ttu-id="55bc0-129">A ID do recurso de replicação do registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="55bc0-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="55bc0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55bc0-130">CommonParameters</span></span>
<span data-ttu-id="55bc0-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55bc0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55bc0-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55bc0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55bc0-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55bc0-133">INPUTS</span></span>

### <span data-ttu-id="55bc0-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="55bc0-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="55bc0-135">System.String</span><span class="sxs-lookup"><span data-stu-id="55bc0-135">System.String</span></span>

## <span data-ttu-id="55bc0-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="55bc0-136">OUTPUTS</span></span>

### <span data-ttu-id="55bc0-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="55bc0-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="55bc0-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="55bc0-138">NOTES</span></span>

## <span data-ttu-id="55bc0-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55bc0-139">RELATED LINKS</span></span>

[<span data-ttu-id="55bc0-140">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="55bc0-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="55bc0-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="55bc0-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)