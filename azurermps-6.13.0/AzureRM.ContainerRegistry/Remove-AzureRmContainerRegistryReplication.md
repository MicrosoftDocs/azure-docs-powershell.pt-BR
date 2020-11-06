---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 7dfb080ae20c583467add8ce298b03199a4f89dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609817"
---
# <span data-ttu-id="c53ae-101">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c53ae-101">Remove-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="c53ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c53ae-102">SYNOPSIS</span></span>
<span data-ttu-id="c53ae-103">Remove a replicação do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c53ae-103">Removes a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c53ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c53ae-104">SYNTAX</span></span>

### <span data-ttu-id="c53ae-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c53ae-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c53ae-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c53ae-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c53ae-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c53ae-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c53ae-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c53ae-108">DESCRIPTION</span></span>
<span data-ttu-id="c53ae-109">O cmdlet Remove-AzureRmContainerRegistryReplication remove a replicação do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c53ae-109">The Remove-AzureRmContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="c53ae-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c53ae-110">EXAMPLES</span></span>

### <span data-ttu-id="c53ae-111">Exemplo 1: Remove uma replicação de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="c53ae-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="c53ae-112">Remove a replicação do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c53ae-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="c53ae-113">OS</span><span class="sxs-lookup"><span data-stu-id="c53ae-113">PARAMETERS</span></span>

### <span data-ttu-id="c53ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c53ae-114">-DefaultProfile</span></span>
<span data-ttu-id="c53ae-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c53ae-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c53ae-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c53ae-116">-Name</span></span>
<span data-ttu-id="c53ae-117">Nome de replicação do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c53ae-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="c53ae-118">Padrão para o nome do local.</span><span class="sxs-lookup"><span data-stu-id="c53ae-118">Default to the location name.</span></span>

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

### <span data-ttu-id="c53ae-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c53ae-119">-PassThru</span></span>
<span data-ttu-id="c53ae-120">Indica que esse cmdlet retorna true se a remoção tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c53ae-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="c53ae-121">-Registryname</span><span class="sxs-lookup"><span data-stu-id="c53ae-121">-RegistryName</span></span>
<span data-ttu-id="c53ae-122">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c53ae-122">Container Registry Name.</span></span>

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

### <span data-ttu-id="c53ae-123">-Replicatoin</span><span class="sxs-lookup"><span data-stu-id="c53ae-123">-Replicatoin</span></span>
<span data-ttu-id="c53ae-124">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c53ae-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c53ae-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c53ae-125">-ResourceGroupName</span></span>
<span data-ttu-id="c53ae-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c53ae-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="c53ae-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c53ae-127">-ResourceId</span></span>
<span data-ttu-id="c53ae-128">A ID do recurso de replicação do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="c53ae-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="c53ae-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c53ae-129">-Confirm</span></span>
<span data-ttu-id="c53ae-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c53ae-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c53ae-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c53ae-131">-WhatIf</span></span>
<span data-ttu-id="c53ae-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c53ae-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c53ae-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c53ae-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c53ae-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c53ae-134">CommonParameters</span></span>
<span data-ttu-id="c53ae-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c53ae-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c53ae-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c53ae-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c53ae-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c53ae-137">INPUTS</span></span>

### <span data-ttu-id="c53ae-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c53ae-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="c53ae-139">Parâmetros: Replicatoin (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c53ae-139">Parameters: Replicatoin (ByValue)</span></span>

### <span data-ttu-id="c53ae-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c53ae-140">System.String</span></span>

## <span data-ttu-id="c53ae-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c53ae-141">OUTPUTS</span></span>

### <span data-ttu-id="c53ae-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c53ae-142">System.Boolean</span></span>

## <span data-ttu-id="c53ae-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c53ae-143">NOTES</span></span>

## <span data-ttu-id="c53ae-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c53ae-144">RELATED LINKS</span></span>

[<span data-ttu-id="c53ae-145">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c53ae-145">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="c53ae-146">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c53ae-146">Get-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)

