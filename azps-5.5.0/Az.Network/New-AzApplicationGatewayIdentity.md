---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: e32c0912026555f9b85a83720d1c7c48a5170f70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117416"
---
# <span data-ttu-id="120a8-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="120a8-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="120a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="120a8-102">SYNOPSIS</span></span>
<span data-ttu-id="120a8-103">Cria um objeto de identidade para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="120a8-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="120a8-104">Isso fará referência à identidade atribuída pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="120a8-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="120a8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="120a8-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="120a8-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="120a8-106">DESCRIPTION</span></span>
<span data-ttu-id="120a8-107">**O cmdlet New-AzApplicationGatewayIdentity cria** um objeto de identidade do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="120a8-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="120a8-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="120a8-108">EXAMPLES</span></span>

### <span data-ttu-id="120a8-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="120a8-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="120a8-110">Neste exemplo, criamos uma identidade atribuída ao usuário e a referenciamos no objeto de identidade usado com o Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="120a8-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="120a8-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="120a8-111">PARAMETERS</span></span>

### <span data-ttu-id="120a8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="120a8-112">-DefaultProfile</span></span>
<span data-ttu-id="120a8-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="120a8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="120a8-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="120a8-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="120a8-115">ResourceId da identidade atribuída pelo usuário a ser atribuída ao Gateway de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="120a8-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="120a8-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="120a8-116">-Confirm</span></span>
<span data-ttu-id="120a8-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="120a8-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="120a8-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="120a8-118">-WhatIf</span></span>
<span data-ttu-id="120a8-119">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="120a8-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="120a8-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="120a8-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="120a8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="120a8-121">CommonParameters</span></span>
<span data-ttu-id="120a8-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="120a8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="120a8-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="120a8-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="120a8-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="120a8-124">INPUTS</span></span>

### <span data-ttu-id="120a8-125">System.String</span><span class="sxs-lookup"><span data-stu-id="120a8-125">System.String</span></span>

## <span data-ttu-id="120a8-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="120a8-126">OUTPUTS</span></span>

### <span data-ttu-id="120a8-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="120a8-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="120a8-128">Notas</span><span class="sxs-lookup"><span data-stu-id="120a8-128">NOTES</span></span>

## <span data-ttu-id="120a8-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="120a8-129">RELATED LINKS</span></span>
