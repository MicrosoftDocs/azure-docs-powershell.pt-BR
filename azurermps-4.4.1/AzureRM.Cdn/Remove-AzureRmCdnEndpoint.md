---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 49afefc7b80b5475735f61cb0511366b7f27a466
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441586"
---
# <span data-ttu-id="ed8c9-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed8c9-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="ed8c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed8c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ed8c9-103">Remove um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="ed8c9-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed8c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed8c9-104">SYNTAX</span></span>

### <span data-ttu-id="ed8c9-105">Conjunto de parâmetros para parâmetros de campos</span><span class="sxs-lookup"><span data-stu-id="ed8c9-105">Parameter Set for fields parameters</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed8c9-106">Conjunto de parâmetros para parâmetros de objeto</span><span class="sxs-lookup"><span data-stu-id="ed8c9-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed8c9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed8c9-107">DESCRIPTION</span></span>
<span data-ttu-id="ed8c9-108">O cmdlet **Remove-AzureRmCdnEndpoint** remove um ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="ed8c9-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="ed8c9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed8c9-109">EXAMPLES</span></span>

## <span data-ttu-id="ed8c9-110">OS</span><span class="sxs-lookup"><span data-stu-id="ed8c9-110">PARAMETERS</span></span>

### <span data-ttu-id="ed8c9-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed8c9-111">-CdnEndpoint</span></span>
<span data-ttu-id="ed8c9-112">Especifica o ponto de extremidade que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="ed8c9-112">Specifies the endpoint that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8c9-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ed8c9-113">-EndpointName</span></span>
<span data-ttu-id="ed8c9-114">Especifica o nome do ponto de extremidade que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="ed8c9-114">Specifies the name of the endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8c9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ed8c9-115">-Force</span></span>
<span data-ttu-id="ed8c9-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ed8c9-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ed8c9-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed8c9-117">-PassThru</span></span>
<span data-ttu-id="ed8c9-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="ed8c9-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ed8c9-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ed8c9-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ed8c9-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ed8c9-120">-ProfileName</span></span>
<span data-ttu-id="ed8c9-121">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="ed8c9-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8c9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed8c9-122">-ResourceGroupName</span></span>
<span data-ttu-id="ed8c9-123">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="ed8c9-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8c9-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ed8c9-124">-Confirm</span></span>
<span data-ttu-id="ed8c9-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed8c9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed8c9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed8c9-126">-WhatIf</span></span>
<span data-ttu-id="ed8c9-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ed8c9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed8c9-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ed8c9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed8c9-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed8c9-129">-DefaultProfile</span></span>
<span data-ttu-id="ed8c9-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed8c9-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8c9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed8c9-131">CommonParameters</span></span>
<span data-ttu-id="ed8c9-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed8c9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed8c9-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed8c9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed8c9-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed8c9-134">INPUTS</span></span>

### <span data-ttu-id="ed8c9-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed8c9-135">PSEndpoint</span></span>
<span data-ttu-id="ed8c9-136">O parâmetro ' CdnEndpoint ' aceita o valor do tipo ' PSEndpoint ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ed8c9-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="ed8c9-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed8c9-137">OUTPUTS</span></span>

### <span data-ttu-id="ed8c9-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed8c9-138">System.Boolean</span></span>

## <span data-ttu-id="ed8c9-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed8c9-139">NOTES</span></span>

## <span data-ttu-id="ed8c9-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed8c9-140">RELATED LINKS</span></span>

[<span data-ttu-id="ed8c9-141">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed8c9-141">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="ed8c9-142">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed8c9-142">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="ed8c9-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed8c9-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="ed8c9-144">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed8c9-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="ed8c9-145">Parar-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed8c9-145">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)

