---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: ec7003b90d9489f2966d4fd1ebe3e3fb3fa74ce5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114580"
---
# <span data-ttu-id="89ff6-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="89ff6-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="89ff6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="89ff6-103">Atualizar Informações de Contato</span><span class="sxs-lookup"><span data-stu-id="89ff6-103">Update Contact Information</span></span>

## <span data-ttu-id="89ff6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89ff6-104">SYNTAX</span></span>

```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89ff6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="89ff6-105">DESCRIPTION</span></span>
<span data-ttu-id="89ff6-106">Permite atualizar as informações de contato de um PeerAsn na assinatura.</span><span class="sxs-lookup"><span data-stu-id="89ff6-106">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="89ff6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="89ff6-107">EXAMPLES</span></span>

### <span data-ttu-id="89ff6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="89ff6-108">Example 1</span></span>
```powershell
#Get the Peer ASN object
PS C:> Get-AzPeerAsn -PeerName Contoso | Set-AzPeerAsn -Email noc1@contoso.com

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="89ff6-109">Adiciona um endereço de email ao Peer Asn</span><span class="sxs-lookup"><span data-stu-id="89ff6-109">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="89ff6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89ff6-110">PARAMETERS</span></span>

### <span data-ttu-id="89ff6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89ff6-111">-AsJob</span></span>
<span data-ttu-id="89ff6-112">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="89ff6-112">Run in the background.</span></span>

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

### <span data-ttu-id="89ff6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ff6-113">-DefaultProfile</span></span>
<span data-ttu-id="89ff6-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89ff6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89ff6-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89ff6-115">-InputObject</span></span>
<span data-ttu-id="89ff6-116">{{ Fill InputObject Description }}</span><span class="sxs-lookup"><span data-stu-id="89ff6-116">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89ff6-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="89ff6-117">-Confirm</span></span>
<span data-ttu-id="89ff6-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89ff6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89ff6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89ff6-119">-WhatIf</span></span>
<span data-ttu-id="89ff6-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="89ff6-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89ff6-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="89ff6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89ff6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ff6-122">CommonParameters</span></span>
<span data-ttu-id="89ff6-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89ff6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ff6-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89ff6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ff6-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="89ff6-125">INPUTS</span></span>

### <span data-ttu-id="89ff6-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="89ff6-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="89ff6-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="89ff6-127">OUTPUTS</span></span>

### <span data-ttu-id="89ff6-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="89ff6-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="89ff6-129">Notas</span><span class="sxs-lookup"><span data-stu-id="89ff6-129">NOTES</span></span>

## <span data-ttu-id="89ff6-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89ff6-130">RELATED LINKS</span></span>
