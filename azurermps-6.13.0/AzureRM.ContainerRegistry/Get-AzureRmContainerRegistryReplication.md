---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: d2cac696382f807a1fc4afe94f9d2d61ea65cece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93601977"
---
# <span data-ttu-id="25f3d-101">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="25f3d-101">Get-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="25f3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="25f3d-103">Obtém uma replicação de um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="25f3d-103">Gets a replication of a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25f3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25f3d-104">SYNTAX</span></span>

### <span data-ttu-id="25f3d-105">ListReplicationByNameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="25f3d-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25f3d-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="25f3d-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25f3d-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25f3d-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25f3d-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25f3d-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25f3d-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25f3d-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25f3d-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25f3d-110">DESCRIPTION</span></span>
<span data-ttu-id="25f3d-111">O cmdlet Get-AzureRmContainerRegistryReplication Obtém uma replicação especificada de um registro de contêiner ou todas as replicações de um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="25f3d-111">The Get-AzureRmContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="25f3d-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25f3d-112">EXAMPLES</span></span>

### <span data-ttu-id="25f3d-113">Exemplo 1: Obtém uma replicação especificada de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="25f3d-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="25f3d-114">Obtém uma replicação especificada de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="25f3d-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="25f3d-115">Exemplo 2: Obtém todas as replicações de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="25f3d-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="25f3d-116">Obtém todas as replicações de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="25f3d-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="25f3d-117">OS</span><span class="sxs-lookup"><span data-stu-id="25f3d-117">PARAMETERS</span></span>

### <span data-ttu-id="25f3d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25f3d-118">-DefaultProfile</span></span>
<span data-ttu-id="25f3d-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25f3d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f3d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="25f3d-120">-Name</span></span>
<span data-ttu-id="25f3d-121">Nome de replicação do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="25f3d-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="25f3d-122">-Registro</span><span class="sxs-lookup"><span data-stu-id="25f3d-122">-Registry</span></span>
<span data-ttu-id="25f3d-123">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="25f3d-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="25f3d-124">-Registryname</span><span class="sxs-lookup"><span data-stu-id="25f3d-124">-RegistryName</span></span>
<span data-ttu-id="25f3d-125">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="25f3d-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="25f3d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25f3d-126">-ResourceGroupName</span></span>
<span data-ttu-id="25f3d-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="25f3d-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="25f3d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25f3d-128">-ResourceId</span></span>
<span data-ttu-id="25f3d-129">A ID do recurso de replicação do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="25f3d-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="25f3d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25f3d-130">CommonParameters</span></span>
<span data-ttu-id="25f3d-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25f3d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25f3d-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25f3d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25f3d-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25f3d-133">INPUTS</span></span>

### <span data-ttu-id="25f3d-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="25f3d-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="25f3d-135">Parâmetros: Registry (ByValue)</span><span class="sxs-lookup"><span data-stu-id="25f3d-135">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="25f3d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="25f3d-136">System.String</span></span>

## <span data-ttu-id="25f3d-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25f3d-137">OUTPUTS</span></span>

### <span data-ttu-id="25f3d-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="25f3d-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="25f3d-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25f3d-139">NOTES</span></span>

## <span data-ttu-id="25f3d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25f3d-140">RELATED LINKS</span></span>

[<span data-ttu-id="25f3d-141">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="25f3d-141">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="25f3d-142">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="25f3d-142">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
