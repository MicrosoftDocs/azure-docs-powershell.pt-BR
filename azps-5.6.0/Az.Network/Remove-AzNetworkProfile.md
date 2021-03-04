---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 02a8fef51ca0689fb92d3990bf5bcc182f902549
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891128"
---
# <span data-ttu-id="9b158-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9b158-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="9b158-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b158-102">SYNOPSIS</span></span>
<span data-ttu-id="9b158-103">Remove um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="9b158-103">Removes a network profile.</span></span>

## <span data-ttu-id="9b158-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9b158-104">SYNTAX</span></span>

### <span data-ttu-id="9b158-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9b158-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b158-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b158-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b158-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b158-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b158-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9b158-108">DESCRIPTION</span></span>
<span data-ttu-id="9b158-109">O cmdlet **Remove-AzNetworkProfile** removerá um perfil de rede se nenhuma interface de rede de contêiner (como contrastada com uma configuração de **interface** de rede de contêiner ) tiver sido criada.</span><span class="sxs-lookup"><span data-stu-id="9b158-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration**) have been created.</span></span>

## <span data-ttu-id="9b158-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b158-110">EXAMPLES</span></span>

### <span data-ttu-id="9b158-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9b158-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="9b158-112">Isso remove o perfil de rede com o nome np1 do grupo de recursos rg1.</span><span class="sxs-lookup"><span data-stu-id="9b158-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="9b158-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9b158-113">PARAMETERS</span></span>

### <span data-ttu-id="9b158-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b158-114">-AsJob</span></span>
<span data-ttu-id="9b158-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9b158-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b158-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b158-116">-DefaultProfile</span></span>
<span data-ttu-id="9b158-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b158-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b158-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9b158-118">-Force</span></span>
<span data-ttu-id="9b158-119">Não peça confirmação se você deseja excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="9b158-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="9b158-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b158-120">-InputObject</span></span>
<span data-ttu-id="9b158-121">Objeto perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="9b158-121">Network profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b158-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9b158-122">-Name</span></span>
<span data-ttu-id="9b158-123">O nome do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="9b158-123">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b158-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b158-124">-PassThru</span></span>
<span data-ttu-id="9b158-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="9b158-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="9b158-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b158-126">-ResourceGroupName</span></span>
<span data-ttu-id="9b158-127">O nome do grupo de recursos do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="9b158-127">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b158-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b158-128">-ResourceId</span></span>
<span data-ttu-id="9b158-129">A ID de recurso do gerenciador de recursos do Azure do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="9b158-129">The Azure resource manager resource ID of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b158-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b158-130">-Confirm</span></span>
<span data-ttu-id="9b158-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b158-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b158-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b158-132">-WhatIf</span></span>
<span data-ttu-id="9b158-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b158-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b158-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b158-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b158-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b158-135">CommonParameters</span></span>
<span data-ttu-id="9b158-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b158-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b158-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b158-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b158-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b158-138">INPUTS</span></span>

### <span data-ttu-id="9b158-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9b158-139">System.String</span></span>

### <span data-ttu-id="9b158-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9b158-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="9b158-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9b158-141">OUTPUTS</span></span>

### <span data-ttu-id="9b158-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9b158-142">System.Boolean</span></span>

## <span data-ttu-id="9b158-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="9b158-143">NOTES</span></span>

## <span data-ttu-id="9b158-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b158-144">RELATED LINKS</span></span>

[<span data-ttu-id="9b158-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9b158-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="9b158-146">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9b158-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="9b158-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9b158-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
