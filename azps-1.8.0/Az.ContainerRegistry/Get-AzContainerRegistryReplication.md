---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 21e821a4575fb918599ad2315c569a7f270e0a84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601183"
---
# <span data-ttu-id="cfeca-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cfeca-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="cfeca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cfeca-102">SYNOPSIS</span></span>
<span data-ttu-id="cfeca-103">Obtém uma replicação de um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="cfeca-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="cfeca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cfeca-104">SYNTAX</span></span>

### <span data-ttu-id="cfeca-105">ListReplicationByNameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cfeca-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfeca-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfeca-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfeca-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfeca-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfeca-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfeca-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cfeca-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfeca-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfeca-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cfeca-110">DESCRIPTION</span></span>
<span data-ttu-id="cfeca-111">O cmdlet Get-AzContainerRegistryReplication Obtém uma replicação especificada de um registro de contêiner ou todas as replicações de um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="cfeca-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="cfeca-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cfeca-112">EXAMPLES</span></span>

### <span data-ttu-id="cfeca-113">Exemplo 1: Obtém uma replicação especificada de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="cfeca-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="cfeca-114">Obtém uma replicação especificada de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="cfeca-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="cfeca-115">Exemplo 2: Obtém todas as replicações de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="cfeca-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="cfeca-116">Obtém todas as replicações de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="cfeca-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="cfeca-117">OS</span><span class="sxs-lookup"><span data-stu-id="cfeca-117">PARAMETERS</span></span>

### <span data-ttu-id="cfeca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfeca-118">-DefaultProfile</span></span>
<span data-ttu-id="cfeca-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cfeca-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfeca-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="cfeca-120">-Name</span></span>
<span data-ttu-id="cfeca-121">Nome de replicação do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="cfeca-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="cfeca-122">-Registro</span><span class="sxs-lookup"><span data-stu-id="cfeca-122">-Registry</span></span>
<span data-ttu-id="cfeca-123">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="cfeca-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="cfeca-124">-Registryname</span><span class="sxs-lookup"><span data-stu-id="cfeca-124">-RegistryName</span></span>
<span data-ttu-id="cfeca-125">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="cfeca-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="cfeca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfeca-126">-ResourceGroupName</span></span>
<span data-ttu-id="cfeca-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cfeca-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="cfeca-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfeca-128">-ResourceId</span></span>
<span data-ttu-id="cfeca-129">A ID do recurso de replicação do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="cfeca-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="cfeca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfeca-130">CommonParameters</span></span>
<span data-ttu-id="cfeca-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfeca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfeca-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfeca-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfeca-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cfeca-133">INPUTS</span></span>

### <span data-ttu-id="cfeca-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cfeca-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="cfeca-135">System. String</span><span class="sxs-lookup"><span data-stu-id="cfeca-135">System.String</span></span>

## <span data-ttu-id="cfeca-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cfeca-136">OUTPUTS</span></span>

### <span data-ttu-id="cfeca-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cfeca-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="cfeca-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cfeca-138">NOTES</span></span>

## <span data-ttu-id="cfeca-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cfeca-139">RELATED LINKS</span></span>

[<span data-ttu-id="cfeca-140">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cfeca-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="cfeca-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cfeca-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)