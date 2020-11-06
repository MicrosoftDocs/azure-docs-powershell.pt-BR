---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 824b3226b29ba381b9ed963bf6a21f4691c17733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602740"
---
# <span data-ttu-id="4c336-101">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4c336-101">Remove-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="4c336-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c336-102">SYNOPSIS</span></span>
<span data-ttu-id="4c336-103">Remove a replicação do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="4c336-103">Removes a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c336-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c336-104">SYNTAX</span></span>

### <span data-ttu-id="4c336-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4c336-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c336-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c336-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c336-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c336-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c336-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4c336-108">DESCRIPTION</span></span>
<span data-ttu-id="4c336-109">O cmdlet Remove-AzureRmContainerRegistryReplication remove a replicação do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="4c336-109">The Remove-AzureRmContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="4c336-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c336-110">EXAMPLES</span></span>

### <span data-ttu-id="4c336-111">Exemplo 1: Remove uma replicação de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="4c336-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="4c336-112">Remove a replicação do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="4c336-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="4c336-113">OS</span><span class="sxs-lookup"><span data-stu-id="4c336-113">PARAMETERS</span></span>

### <span data-ttu-id="4c336-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4c336-114">-Confirm</span></span>
<span data-ttu-id="4c336-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c336-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c336-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c336-116">-DefaultProfile</span></span>
<span data-ttu-id="4c336-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c336-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c336-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c336-118">-Name</span></span>
<span data-ttu-id="4c336-119">Nome de replicação do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="4c336-119">Container Registry Replication Name.</span></span>
<span data-ttu-id="4c336-120">Padrão para o nome do local.</span><span class="sxs-lookup"><span data-stu-id="4c336-120">Default to the location name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c336-121">-Registryname</span><span class="sxs-lookup"><span data-stu-id="4c336-121">-RegistryName</span></span>
<span data-ttu-id="4c336-122">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="4c336-122">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c336-123">-Replicatoin</span><span class="sxs-lookup"><span data-stu-id="4c336-123">-Replicatoin</span></span>
<span data-ttu-id="4c336-124">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="4c336-124">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c336-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c336-125">-ResourceGroupName</span></span>
<span data-ttu-id="4c336-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4c336-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c336-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c336-127">-ResourceId</span></span>
<span data-ttu-id="4c336-128">A ID do recurso de replicação do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="4c336-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="4c336-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c336-129">-WhatIf</span></span>
<span data-ttu-id="4c336-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4c336-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c336-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c336-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c336-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c336-132">-PassThru</span></span>
<span data-ttu-id="4c336-133">Indica que esse cmdlet retorna true se a remoção tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4c336-133">Indicates that this cmdlet returns true if the removal was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c336-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c336-134">CommonParameters</span></span>
<span data-ttu-id="4c336-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c336-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c336-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c336-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c336-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4c336-137">INPUTS</span></span>

### <span data-ttu-id="4c336-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4c336-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="4c336-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4c336-139">System.String</span></span>

## <span data-ttu-id="4c336-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4c336-140">OUTPUTS</span></span>

### <span data-ttu-id="4c336-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="4c336-141">System.Object</span></span>

## <span data-ttu-id="4c336-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4c336-142">NOTES</span></span>

## <span data-ttu-id="4c336-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c336-143">RELATED LINKS</span></span>

[<span data-ttu-id="4c336-144">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4c336-144">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="4c336-145">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4c336-145">Get-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)

