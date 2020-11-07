---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 9de25adae04afd0f09a2a09118c55d4e679a44db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772258"
---
# <span data-ttu-id="74cda-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="74cda-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="74cda-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74cda-102">SYNOPSIS</span></span>
<span data-ttu-id="74cda-103">Remove uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="74cda-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="74cda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74cda-104">SYNTAX</span></span>

### <span data-ttu-id="74cda-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="74cda-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection [-Force] [-AsJob] [-PassThru] -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74cda-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="74cda-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection [-Force] [-AsJob] [-PassThru] -Name <String> -ServiceName <String>
 -ResourceGroupName <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74cda-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74cda-107">DESCRIPTION</span></span>
<span data-ttu-id="74cda-108">O cmdlet **Remove-AzPrivateEndpointConnection** remove uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="74cda-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span> 

## <span data-ttu-id="74cda-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74cda-109">EXAMPLES</span></span>

### <span data-ttu-id="74cda-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="74cda-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="74cda-111">Este exemplo remove uma conexão de ponto de extremidade particular chamada MyPrivateEndpointConnection1</span><span class="sxs-lookup"><span data-stu-id="74cda-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="74cda-112">OS</span><span class="sxs-lookup"><span data-stu-id="74cda-112">PARAMETERS</span></span>

### <span data-ttu-id="74cda-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74cda-113">-AsJob</span></span>
<span data-ttu-id="74cda-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="74cda-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74cda-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74cda-115">-DefaultProfile</span></span>
<span data-ttu-id="74cda-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74cda-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74cda-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="74cda-117">-Description</span></span>
<span data-ttu-id="74cda-118">O motivo da ação.</span><span class="sxs-lookup"><span data-stu-id="74cda-118">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74cda-119">-Force</span><span class="sxs-lookup"><span data-stu-id="74cda-119">-Force</span></span>
<span data-ttu-id="74cda-120">Não pedir confirmação se quiser excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="74cda-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="74cda-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="74cda-121">-Name</span></span>
<span data-ttu-id="74cda-122">O nome da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="74cda-122">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="74cda-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74cda-123">-PassThru</span></span>
<span data-ttu-id="74cda-124">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="74cda-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="74cda-125">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="74cda-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="74cda-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74cda-126">-ResourceGroupName</span></span>
<span data-ttu-id="74cda-127">O nome do grupo de recursos da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="74cda-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="74cda-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74cda-128">-ResourceId</span></span>
<span data-ttu-id="74cda-129">A ID do Gerenciador de recursos do Azure da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="74cda-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="74cda-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="74cda-130">-ServiceName</span></span>
<span data-ttu-id="74cda-131">O nome do serviço de vínculo privado que tem a conexão de ponto de extremidade privada.</span><span class="sxs-lookup"><span data-stu-id="74cda-131">The name of the private link service that has the private endpoint connection.</span></span>

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

### <span data-ttu-id="74cda-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="74cda-132">-Confirm</span></span>
<span data-ttu-id="74cda-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74cda-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74cda-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74cda-134">-WhatIf</span></span>
<span data-ttu-id="74cda-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="74cda-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74cda-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74cda-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74cda-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74cda-137">CommonParameters</span></span>
<span data-ttu-id="74cda-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74cda-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74cda-139">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74cda-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74cda-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74cda-140">INPUTS</span></span>

### <span data-ttu-id="74cda-141">System. String</span><span class="sxs-lookup"><span data-stu-id="74cda-141">System.String</span></span>

## <span data-ttu-id="74cda-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74cda-142">OUTPUTS</span></span>

### <span data-ttu-id="74cda-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="74cda-143">System.Boolean</span></span>

## <span data-ttu-id="74cda-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74cda-144">NOTES</span></span>

## <span data-ttu-id="74cda-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74cda-145">RELATED LINKS</span></span>

[<span data-ttu-id="74cda-146">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="74cda-146">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
