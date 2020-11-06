---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: db03414e9cebe4c1593013a928b8a66d9b70bd91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428967"
---
# <span data-ttu-id="73279-101">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="73279-101">Get-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="73279-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73279-102">SYNOPSIS</span></span>
<span data-ttu-id="73279-103">Obtém uma replicação de um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="73279-103">Gets a replication of a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73279-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73279-104">SYNTAX</span></span>

### <span data-ttu-id="73279-105">ListReplicationByNameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="73279-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73279-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="73279-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73279-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73279-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73279-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73279-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73279-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73279-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73279-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="73279-110">DESCRIPTION</span></span>
<span data-ttu-id="73279-111">O cmdlet Get-AzureRmContainerRegistryReplication Obtém uma replicação especificada de um registro de contêiner ou todas as replicações de um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="73279-111">The Get-AzureRmContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="73279-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73279-112">EXAMPLES</span></span>

### <span data-ttu-id="73279-113">Exemplo 1: Obtém uma replicação especificada de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="73279-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="73279-114">Obtém uma replicação especificada de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="73279-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="73279-115">Exemplo 2: Obtém todas as replicações de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="73279-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="73279-116">Obtém todas as replicações de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="73279-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="73279-117">OS</span><span class="sxs-lookup"><span data-stu-id="73279-117">PARAMETERS</span></span>

### <span data-ttu-id="73279-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73279-118">-DefaultProfile</span></span>
<span data-ttu-id="73279-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73279-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73279-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="73279-120">-Name</span></span>
<span data-ttu-id="73279-121">Nome de replicação do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="73279-121">Container Registry Replication Name.</span></span>

```yaml
Type: String
Parameter Sets: ShowReplicationByNameResourceGroupParameterSet, ShowReplicationByRegistryObjectParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73279-122">-Registro</span><span class="sxs-lookup"><span data-stu-id="73279-122">-Registry</span></span>
<span data-ttu-id="73279-123">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="73279-123">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: ShowReplicationByRegistryObjectParameterSet, ListReplicationByRegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73279-124">-Registryname</span><span class="sxs-lookup"><span data-stu-id="73279-124">-RegistryName</span></span>
<span data-ttu-id="73279-125">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="73279-125">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73279-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73279-126">-ResourceGroupName</span></span>
<span data-ttu-id="73279-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="73279-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73279-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73279-128">-ResourceId</span></span>
<span data-ttu-id="73279-129">A ID do recurso de replicação do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="73279-129">The container registry replication resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73279-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73279-130">CommonParameters</span></span>
<span data-ttu-id="73279-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73279-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73279-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73279-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73279-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="73279-133">INPUTS</span></span>

### <span data-ttu-id="73279-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="73279-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="73279-135">System. String</span><span class="sxs-lookup"><span data-stu-id="73279-135">System.String</span></span>

## <span data-ttu-id="73279-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="73279-136">OUTPUTS</span></span>

### <span data-ttu-id="73279-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="73279-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="73279-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication []</span><span class="sxs-lookup"><span data-stu-id="73279-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication[]</span></span>

## <span data-ttu-id="73279-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="73279-139">NOTES</span></span>

## <span data-ttu-id="73279-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73279-140">RELATED LINKS</span></span>

[<span data-ttu-id="73279-141">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="73279-141">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="73279-142">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="73279-142">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
