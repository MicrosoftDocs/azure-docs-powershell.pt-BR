---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 2b7b6755b15c5dcaf0442557eb32b563f0c1af6e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111545"
---
# <span data-ttu-id="266b8-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="266b8-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="266b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="266b8-102">SYNOPSIS</span></span>
<span data-ttu-id="266b8-103">Remove uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="266b8-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="266b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="266b8-104">SYNTAX</span></span>

### <span data-ttu-id="266b8-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="266b8-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="266b8-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="266b8-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="266b8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="266b8-107">DESCRIPTION</span></span>
<span data-ttu-id="266b8-108">O cmdlet **Remove-AzPrivateEndpointConnection** remove uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="266b8-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="266b8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="266b8-109">EXAMPLES</span></span>

### <span data-ttu-id="266b8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="266b8-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="266b8-111">Este exemplo remove uma conexão de ponto de extremidade particular chamada MyPrivateEndpointConnection1</span><span class="sxs-lookup"><span data-stu-id="266b8-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="266b8-112">OS</span><span class="sxs-lookup"><span data-stu-id="266b8-112">PARAMETERS</span></span>

### <span data-ttu-id="266b8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="266b8-113">-AsJob</span></span>
<span data-ttu-id="266b8-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="266b8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="266b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="266b8-115">-DefaultProfile</span></span>
<span data-ttu-id="266b8-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="266b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="266b8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="266b8-117">-Force</span></span>
<span data-ttu-id="266b8-118">Não pedir confirmação se quiser excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="266b8-118">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="266b8-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="266b8-119">-Name</span></span>
<span data-ttu-id="266b8-120">O nome da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="266b8-120">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="266b8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="266b8-121">-PassThru</span></span>
<span data-ttu-id="266b8-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="266b8-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="266b8-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="266b8-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="266b8-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="266b8-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="266b8-125">O tipo de recurso de link particular.</span><span class="sxs-lookup"><span data-stu-id="266b8-125">The private link resource type.</span></span>

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

### <span data-ttu-id="266b8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="266b8-126">-ResourceGroupName</span></span>
<span data-ttu-id="266b8-127">O nome do grupo de recursos da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="266b8-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="266b8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="266b8-128">-ResourceId</span></span>
<span data-ttu-id="266b8-129">A ID do Gerenciador de recursos do Azure da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="266b8-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="266b8-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="266b8-130">-ServiceName</span></span>
<span data-ttu-id="266b8-131">O nome do serviço ao qual pertence a conexão de ponto de extremidade privada.</span><span class="sxs-lookup"><span data-stu-id="266b8-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="266b8-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="266b8-132">-Confirm</span></span>
<span data-ttu-id="266b8-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="266b8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="266b8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="266b8-134">-WhatIf</span></span>
<span data-ttu-id="266b8-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="266b8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="266b8-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="266b8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="266b8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="266b8-137">CommonParameters</span></span>
<span data-ttu-id="266b8-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="266b8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="266b8-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="266b8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="266b8-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="266b8-140">INPUTS</span></span>

### <span data-ttu-id="266b8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="266b8-141">System.String</span></span>

## <span data-ttu-id="266b8-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="266b8-142">OUTPUTS</span></span>

### <span data-ttu-id="266b8-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="266b8-143">System.Boolean</span></span>

## <span data-ttu-id="266b8-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="266b8-144">NOTES</span></span>

## <span data-ttu-id="266b8-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="266b8-145">RELATED LINKS</span></span>

[<span data-ttu-id="266b8-146">Aprovar-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="266b8-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="266b8-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="266b8-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="266b8-148">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="266b8-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="266b8-149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="266b8-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
