---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
ms.openlocfilehash: 780765ea56cd13ee7cbd09b64dc20db896234aec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116907"
---
# <span data-ttu-id="78c2b-101">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="78c2b-101">Remove-AzCdnEndpoint</span></span>

## <span data-ttu-id="78c2b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="78c2b-103">Remove um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="78c2b-103">Removes a CDN endpoint.</span></span>

## <span data-ttu-id="78c2b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78c2b-104">SYNTAX</span></span>

### <span data-ttu-id="78c2b-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="78c2b-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78c2b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78c2b-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78c2b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="78c2b-107">DESCRIPTION</span></span>
<span data-ttu-id="78c2b-108">O cmdlet **Remove-AzCdnEndpoint** remove um ponto de extremidade de Rede de Distribuição de Conteúdo (CDN) do Azure.</span><span class="sxs-lookup"><span data-stu-id="78c2b-108">The **Remove-AzCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="78c2b-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="78c2b-109">EXAMPLES</span></span>

## <span data-ttu-id="78c2b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78c2b-110">PARAMETERS</span></span>

### <span data-ttu-id="78c2b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="78c2b-111">-CdnEndpoint</span></span>
<span data-ttu-id="78c2b-112">Especifica o ponto de extremidade que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="78c2b-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="78c2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78c2b-113">-DefaultProfile</span></span>
<span data-ttu-id="78c2b-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="78c2b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78c2b-115">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="78c2b-115">-EndpointName</span></span>
<span data-ttu-id="78c2b-116">Especifica o nome do ponto de extremidade que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="78c2b-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="78c2b-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="78c2b-117">-Force</span></span>
<span data-ttu-id="78c2b-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="78c2b-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="78c2b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78c2b-119">-PassThru</span></span>
<span data-ttu-id="78c2b-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="78c2b-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="78c2b-121">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="78c2b-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="78c2b-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="78c2b-122">-ProfileName</span></span>
<span data-ttu-id="78c2b-123">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="78c2b-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="78c2b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78c2b-124">-ResourceGroupName</span></span>
<span data-ttu-id="78c2b-125">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="78c2b-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="78c2b-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="78c2b-126">-Confirm</span></span>
<span data-ttu-id="78c2b-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78c2b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78c2b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78c2b-128">-WhatIf</span></span>
<span data-ttu-id="78c2b-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="78c2b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78c2b-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="78c2b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78c2b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c2b-131">CommonParameters</span></span>
<span data-ttu-id="78c2b-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78c2b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c2b-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78c2b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c2b-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="78c2b-134">INPUTS</span></span>

### <span data-ttu-id="78c2b-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="78c2b-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="78c2b-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="78c2b-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="78c2b-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="78c2b-137">OUTPUTS</span></span>

### <span data-ttu-id="78c2b-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="78c2b-138">System.Boolean</span></span>

## <span data-ttu-id="78c2b-139">Notas</span><span class="sxs-lookup"><span data-stu-id="78c2b-139">NOTES</span></span>

## <span data-ttu-id="78c2b-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78c2b-140">RELATED LINKS</span></span>

[<span data-ttu-id="78c2b-141">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="78c2b-141">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="78c2b-142">Novo-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="78c2b-142">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="78c2b-143">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="78c2b-143">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="78c2b-144">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="78c2b-144">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="78c2b-145">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="78c2b-145">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


