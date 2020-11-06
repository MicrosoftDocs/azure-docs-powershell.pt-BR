---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 8748806346baa4f84550d15749e7792ae928ad34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429893"
---
# <span data-ttu-id="fee42-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fee42-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="fee42-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fee42-102">SYNOPSIS</span></span>
<span data-ttu-id="fee42-103">Remove um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="fee42-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fee42-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fee42-104">SYNTAX</span></span>

### <span data-ttu-id="fee42-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="fee42-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fee42-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fee42-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fee42-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fee42-107">DESCRIPTION</span></span>
<span data-ttu-id="fee42-108">O cmdlet **Remove-AzureRmCdnEndpoint** remove um ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="fee42-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="fee42-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fee42-109">EXAMPLES</span></span>

## <span data-ttu-id="fee42-110">OS</span><span class="sxs-lookup"><span data-stu-id="fee42-110">PARAMETERS</span></span>

### <span data-ttu-id="fee42-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fee42-111">-CdnEndpoint</span></span>
<span data-ttu-id="fee42-112">Especifica o ponto de extremidade que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="fee42-112">Specifies the endpoint that this cmdlet removes.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fee42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee42-113">-DefaultProfile</span></span>
<span data-ttu-id="fee42-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fee42-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fee42-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fee42-115">-EndpointName</span></span>
<span data-ttu-id="fee42-116">Especifica o nome do ponto de extremidade que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="fee42-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fee42-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fee42-117">-Force</span></span>
<span data-ttu-id="fee42-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="fee42-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fee42-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fee42-119">-PassThru</span></span>
<span data-ttu-id="fee42-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="fee42-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fee42-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="fee42-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fee42-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fee42-122">-ProfileName</span></span>
<span data-ttu-id="fee42-123">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="fee42-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fee42-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fee42-124">-ResourceGroupName</span></span>
<span data-ttu-id="fee42-125">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="fee42-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fee42-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fee42-126">-Confirm</span></span>
<span data-ttu-id="fee42-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fee42-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fee42-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fee42-128">-WhatIf</span></span>
<span data-ttu-id="fee42-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fee42-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fee42-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fee42-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fee42-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee42-131">CommonParameters</span></span>
<span data-ttu-id="fee42-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fee42-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee42-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fee42-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee42-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fee42-134">INPUTS</span></span>

### <span data-ttu-id="fee42-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="fee42-135">PSEndpoint</span></span>
<span data-ttu-id="fee42-136">O parâmetro ' CdnEndpoint ' aceita o valor do tipo ' PSEndpoint ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="fee42-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="fee42-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fee42-137">OUTPUTS</span></span>

### <span data-ttu-id="fee42-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fee42-138">System.Boolean</span></span>

## <span data-ttu-id="fee42-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fee42-139">NOTES</span></span>

## <span data-ttu-id="fee42-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fee42-140">RELATED LINKS</span></span>

[<span data-ttu-id="fee42-141">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fee42-141">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="fee42-142">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fee42-142">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="fee42-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fee42-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="fee42-144">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fee42-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="fee42-145">Parar-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fee42-145">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


