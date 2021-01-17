---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 3a83b7200f7634574fd457d2fa08f926a62b9a82
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428896"
---
# <span data-ttu-id="70c7d-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="70c7d-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="70c7d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="70c7d-103">Remove um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="70c7d-103">Removes a network profile.</span></span>

## <span data-ttu-id="70c7d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70c7d-104">SYNTAX</span></span>

### <span data-ttu-id="70c7d-105">RemoveByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="70c7d-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70c7d-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70c7d-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70c7d-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70c7d-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70c7d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="70c7d-108">DESCRIPTION</span></span>
<span data-ttu-id="70c7d-109">O cmdlet **Remove-AzNetworkProfile** remove um perfil de rede se não for criada nenhuma interface de rede de contêiner (conforme o contraste com uma **configuração** de interface de rede de contêiner).</span><span class="sxs-lookup"><span data-stu-id="70c7d-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration**) have been created.</span></span>

## <span data-ttu-id="70c7d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70c7d-110">EXAMPLES</span></span>

### <span data-ttu-id="70c7d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="70c7d-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="70c7d-112">Isso remove o perfil de rede com o nome NP1 da Rg1 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="70c7d-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="70c7d-113">OS</span><span class="sxs-lookup"><span data-stu-id="70c7d-113">PARAMETERS</span></span>

### <span data-ttu-id="70c7d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70c7d-114">-AsJob</span></span>
<span data-ttu-id="70c7d-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="70c7d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70c7d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c7d-116">-DefaultProfile</span></span>
<span data-ttu-id="70c7d-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="70c7d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70c7d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="70c7d-118">-Force</span></span>
<span data-ttu-id="70c7d-119">Não pedir confirmação se quiser excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="70c7d-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="70c7d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70c7d-120">-InputObject</span></span>
<span data-ttu-id="70c7d-121">Objeto de perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="70c7d-121">Network profile object.</span></span>

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

### <span data-ttu-id="70c7d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="70c7d-122">-Name</span></span>
<span data-ttu-id="70c7d-123">O nome do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="70c7d-123">The name of the network profile.</span></span>

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

### <span data-ttu-id="70c7d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70c7d-124">-PassThru</span></span>
<span data-ttu-id="70c7d-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="70c7d-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="70c7d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70c7d-126">-ResourceGroupName</span></span>
<span data-ttu-id="70c7d-127">O nome do grupo de recursos do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="70c7d-127">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="70c7d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70c7d-128">-ResourceId</span></span>
<span data-ttu-id="70c7d-129">A ID do recurso do Gerenciador de recursos do Azure do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="70c7d-129">The Azure resource manager resource ID of the network profile.</span></span>

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

### <span data-ttu-id="70c7d-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="70c7d-130">-Confirm</span></span>
<span data-ttu-id="70c7d-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70c7d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70c7d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70c7d-132">-WhatIf</span></span>
<span data-ttu-id="70c7d-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="70c7d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70c7d-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="70c7d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70c7d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c7d-135">CommonParameters</span></span>
<span data-ttu-id="70c7d-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70c7d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c7d-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70c7d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c7d-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="70c7d-138">INPUTS</span></span>

### <span data-ttu-id="70c7d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="70c7d-139">System.String</span></span>

### <span data-ttu-id="70c7d-140">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="70c7d-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="70c7d-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="70c7d-141">OUTPUTS</span></span>

### <span data-ttu-id="70c7d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="70c7d-142">System.Boolean</span></span>

## <span data-ttu-id="70c7d-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="70c7d-143">NOTES</span></span>

## <span data-ttu-id="70c7d-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70c7d-144">RELATED LINKS</span></span>

[<span data-ttu-id="70c7d-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="70c7d-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="70c7d-146">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="70c7d-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="70c7d-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="70c7d-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
