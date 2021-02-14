---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 57b482368834d91e36a3f557c9657c82cea24f4e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111050"
---
# <span data-ttu-id="ebb07-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ebb07-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="ebb07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ebb07-102">SYNOPSIS</span></span>
<span data-ttu-id="ebb07-103">Obtém uma replicação de um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="ebb07-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="ebb07-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ebb07-104">SYNTAX</span></span>

### <span data-ttu-id="ebb07-105">ListReplicationByNameResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ebb07-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebb07-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebb07-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebb07-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebb07-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebb07-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebb07-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ebb07-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebb07-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ebb07-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ebb07-110">DESCRIPTION</span></span>
<span data-ttu-id="ebb07-111">O Get-AzContainerRegistryReplication cmdlet obtém uma replicação especificada de um registro de contêiner ou todas as replicaçãos de um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="ebb07-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="ebb07-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ebb07-112">EXAMPLES</span></span>

### <span data-ttu-id="ebb07-113">Exemplo 1: obtém uma replicação especificada de um registro de contêineres</span><span class="sxs-lookup"><span data-stu-id="ebb07-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="ebb07-114">Obtém uma replicação especificada de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="ebb07-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="ebb07-115">Exemplo 2: Obtém todas as replicaçãos de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="ebb07-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="ebb07-116">Obtém todas as replicaçãos de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="ebb07-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="ebb07-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebb07-117">PARAMETERS</span></span>

### <span data-ttu-id="ebb07-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebb07-118">-DefaultProfile</span></span>
<span data-ttu-id="ebb07-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ebb07-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebb07-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ebb07-120">-Name</span></span>
<span data-ttu-id="ebb07-121">Nome de Replicação do Registro de Contêineres.</span><span class="sxs-lookup"><span data-stu-id="ebb07-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="ebb07-122">-Registro</span><span class="sxs-lookup"><span data-stu-id="ebb07-122">-Registry</span></span>
<span data-ttu-id="ebb07-123">Objeto do Registro de Contêineres.</span><span class="sxs-lookup"><span data-stu-id="ebb07-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="ebb07-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="ebb07-124">-RegistryName</span></span>
<span data-ttu-id="ebb07-125">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="ebb07-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="ebb07-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebb07-126">-ResourceGroupName</span></span>
<span data-ttu-id="ebb07-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ebb07-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="ebb07-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebb07-128">-ResourceId</span></span>
<span data-ttu-id="ebb07-129">A ID do recurso de replicação do registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="ebb07-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="ebb07-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebb07-130">CommonParameters</span></span>
<span data-ttu-id="ebb07-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebb07-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebb07-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ebb07-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebb07-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="ebb07-133">INPUTS</span></span>

### <span data-ttu-id="ebb07-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ebb07-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="ebb07-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ebb07-135">System.String</span></span>

## <span data-ttu-id="ebb07-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="ebb07-136">OUTPUTS</span></span>

### <span data-ttu-id="ebb07-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ebb07-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="ebb07-138">Notas</span><span class="sxs-lookup"><span data-stu-id="ebb07-138">NOTES</span></span>

## <span data-ttu-id="ebb07-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ebb07-139">RELATED LINKS</span></span>

[<span data-ttu-id="ebb07-140">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ebb07-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="ebb07-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ebb07-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)