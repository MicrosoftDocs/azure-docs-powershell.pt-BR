---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 3a83b7200f7634574fd457d2fa08f926a62b9a82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118283"
---
# <span data-ttu-id="b2b3a-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b2b3a-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="b2b3a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="b2b3a-103">Remove um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="b2b3a-103">Removes a network profile.</span></span>

## <span data-ttu-id="b2b3a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2b3a-104">SYNTAX</span></span>

### <span data-ttu-id="b2b3a-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b2b3a-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2b3a-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2b3a-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2b3a-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2b3a-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2b3a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2b3a-108">DESCRIPTION</span></span>
<span data-ttu-id="b2b3a-109">O cmdlet **Remove-AzNetworkProfile** removerá um perfil de rede se nenhuma interface de rede de contêiner (contrastada com uma configuração de **interface** de rede de contêiner) tiver sido criada.</span><span class="sxs-lookup"><span data-stu-id="b2b3a-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration**) have been created.</span></span>

## <span data-ttu-id="b2b3a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b2b3a-110">EXAMPLES</span></span>

### <span data-ttu-id="b2b3a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b2b3a-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="b2b3a-112">Isso remove o perfil da rede com o nome np1 do grupo de recursos rg1.</span><span class="sxs-lookup"><span data-stu-id="b2b3a-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="b2b3a-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2b3a-113">PARAMETERS</span></span>

### <span data-ttu-id="b2b3a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2b3a-114">-AsJob</span></span>
<span data-ttu-id="b2b3a-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b2b3a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2b3a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2b3a-116">-DefaultProfile</span></span>
<span data-ttu-id="b2b3a-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2b3a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2b3a-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="b2b3a-118">-Force</span></span>
<span data-ttu-id="b2b3a-119">Não peça confirmação se quiser excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="b2b3a-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="b2b3a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2b3a-120">-InputObject</span></span>
<span data-ttu-id="b2b3a-121">Objeto de perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="b2b3a-121">Network profile object.</span></span>

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

### <span data-ttu-id="b2b3a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2b3a-122">-Name</span></span>
<span data-ttu-id="b2b3a-123">O nome do perfil da rede.</span><span class="sxs-lookup"><span data-stu-id="b2b3a-123">The name of the network profile.</span></span>

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

### <span data-ttu-id="b2b3a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2b3a-124">-PassThru</span></span>
<span data-ttu-id="b2b3a-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="b2b3a-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="b2b3a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2b3a-126">-ResourceGroupName</span></span>
<span data-ttu-id="b2b3a-127">O nome do grupo de recursos do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="b2b3a-127">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="b2b3a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2b3a-128">-ResourceId</span></span>
<span data-ttu-id="b2b3a-129">A ID de recurso do gerenciador de recursos do Azure do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="b2b3a-129">The Azure resource manager resource ID of the network profile.</span></span>

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

### <span data-ttu-id="b2b3a-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b2b3a-130">-Confirm</span></span>
<span data-ttu-id="b2b3a-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2b3a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2b3a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2b3a-132">-WhatIf</span></span>
<span data-ttu-id="b2b3a-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b2b3a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2b3a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2b3a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2b3a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2b3a-135">CommonParameters</span></span>
<span data-ttu-id="b2b3a-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2b3a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2b3a-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2b3a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2b3a-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="b2b3a-138">INPUTS</span></span>

### <span data-ttu-id="b2b3a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b2b3a-139">System.String</span></span>

### <span data-ttu-id="b2b3a-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b2b3a-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="b2b3a-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="b2b3a-141">OUTPUTS</span></span>

### <span data-ttu-id="b2b3a-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b2b3a-142">System.Boolean</span></span>

## <span data-ttu-id="b2b3a-143">Notas</span><span class="sxs-lookup"><span data-stu-id="b2b3a-143">NOTES</span></span>

## <span data-ttu-id="b2b3a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2b3a-144">RELATED LINKS</span></span>

[<span data-ttu-id="b2b3a-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b2b3a-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="b2b3a-146">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b2b3a-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="b2b3a-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b2b3a-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
