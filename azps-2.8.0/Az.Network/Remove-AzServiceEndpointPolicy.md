---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: fbe09b0ce6ad997ee914bf515aeb78f3fcee7971
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772252"
---
# <span data-ttu-id="b040e-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b040e-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="b040e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b040e-102">SYNOPSIS</span></span>
<span data-ttu-id="b040e-103">Remove uma política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="b040e-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="b040e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b040e-104">SYNTAX</span></span>

### <span data-ttu-id="b040e-105">RemoveByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b040e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b040e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b040e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b040e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b040e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b040e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b040e-108">DESCRIPTION</span></span>
<span data-ttu-id="b040e-109">O cmdlet **Remove-AzServiceEndpointPolicy** remove uma política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b040e-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="b040e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b040e-110">EXAMPLES</span></span>

### <span data-ttu-id="b040e-111">Exemplo 1: Remove uma política de ponto de extremidade do serviço usando Name</span><span class="sxs-lookup"><span data-stu-id="b040e-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="b040e-112">Esse comando Remove uma política de ponto de extremidade de serviço com o nome Policy1 que pertence a um MySource com o nome "resourcegroup1"</span><span class="sxs-lookup"><span data-stu-id="b040e-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="b040e-113">Exemplo 2: remover uma política de ponto de extremidade de serviço usando objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="b040e-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="b040e-114">Esse comando Remove um objeto de política de ponto de extremidade de serviço de Policy1 que pertence a um nome de resourcegroup1 "</span><span class="sxs-lookup"><span data-stu-id="b040e-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="b040e-115">OS</span><span class="sxs-lookup"><span data-stu-id="b040e-115">PARAMETERS</span></span>

### <span data-ttu-id="b040e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b040e-116">-DefaultProfile</span></span>
<span data-ttu-id="b040e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b040e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b040e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b040e-118">-Force</span></span>
<span data-ttu-id="b040e-119">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="b040e-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b040e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b040e-120">-InputObject</span></span>
<span data-ttu-id="b040e-121">O objeto da política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="b040e-121">The service endpoint policy object.</span></span>

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

### <span data-ttu-id="b040e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b040e-122">-Name</span></span>
<span data-ttu-id="b040e-123">O nome da política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="b040e-123">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="b040e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b040e-124">-PassThru</span></span>
<span data-ttu-id="b040e-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="b040e-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="b040e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b040e-126">-ResourceGroupName</span></span>
<span data-ttu-id="b040e-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b040e-127">The resource group name.</span></span>

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

### <span data-ttu-id="b040e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b040e-128">-ResourceId</span></span>
<span data-ttu-id="b040e-129">A ID da política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="b040e-129">The ID of service endpoint policy.</span></span>

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

### <span data-ttu-id="b040e-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b040e-130">-Confirm</span></span>
<span data-ttu-id="b040e-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b040e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b040e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b040e-132">-WhatIf</span></span>
<span data-ttu-id="b040e-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b040e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b040e-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b040e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b040e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b040e-135">CommonParameters</span></span>
<span data-ttu-id="b040e-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b040e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b040e-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b040e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b040e-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b040e-138">INPUTS</span></span>

### <span data-ttu-id="b040e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b040e-139">System.String</span></span>

### <span data-ttu-id="b040e-140">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b040e-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="b040e-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b040e-141">OUTPUTS</span></span>

### <span data-ttu-id="b040e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b040e-142">System.Boolean</span></span>

## <span data-ttu-id="b040e-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b040e-143">NOTES</span></span>

## <span data-ttu-id="b040e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b040e-144">RELATED LINKS</span></span>

[<span data-ttu-id="b040e-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b040e-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="b040e-146">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b040e-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="b040e-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b040e-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
