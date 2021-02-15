---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: d0056cedad180fda8475abae2106aaba3d2ad239
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112799"
---
# <span data-ttu-id="14489-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="14489-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="14489-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14489-102">SYNOPSIS</span></span>
<span data-ttu-id="14489-103">Remove uma identidade de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="14489-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="14489-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14489-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14489-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="14489-105">DESCRIPTION</span></span>
<span data-ttu-id="14489-106">**O cmdlet Remove-AzApplicationGatewayIdentity** remove a identidade de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="14489-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="14489-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="14489-107">EXAMPLES</span></span>

### <span data-ttu-id="14489-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="14489-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="14489-109">Neste exemplo, removemos a identidade de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="14489-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="14489-110">Observação: se o gateway estiver fazendo referência a um segredo de keyvault, também é importante remover essas referências de certificado ssl ao longo desta operação.</span><span class="sxs-lookup"><span data-stu-id="14489-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="14489-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14489-111">PARAMETERS</span></span>

### <span data-ttu-id="14489-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14489-112">-ApplicationGateway</span></span>
<span data-ttu-id="14489-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="14489-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14489-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14489-114">-DefaultProfile</span></span>
<span data-ttu-id="14489-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14489-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14489-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="14489-116">-Confirm</span></span>
<span data-ttu-id="14489-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14489-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14489-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14489-118">-WhatIf</span></span>
<span data-ttu-id="14489-119">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="14489-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14489-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14489-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14489-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14489-121">CommonParameters</span></span>
<span data-ttu-id="14489-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14489-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14489-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14489-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14489-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="14489-124">INPUTS</span></span>

### <span data-ttu-id="14489-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14489-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14489-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="14489-126">OUTPUTS</span></span>

### <span data-ttu-id="14489-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14489-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14489-128">Notas</span><span class="sxs-lookup"><span data-stu-id="14489-128">NOTES</span></span>

## <span data-ttu-id="14489-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14489-129">RELATED LINKS</span></span>
