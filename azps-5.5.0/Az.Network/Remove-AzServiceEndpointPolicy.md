---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 207a07186cd7284059e0824da1f86afbc22873f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113449"
---
# <span data-ttu-id="2822d-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2822d-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="2822d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2822d-102">SYNOPSIS</span></span>
<span data-ttu-id="2822d-103">Remove uma política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="2822d-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="2822d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2822d-104">SYNTAX</span></span>

### <span data-ttu-id="2822d-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2822d-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2822d-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2822d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2822d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2822d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2822d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2822d-108">DESCRIPTION</span></span>
<span data-ttu-id="2822d-109">O cmdlet **Remove-AzServiceEndpointPolicy** remove uma política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="2822d-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="2822d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2822d-110">EXAMPLES</span></span>

### <span data-ttu-id="2822d-111">Exemplo 1: remove uma política de ponto de extremidade de serviço usando o nome</span><span class="sxs-lookup"><span data-stu-id="2822d-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="2822d-112">Esse comando remove uma política de ponto de extremidade de serviço com o nome Política1 que pertence ao grupo de recursos com o nome "resourcegroup1"</span><span class="sxs-lookup"><span data-stu-id="2822d-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="2822d-113">Exemplo 2: Remover uma política de ponto de extremidade de serviço usando o objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="2822d-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="2822d-114">Esse comando remove uma Política de objeto de política de ponto de extremidade de serviço1 que pertence ao grupo de recursos com o nome "resourcegroup1"</span><span class="sxs-lookup"><span data-stu-id="2822d-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="2822d-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2822d-115">PARAMETERS</span></span>

### <span data-ttu-id="2822d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2822d-116">-DefaultProfile</span></span>
<span data-ttu-id="2822d-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2822d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2822d-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="2822d-118">-Force</span></span>
<span data-ttu-id="2822d-119">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="2822d-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2822d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2822d-120">-InputObject</span></span>
<span data-ttu-id="2822d-121">O objeto de política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="2822d-121">The service endpoint policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2822d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2822d-122">-Name</span></span>
<span data-ttu-id="2822d-123">O nome da política de ponto de extremidade de serviço</span><span class="sxs-lookup"><span data-stu-id="2822d-123">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="2822d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2822d-124">-PassThru</span></span>
<span data-ttu-id="2822d-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="2822d-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="2822d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2822d-126">-ResourceGroupName</span></span>
<span data-ttu-id="2822d-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2822d-127">The resource group name.</span></span>

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

### <span data-ttu-id="2822d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2822d-128">-ResourceId</span></span>
<span data-ttu-id="2822d-129">A ID da política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="2822d-129">The ID of service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2822d-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2822d-130">-Confirm</span></span>
<span data-ttu-id="2822d-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2822d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2822d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2822d-132">-WhatIf</span></span>
<span data-ttu-id="2822d-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2822d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2822d-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2822d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2822d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2822d-135">CommonParameters</span></span>
<span data-ttu-id="2822d-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2822d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2822d-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2822d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2822d-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="2822d-138">INPUTS</span></span>

### <span data-ttu-id="2822d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2822d-139">System.String</span></span>

### <span data-ttu-id="2822d-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2822d-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="2822d-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="2822d-141">OUTPUTS</span></span>

### <span data-ttu-id="2822d-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2822d-142">System.Boolean</span></span>

## <span data-ttu-id="2822d-143">Notas</span><span class="sxs-lookup"><span data-stu-id="2822d-143">NOTES</span></span>

## <span data-ttu-id="2822d-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2822d-144">RELATED LINKS</span></span>

[<span data-ttu-id="2822d-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2822d-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="2822d-146">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2822d-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="2822d-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2822d-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
