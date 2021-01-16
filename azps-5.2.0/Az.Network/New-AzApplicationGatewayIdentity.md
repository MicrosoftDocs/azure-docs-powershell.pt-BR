---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: e32c0912026555f9b85a83720d1c7c48a5170f70
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261353"
---
# <span data-ttu-id="2df42-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="2df42-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="2df42-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2df42-102">SYNOPSIS</span></span>
<span data-ttu-id="2df42-103">Cria um objeto Identity para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2df42-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="2df42-104">Isso fará referência à identidade atribuída ao usuário.</span><span class="sxs-lookup"><span data-stu-id="2df42-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="2df42-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2df42-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2df42-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2df42-106">DESCRIPTION</span></span>
<span data-ttu-id="2df42-107">O cmdlet **New-AzApplicationGatewayIdentity** cria um objeto Identity do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="2df42-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="2df42-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2df42-108">EXAMPLES</span></span>

### <span data-ttu-id="2df42-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2df42-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="2df42-110">Neste exemplo, criamos uma identidade atribuída pelo usuário e a referenciamos no objeto Identity usado com o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="2df42-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="2df42-111">OS</span><span class="sxs-lookup"><span data-stu-id="2df42-111">PARAMETERS</span></span>

### <span data-ttu-id="2df42-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df42-112">-DefaultProfile</span></span>
<span data-ttu-id="2df42-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2df42-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2df42-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="2df42-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="2df42-115">ResourceId da identidade atribuída pelo usuário a ser atribuído ao Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="2df42-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="2df42-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2df42-116">-Confirm</span></span>
<span data-ttu-id="2df42-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2df42-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2df42-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2df42-118">-WhatIf</span></span>
<span data-ttu-id="2df42-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2df42-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2df42-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2df42-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2df42-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df42-121">CommonParameters</span></span>
<span data-ttu-id="2df42-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2df42-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df42-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2df42-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df42-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2df42-124">INPUTS</span></span>

### <span data-ttu-id="2df42-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2df42-125">System.String</span></span>

## <span data-ttu-id="2df42-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2df42-126">OUTPUTS</span></span>

### <span data-ttu-id="2df42-127">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="2df42-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="2df42-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2df42-128">NOTES</span></span>

## <span data-ttu-id="2df42-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2df42-129">RELATED LINKS</span></span>
