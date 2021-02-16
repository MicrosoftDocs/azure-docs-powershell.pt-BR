---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 2b7b6755b15c5dcaf0442557eb32b563f0c1af6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118280"
---
# <span data-ttu-id="0e0c4-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0e0c4-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="0e0c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e0c4-102">SYNOPSIS</span></span>
<span data-ttu-id="0e0c4-103">Remove uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="0e0c4-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="0e0c4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e0c4-104">SYNTAX</span></span>

### <span data-ttu-id="0e0c4-105">ByResourceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0e0c4-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e0c4-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="0e0c4-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e0c4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e0c4-107">DESCRIPTION</span></span>
<span data-ttu-id="0e0c4-108">O cmdlet **Remove-AzPrivateEndpointConnection** remove uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="0e0c4-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="0e0c4-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0e0c4-109">EXAMPLES</span></span>

### <span data-ttu-id="0e0c4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0e0c4-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="0e0c4-111">Este exemplo remove uma conexão de ponto de extremidade particular chamada MyPrivateEndpointConnection1</span><span class="sxs-lookup"><span data-stu-id="0e0c4-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="0e0c4-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e0c4-112">PARAMETERS</span></span>

### <span data-ttu-id="0e0c4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e0c4-113">-AsJob</span></span>
<span data-ttu-id="0e0c4-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0e0c4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e0c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e0c4-115">-DefaultProfile</span></span>
<span data-ttu-id="0e0c4-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e0c4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e0c4-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="0e0c4-117">-Force</span></span>
<span data-ttu-id="0e0c4-118">Não peça confirmação se quiser excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="0e0c4-118">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="0e0c4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e0c4-119">-Name</span></span>
<span data-ttu-id="0e0c4-120">O nome da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="0e0c4-120">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0c4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e0c4-121">-PassThru</span></span>
<span data-ttu-id="0e0c4-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="0e0c4-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0e0c4-123">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="0e0c4-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0e0c4-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="0e0c4-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="0e0c4-125">O tipo de recurso de vínculo privado.</span><span class="sxs-lookup"><span data-stu-id="0e0c4-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0c4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e0c4-126">-ResourceGroupName</span></span>
<span data-ttu-id="0e0c4-127">O nome do grupo de recursos da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="0e0c4-127">The resource group name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0c4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e0c4-128">-ResourceId</span></span>
<span data-ttu-id="0e0c4-129">A ID do gerenciador de recursos do Azure da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="0e0c4-129">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0c4-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0e0c4-130">-ServiceName</span></span>
<span data-ttu-id="0e0c4-131">O nome do serviço ao que a conexão de ponto de extremidade particular pertence.</span><span class="sxs-lookup"><span data-stu-id="0e0c4-131">The name of service that the private endpoint connection belong to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0c4-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0e0c4-132">-Confirm</span></span>
<span data-ttu-id="0e0c4-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e0c4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e0c4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e0c4-134">-WhatIf</span></span>
<span data-ttu-id="0e0c4-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0e0c4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e0c4-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0e0c4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e0c4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e0c4-137">CommonParameters</span></span>
<span data-ttu-id="0e0c4-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e0c4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e0c4-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e0c4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e0c4-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="0e0c4-140">INPUTS</span></span>

### <span data-ttu-id="0e0c4-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0e0c4-141">System.String</span></span>

## <span data-ttu-id="0e0c4-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="0e0c4-142">OUTPUTS</span></span>

### <span data-ttu-id="0e0c4-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0e0c4-143">System.Boolean</span></span>

## <span data-ttu-id="0e0c4-144">Notas</span><span class="sxs-lookup"><span data-stu-id="0e0c4-144">NOTES</span></span>

## <span data-ttu-id="0e0c4-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e0c4-145">RELATED LINKS</span></span>

[<span data-ttu-id="0e0c4-146">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0e0c4-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0e0c4-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0e0c4-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0e0c4-148">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0e0c4-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0e0c4-149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0e0c4-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
