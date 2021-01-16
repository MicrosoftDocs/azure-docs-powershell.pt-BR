---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272551"
---
# <span data-ttu-id="e5054-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="e5054-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="e5054-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5054-102">SYNOPSIS</span></span>
<span data-ttu-id="e5054-103">Cria um detalhe de contato na memória para PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="e5054-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="e5054-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5054-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5054-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5054-105">DESCRIPTION</span></span>
<span data-ttu-id="e5054-106">Crie um detalhe de contato do PeerAsn de memória.</span><span class="sxs-lookup"><span data-stu-id="e5054-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="e5054-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5054-107">EXAMPLES</span></span>

### <span data-ttu-id="e5054-108">Criar um detalhe de contato e adicionar ao PeerAsn</span><span class="sxs-lookup"><span data-stu-id="e5054-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="e5054-109">A função e o e-mail são obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="e5054-109">Role and email are required.</span></span> <span data-ttu-id="e5054-110">O telefone é opcional.</span><span class="sxs-lookup"><span data-stu-id="e5054-110">Phone is optional.</span></span> <span data-ttu-id="e5054-111">Telefone compatível com +-() ou espaços.</span><span class="sxs-lookup"><span data-stu-id="e5054-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="e5054-112">Um PeerAsn deve incluir pelo menos um detalhe de contato do tipo "NOC"</span><span class="sxs-lookup"><span data-stu-id="e5054-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="e5054-113">OS</span><span class="sxs-lookup"><span data-stu-id="e5054-113">PARAMETERS</span></span>

### <span data-ttu-id="e5054-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5054-114">-DefaultProfile</span></span>
<span data-ttu-id="e5054-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5054-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5054-116">-Email</span><span class="sxs-lookup"><span data-stu-id="e5054-116">-Email</span></span>
<span data-ttu-id="e5054-117">Endereços de email usados para entrar em contato se os problemas arrise normalmente um centro de operações de rede</span><span class="sxs-lookup"><span data-stu-id="e5054-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="e5054-118">-Telefone</span><span class="sxs-lookup"><span data-stu-id="e5054-118">-Phone</span></span>
<span data-ttu-id="e5054-119">Telefone usado para entrar em contato se os problemas arrise normalmente um centro de operações de rede</span><span class="sxs-lookup"><span data-stu-id="e5054-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="e5054-120">-Função</span><span class="sxs-lookup"><span data-stu-id="e5054-120">-Role</span></span>
<span data-ttu-id="e5054-121">Escolha a função que melhor se adapta às informações de contato.</span><span class="sxs-lookup"><span data-stu-id="e5054-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="e5054-122">O contato do NOC é necessário.</span><span class="sxs-lookup"><span data-stu-id="e5054-122">NOC Contact is required.</span></span>

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

### <span data-ttu-id="e5054-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5054-123">CommonParameters</span></span>
<span data-ttu-id="e5054-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5054-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5054-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5054-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5054-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5054-126">INPUTS</span></span>

### <span data-ttu-id="e5054-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e5054-127">None</span></span>

## <span data-ttu-id="e5054-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5054-128">OUTPUTS</span></span>

### <span data-ttu-id="e5054-129">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="e5054-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="e5054-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5054-130">NOTES</span></span>

## <span data-ttu-id="e5054-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5054-131">RELATED LINKS</span></span>
