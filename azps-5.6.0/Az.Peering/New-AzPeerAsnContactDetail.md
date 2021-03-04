---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: 978c513646c08577f4fa15b8a0e460320878c7c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890158"
---
# <span data-ttu-id="75012-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="75012-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="75012-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75012-102">SYNOPSIS</span></span>
<span data-ttu-id="75012-103">Cria um detalhe de contato na memória para PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="75012-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="75012-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="75012-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75012-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="75012-105">DESCRIPTION</span></span>
<span data-ttu-id="75012-106">Crie um detalhe de contato peerAsn na memória.</span><span class="sxs-lookup"><span data-stu-id="75012-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="75012-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75012-107">EXAMPLES</span></span>

### <span data-ttu-id="75012-108">Criar detalhes de contato e adicionar a PeerAsn</span><span class="sxs-lookup"><span data-stu-id="75012-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="75012-109">Função e email são necessários.</span><span class="sxs-lookup"><span data-stu-id="75012-109">Role and email are required.</span></span> <span data-ttu-id="75012-110">O telefone é opcional.</span><span class="sxs-lookup"><span data-stu-id="75012-110">Phone is optional.</span></span> <span data-ttu-id="75012-111">O telefone dá suporte a +-() ou espaços.</span><span class="sxs-lookup"><span data-stu-id="75012-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="75012-112">Um PeerAsn deve incluir pelo menos um detalhe de contato do tipo "Noc"</span><span class="sxs-lookup"><span data-stu-id="75012-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="75012-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="75012-113">PARAMETERS</span></span>

### <span data-ttu-id="75012-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75012-114">-DefaultProfile</span></span>
<span data-ttu-id="75012-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75012-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75012-116">-Email</span><span class="sxs-lookup"><span data-stu-id="75012-116">-Email</span></span>
<span data-ttu-id="75012-117">Endereços de email usados para entrar em contato se problemas normalmente arrise um Centro de Operações de Rede</span><span class="sxs-lookup"><span data-stu-id="75012-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75012-118">-Phone</span><span class="sxs-lookup"><span data-stu-id="75012-118">-Phone</span></span>
<span data-ttu-id="75012-119">Telefone usado para contatar se problemas arrise normalmente um Centro de Operações de Rede</span><span class="sxs-lookup"><span data-stu-id="75012-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75012-120">-Role</span><span class="sxs-lookup"><span data-stu-id="75012-120">-Role</span></span>
<span data-ttu-id="75012-121">Escolha a função mais adequada às informações de contato.</span><span class="sxs-lookup"><span data-stu-id="75012-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="75012-122">O contato do NOC é necessário.</span><span class="sxs-lookup"><span data-stu-id="75012-122">NOC Contact is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75012-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75012-123">CommonParameters</span></span>
<span data-ttu-id="75012-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75012-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75012-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75012-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75012-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75012-126">INPUTS</span></span>

### <span data-ttu-id="75012-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="75012-127">None</span></span>

## <span data-ttu-id="75012-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="75012-128">OUTPUTS</span></span>

### <span data-ttu-id="75012-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="75012-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="75012-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="75012-130">NOTES</span></span>

## <span data-ttu-id="75012-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75012-131">RELATED LINKS</span></span>
