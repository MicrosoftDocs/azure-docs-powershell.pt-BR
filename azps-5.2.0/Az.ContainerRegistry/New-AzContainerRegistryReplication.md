---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: aadac0f7d408efd5f635d77d14f9afabfbd444d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259038"
---
# <span data-ttu-id="150fb-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="150fb-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="150fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="150fb-102">SYNOPSIS</span></span>
<span data-ttu-id="150fb-103">Cria uma replicação de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="150fb-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="150fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="150fb-104">SYNTAX</span></span>

### <span data-ttu-id="150fb-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="150fb-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="150fb-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="150fb-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="150fb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="150fb-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="150fb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="150fb-108">DESCRIPTION</span></span>
<span data-ttu-id="150fb-109">O cmdlet New-AzContainerRegistryReplication cria uma nova replicação de registro de contêineres.</span><span class="sxs-lookup"><span data-stu-id="150fb-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="150fb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="150fb-110">EXAMPLES</span></span>

### <span data-ttu-id="150fb-111">Exemplo 1: criar uma nova replicação de registro de contêineres.</span><span class="sxs-lookup"><span data-stu-id="150fb-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="150fb-112">Crie uma nova replicação de registro de contêineres.</span><span class="sxs-lookup"><span data-stu-id="150fb-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="150fb-113">OS</span><span class="sxs-lookup"><span data-stu-id="150fb-113">PARAMETERS</span></span>

### <span data-ttu-id="150fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="150fb-114">-DefaultProfile</span></span>
<span data-ttu-id="150fb-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="150fb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="150fb-116">-Local</span><span class="sxs-lookup"><span data-stu-id="150fb-116">-Location</span></span>
<span data-ttu-id="150fb-117">Local do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="150fb-117">Container Registry Location.</span></span>
<span data-ttu-id="150fb-118">Padrão para o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="150fb-118">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="150fb-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="150fb-119">-Name</span></span>
<span data-ttu-id="150fb-120">Nome de replicação do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="150fb-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="150fb-121">Padrão para o nome do local.</span><span class="sxs-lookup"><span data-stu-id="150fb-121">Default to the location name.</span></span>

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

### <span data-ttu-id="150fb-122">-Registro</span><span class="sxs-lookup"><span data-stu-id="150fb-122">-Registry</span></span>
<span data-ttu-id="150fb-123">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="150fb-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="150fb-124">-Registryname</span><span class="sxs-lookup"><span data-stu-id="150fb-124">-RegistryName</span></span>
<span data-ttu-id="150fb-125">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="150fb-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="150fb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="150fb-126">-ResourceGroupName</span></span>
<span data-ttu-id="150fb-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="150fb-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="150fb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="150fb-128">-ResourceId</span></span>
<span data-ttu-id="150fb-129">A ID do recurso do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="150fb-129">The container registry resource id</span></span>

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

### <span data-ttu-id="150fb-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="150fb-130">-Tag</span></span>
<span data-ttu-id="150fb-131">Marcas de registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="150fb-131">Container Registry Tags.</span></span>

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

### <span data-ttu-id="150fb-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="150fb-132">-Confirm</span></span>
<span data-ttu-id="150fb-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="150fb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="150fb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="150fb-134">-WhatIf</span></span>
<span data-ttu-id="150fb-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="150fb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="150fb-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="150fb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="150fb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="150fb-137">CommonParameters</span></span>
<span data-ttu-id="150fb-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="150fb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="150fb-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="150fb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="150fb-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="150fb-140">INPUTS</span></span>

### <span data-ttu-id="150fb-141">System. String</span><span class="sxs-lookup"><span data-stu-id="150fb-141">System.String</span></span>

## <span data-ttu-id="150fb-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="150fb-142">OUTPUTS</span></span>

### <span data-ttu-id="150fb-143">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="150fb-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="150fb-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="150fb-144">NOTES</span></span>

## <span data-ttu-id="150fb-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="150fb-145">RELATED LINKS</span></span>

[<span data-ttu-id="150fb-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="150fb-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="150fb-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="150fb-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)