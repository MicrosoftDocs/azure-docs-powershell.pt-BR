---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 57b482368834d91e36a3f557c9657c82cea24f4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777572"
---
# <span data-ttu-id="c2cbf-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c2cbf-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="c2cbf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2cbf-102">SYNOPSIS</span></span>
<span data-ttu-id="c2cbf-103">Obtém uma replicação de um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="c2cbf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2cbf-104">SYNTAX</span></span>

### <span data-ttu-id="c2cbf-105">ListReplicationByNameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c2cbf-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2cbf-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2cbf-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2cbf-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2cbf-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2cbf-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2cbf-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2cbf-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2cbf-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2cbf-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c2cbf-110">DESCRIPTION</span></span>
<span data-ttu-id="c2cbf-111">O cmdlet Get-AzContainerRegistryReplication Obtém uma replicação especificada de um registro de contêiner ou todas as replicações de um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="c2cbf-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2cbf-112">EXAMPLES</span></span>

### <span data-ttu-id="c2cbf-113">Exemplo 1: Obtém uma replicação especificada de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="c2cbf-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="c2cbf-114">Obtém uma replicação especificada de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="c2cbf-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="c2cbf-115">Exemplo 2: Obtém todas as replicações de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="c2cbf-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="c2cbf-116">Obtém todas as replicações de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="c2cbf-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="c2cbf-117">OS</span><span class="sxs-lookup"><span data-stu-id="c2cbf-117">PARAMETERS</span></span>

### <span data-ttu-id="c2cbf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2cbf-118">-DefaultProfile</span></span>
<span data-ttu-id="c2cbf-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2cbf-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2cbf-120">-Name</span></span>
<span data-ttu-id="c2cbf-121">Nome de replicação do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="c2cbf-122">-Registro</span><span class="sxs-lookup"><span data-stu-id="c2cbf-122">-Registry</span></span>
<span data-ttu-id="c2cbf-123">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="c2cbf-124">-Registryname</span><span class="sxs-lookup"><span data-stu-id="c2cbf-124">-RegistryName</span></span>
<span data-ttu-id="c2cbf-125">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="c2cbf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2cbf-126">-ResourceGroupName</span></span>
<span data-ttu-id="c2cbf-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="c2cbf-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2cbf-128">-ResourceId</span></span>
<span data-ttu-id="c2cbf-129">A ID do recurso de replicação do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="c2cbf-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="c2cbf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2cbf-130">CommonParameters</span></span>
<span data-ttu-id="c2cbf-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2cbf-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2cbf-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2cbf-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c2cbf-133">INPUTS</span></span>

### <span data-ttu-id="c2cbf-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c2cbf-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="c2cbf-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c2cbf-135">System.String</span></span>

## <span data-ttu-id="c2cbf-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c2cbf-136">OUTPUTS</span></span>

### <span data-ttu-id="c2cbf-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c2cbf-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="c2cbf-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c2cbf-138">NOTES</span></span>

## <span data-ttu-id="c2cbf-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2cbf-139">RELATED LINKS</span></span>

[<span data-ttu-id="c2cbf-140">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c2cbf-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="c2cbf-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c2cbf-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)