---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: e32c0912026555f9b85a83720d1c7c48a5170f70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272658"
---
# <span data-ttu-id="9f678-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="9f678-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="9f678-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f678-102">SYNOPSIS</span></span>
<span data-ttu-id="9f678-103">Cria um objeto Identity para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9f678-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="9f678-104">Isso fará referência à identidade atribuída ao usuário.</span><span class="sxs-lookup"><span data-stu-id="9f678-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="9f678-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f678-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f678-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f678-106">DESCRIPTION</span></span>
<span data-ttu-id="9f678-107">O cmdlet **New-AzApplicationGatewayIdentity** cria um objeto Identity do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9f678-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="9f678-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f678-108">EXAMPLES</span></span>

### <span data-ttu-id="9f678-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9f678-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="9f678-110">Neste exemplo, criamos uma identidade atribuída pelo usuário e a referenciamos no objeto Identity usado com o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9f678-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="9f678-111">OS</span><span class="sxs-lookup"><span data-stu-id="9f678-111">PARAMETERS</span></span>

### <span data-ttu-id="9f678-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f678-112">-DefaultProfile</span></span>
<span data-ttu-id="9f678-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f678-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f678-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="9f678-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="9f678-115">ResourceId da identidade atribuída pelo usuário a ser atribuído ao Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9f678-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="9f678-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9f678-116">-Confirm</span></span>
<span data-ttu-id="9f678-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f678-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f678-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f678-118">-WhatIf</span></span>
<span data-ttu-id="9f678-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9f678-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f678-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f678-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f678-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f678-121">CommonParameters</span></span>
<span data-ttu-id="9f678-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f678-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f678-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f678-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f678-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f678-124">INPUTS</span></span>

### <span data-ttu-id="9f678-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9f678-125">System.String</span></span>

## <span data-ttu-id="9f678-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f678-126">OUTPUTS</span></span>

### <span data-ttu-id="9f678-127">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="9f678-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="9f678-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f678-128">NOTES</span></span>

## <span data-ttu-id="9f678-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f678-129">RELATED LINKS</span></span>
