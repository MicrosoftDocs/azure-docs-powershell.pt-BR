---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: f1cc98c8008d8f9eff47fa6f5172fb28a448c7ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890780"
---
# <span data-ttu-id="a3f1c-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="a3f1c-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="a3f1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3f1c-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f1c-103">Cria um objeto identity para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="a3f1c-104">Isso manterá referência à identidade atribuída pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="a3f1c-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a3f1c-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3f1c-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a3f1c-106">DESCRIPTION</span></span>
<span data-ttu-id="a3f1c-107">O cmdlet **New-AzApplicationGatewayIdentity** cria um objeto de identidade do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="a3f1c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3f1c-108">EXAMPLES</span></span>

### <span data-ttu-id="a3f1c-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a3f1c-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="a3f1c-110">Neste exemplo, criamos uma identidade atribuída ao usuário e a referenciamos no objeto identity usado com o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="a3f1c-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a3f1c-111">PARAMETERS</span></span>

### <span data-ttu-id="a3f1c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f1c-112">-DefaultProfile</span></span>
<span data-ttu-id="a3f1c-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3f1c-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="a3f1c-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="a3f1c-115">ResourceId da identidade atribuída pelo usuário a ser atribuída ao Gateway de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="a3f1c-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3f1c-116">-Confirm</span></span>
<span data-ttu-id="a3f1c-117">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3f1c-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3f1c-118">-WhatIf</span></span>
<span data-ttu-id="a3f1c-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3f1c-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3f1c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f1c-121">CommonParameters</span></span>
<span data-ttu-id="a3f1c-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3f1c-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3f1c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f1c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3f1c-124">INPUTS</span></span>

### <span data-ttu-id="a3f1c-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a3f1c-125">System.String</span></span>

## <span data-ttu-id="a3f1c-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a3f1c-126">OUTPUTS</span></span>

### <span data-ttu-id="a3f1c-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="a3f1c-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="a3f1c-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="a3f1c-128">NOTES</span></span>

## <span data-ttu-id="a3f1c-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3f1c-129">RELATED LINKS</span></span>
