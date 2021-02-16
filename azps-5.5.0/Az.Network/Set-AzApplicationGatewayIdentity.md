---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: aa21ea0719c36e5b737b478657e0734eb21a3c3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113441"
---
# <span data-ttu-id="15b35-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="15b35-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="15b35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15b35-102">SYNOPSIS</span></span>
<span data-ttu-id="15b35-103">Atualiza uma identidade atribuída ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15b35-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="15b35-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15b35-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15b35-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="15b35-105">DESCRIPTION</span></span>
<span data-ttu-id="15b35-106">O cmdlet **Set-AzApplicationGatewayIdentity** atualiza uma identidade atribuída ao gateway de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="15b35-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="15b35-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="15b35-107">EXAMPLES</span></span>

### <span data-ttu-id="15b35-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="15b35-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="15b35-109">Neste exemplo, atribuímos uma identidade atribuída a um usuário a um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="15b35-109">In this example, we assign a user assigned identity to an existing application gateway.</span></span>
<span data-ttu-id="15b35-110">Observação: essa identidade deve ter acesso ao resultado da chave a partir do qual os certificados/segredos serão referenciados.</span><span class="sxs-lookup"><span data-stu-id="15b35-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="15b35-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15b35-111">PARAMETERS</span></span>

### <span data-ttu-id="15b35-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15b35-112">-ApplicationGateway</span></span>
<span data-ttu-id="15b35-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="15b35-113">The applicationGateway</span></span>

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

### <span data-ttu-id="15b35-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15b35-114">-DefaultProfile</span></span>
<span data-ttu-id="15b35-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15b35-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15b35-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="15b35-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="15b35-117">ResourceId da identidade atribuída pelo usuário a ser atribuída ao Gateway de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="15b35-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="15b35-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="15b35-118">-Confirm</span></span>
<span data-ttu-id="15b35-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15b35-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15b35-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15b35-120">-WhatIf</span></span>
<span data-ttu-id="15b35-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="15b35-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15b35-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="15b35-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15b35-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b35-123">CommonParameters</span></span>
<span data-ttu-id="15b35-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15b35-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b35-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15b35-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b35-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="15b35-126">INPUTS</span></span>

### <span data-ttu-id="15b35-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15b35-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="15b35-128">System.String</span><span class="sxs-lookup"><span data-stu-id="15b35-128">System.String</span></span>

## <span data-ttu-id="15b35-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="15b35-129">OUTPUTS</span></span>

### <span data-ttu-id="15b35-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15b35-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="15b35-131">Notas</span><span class="sxs-lookup"><span data-stu-id="15b35-131">NOTES</span></span>

## <span data-ttu-id="15b35-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15b35-132">RELATED LINKS</span></span>
