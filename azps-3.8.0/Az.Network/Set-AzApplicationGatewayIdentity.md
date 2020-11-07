---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: aa21ea0719c36e5b737b478657e0734eb21a3c3f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941347"
---
# <span data-ttu-id="7a093-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="7a093-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="7a093-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a093-102">SYNOPSIS</span></span>
<span data-ttu-id="7a093-103">Atualiza uma identidade atribuída ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7a093-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="7a093-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a093-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a093-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a093-105">DESCRIPTION</span></span>
<span data-ttu-id="7a093-106">O cmdlet **set-AzApplicationGatewayIdentity** atualiza uma identidade atribuída ao Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7a093-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="7a093-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a093-107">EXAMPLES</span></span>

### <span data-ttu-id="7a093-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a093-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="7a093-109">Neste exemplo, atribuímos uma identidade atribuída ao usuário a um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="7a093-109">In this example, we assign a user assigned identity to an existing application gateway.</span></span>
<span data-ttu-id="7a093-110">Observação: essa identidade deve ter acesso ao cofre a partir do qual os certificados/segredos serão referenciados.</span><span class="sxs-lookup"><span data-stu-id="7a093-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="7a093-111">OS</span><span class="sxs-lookup"><span data-stu-id="7a093-111">PARAMETERS</span></span>

### <span data-ttu-id="7a093-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a093-112">-ApplicationGateway</span></span>
<span data-ttu-id="7a093-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a093-113">The applicationGateway</span></span>

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

### <span data-ttu-id="7a093-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a093-114">-DefaultProfile</span></span>
<span data-ttu-id="7a093-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a093-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a093-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="7a093-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="7a093-117">ResourceId da identidade atribuída pelo usuário a ser atribuído ao Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7a093-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a093-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7a093-118">-Confirm</span></span>
<span data-ttu-id="7a093-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a093-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a093-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a093-120">-WhatIf</span></span>
<span data-ttu-id="7a093-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7a093-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a093-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7a093-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a093-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a093-123">CommonParameters</span></span>
<span data-ttu-id="7a093-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a093-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a093-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a093-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a093-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a093-126">INPUTS</span></span>

### <span data-ttu-id="7a093-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a093-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="7a093-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7a093-128">System.String</span></span>

## <span data-ttu-id="7a093-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a093-129">OUTPUTS</span></span>

### <span data-ttu-id="7a093-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a093-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7a093-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a093-131">NOTES</span></span>

## <span data-ttu-id="7a093-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a093-132">RELATED LINKS</span></span>
