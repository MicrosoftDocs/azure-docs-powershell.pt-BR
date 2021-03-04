---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2f100d29b2251d71b170c7833f77ab2f23f90209
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885857"
---
# <span data-ttu-id="6afca-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="6afca-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="6afca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6afca-102">SYNOPSIS</span></span>
<span data-ttu-id="6afca-103">Atualiza uma identidade atribuída ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6afca-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="6afca-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6afca-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6afca-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6afca-105">DESCRIPTION</span></span>
<span data-ttu-id="6afca-106">O cmdlet **Set-AzApplicationGatewayIdentity** atualiza uma identidade atribuída ao gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6afca-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="6afca-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6afca-107">EXAMPLES</span></span>

### <span data-ttu-id="6afca-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6afca-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="6afca-109">Neste exemplo, atribuímos uma identidade atribuída a um usuário a um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="6afca-109">In this example, we assign a user assigned identity to an existing application gateway.</span></span>
<span data-ttu-id="6afca-110">Observação: essa identidade deve ter acesso ao keyvault do qual os certificados/segredos serão referenciados.</span><span class="sxs-lookup"><span data-stu-id="6afca-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="6afca-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6afca-111">PARAMETERS</span></span>

### <span data-ttu-id="6afca-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6afca-112">-ApplicationGateway</span></span>
<span data-ttu-id="6afca-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6afca-113">The applicationGateway</span></span>

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

### <span data-ttu-id="6afca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6afca-114">-DefaultProfile</span></span>
<span data-ttu-id="6afca-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6afca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6afca-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="6afca-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="6afca-117">ResourceId da identidade atribuída pelo usuário a ser atribuída ao Gateway de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6afca-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="6afca-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6afca-118">-Confirm</span></span>
<span data-ttu-id="6afca-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6afca-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6afca-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6afca-120">-WhatIf</span></span>
<span data-ttu-id="6afca-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6afca-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6afca-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6afca-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6afca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6afca-123">CommonParameters</span></span>
<span data-ttu-id="6afca-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6afca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6afca-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6afca-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6afca-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6afca-126">INPUTS</span></span>

### <span data-ttu-id="6afca-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6afca-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="6afca-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6afca-128">System.String</span></span>

## <span data-ttu-id="6afca-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6afca-129">OUTPUTS</span></span>

### <span data-ttu-id="6afca-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6afca-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6afca-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="6afca-131">NOTES</span></span>

## <span data-ttu-id="6afca-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6afca-132">RELATED LINKS</span></span>
