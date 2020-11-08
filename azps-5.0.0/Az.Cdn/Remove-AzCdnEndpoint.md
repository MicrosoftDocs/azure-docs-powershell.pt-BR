---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
ms.openlocfilehash: 780765ea56cd13ee7cbd09b64dc20db896234aec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125039"
---
# <span data-ttu-id="26720-101">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="26720-101">Remove-AzCdnEndpoint</span></span>

## <span data-ttu-id="26720-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26720-102">SYNOPSIS</span></span>
<span data-ttu-id="26720-103">Remove um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="26720-103">Removes a CDN endpoint.</span></span>

## <span data-ttu-id="26720-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26720-104">SYNTAX</span></span>

### <span data-ttu-id="26720-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="26720-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26720-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26720-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26720-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="26720-107">DESCRIPTION</span></span>
<span data-ttu-id="26720-108">O cmdlet **Remove-AzCdnEndpoint** remove um ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="26720-108">The **Remove-AzCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="26720-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26720-109">EXAMPLES</span></span>

## <span data-ttu-id="26720-110">OS</span><span class="sxs-lookup"><span data-stu-id="26720-110">PARAMETERS</span></span>

### <span data-ttu-id="26720-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="26720-111">-CdnEndpoint</span></span>
<span data-ttu-id="26720-112">Especifica o ponto de extremidade que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="26720-112">Specifies the endpoint that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26720-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26720-113">-DefaultProfile</span></span>
<span data-ttu-id="26720-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="26720-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26720-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="26720-115">-EndpointName</span></span>
<span data-ttu-id="26720-116">Especifica o nome do ponto de extremidade que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="26720-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26720-117">-Force</span><span class="sxs-lookup"><span data-stu-id="26720-117">-Force</span></span>
<span data-ttu-id="26720-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="26720-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26720-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26720-119">-PassThru</span></span>
<span data-ttu-id="26720-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="26720-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="26720-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="26720-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26720-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="26720-122">-ProfileName</span></span>
<span data-ttu-id="26720-123">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="26720-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26720-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26720-124">-ResourceGroupName</span></span>
<span data-ttu-id="26720-125">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="26720-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26720-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="26720-126">-Confirm</span></span>
<span data-ttu-id="26720-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26720-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26720-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26720-128">-WhatIf</span></span>
<span data-ttu-id="26720-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="26720-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26720-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="26720-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26720-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26720-131">CommonParameters</span></span>
<span data-ttu-id="26720-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26720-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26720-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26720-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26720-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="26720-134">INPUTS</span></span>

### <span data-ttu-id="26720-135">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="26720-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="26720-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="26720-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="26720-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="26720-137">OUTPUTS</span></span>

### <span data-ttu-id="26720-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26720-138">System.Boolean</span></span>

## <span data-ttu-id="26720-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="26720-139">NOTES</span></span>

## <span data-ttu-id="26720-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26720-140">RELATED LINKS</span></span>

[<span data-ttu-id="26720-141">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="26720-141">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="26720-142">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="26720-142">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="26720-143">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="26720-143">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="26720-144">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="26720-144">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="26720-145">Parar-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="26720-145">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


