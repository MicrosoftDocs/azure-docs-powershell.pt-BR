---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112726"
---
# <span data-ttu-id="9ed67-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="9ed67-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="9ed67-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ed67-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed67-103">Cria um detalhe de contato de memória para PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="9ed67-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="9ed67-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ed67-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ed67-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9ed67-105">DESCRIPTION</span></span>
<span data-ttu-id="9ed67-106">Crie um detalhe de contato PeerAsn na memória.</span><span class="sxs-lookup"><span data-stu-id="9ed67-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="9ed67-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9ed67-107">EXAMPLES</span></span>

### <span data-ttu-id="9ed67-108">Criar detalhes de contato e adicionar ao PeerAsn</span><span class="sxs-lookup"><span data-stu-id="9ed67-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="9ed67-109">Função e email são necessários.</span><span class="sxs-lookup"><span data-stu-id="9ed67-109">Role and email are required.</span></span> <span data-ttu-id="9ed67-110">O telefone é opcional.</span><span class="sxs-lookup"><span data-stu-id="9ed67-110">Phone is optional.</span></span> <span data-ttu-id="9ed67-111">O telefone dá suporte a +-() ou espaços.</span><span class="sxs-lookup"><span data-stu-id="9ed67-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="9ed67-112">Um PeerAsn deve incluir pelo menos um detalhe de contato do tipo "Noc"</span><span class="sxs-lookup"><span data-stu-id="9ed67-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="9ed67-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ed67-113">PARAMETERS</span></span>

### <span data-ttu-id="9ed67-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed67-114">-DefaultProfile</span></span>
<span data-ttu-id="9ed67-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ed67-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ed67-116">-Email</span><span class="sxs-lookup"><span data-stu-id="9ed67-116">-Email</span></span>
<span data-ttu-id="9ed67-117">Endereços de email usados para entrar em contato se os problemas normalmente são uma Central de Operações de Rede</span><span class="sxs-lookup"><span data-stu-id="9ed67-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="9ed67-118">-Telefone</span><span class="sxs-lookup"><span data-stu-id="9ed67-118">-Phone</span></span>
<span data-ttu-id="9ed67-119">Telefone usado para entrar em contato se os problemas normalmente são uma Central de Operações de Rede</span><span class="sxs-lookup"><span data-stu-id="9ed67-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="9ed67-120">-Função</span><span class="sxs-lookup"><span data-stu-id="9ed67-120">-Role</span></span>
<span data-ttu-id="9ed67-121">Escolha a função mais adequada às informações de contato.</span><span class="sxs-lookup"><span data-stu-id="9ed67-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="9ed67-122">O Contato NOC é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="9ed67-122">NOC Contact is required.</span></span>

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

### <span data-ttu-id="9ed67-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed67-123">CommonParameters</span></span>
<span data-ttu-id="9ed67-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ed67-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed67-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ed67-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed67-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="9ed67-126">INPUTS</span></span>

### <span data-ttu-id="9ed67-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9ed67-127">None</span></span>

## <span data-ttu-id="9ed67-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="9ed67-128">OUTPUTS</span></span>

### <span data-ttu-id="9ed67-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="9ed67-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="9ed67-130">Notas</span><span class="sxs-lookup"><span data-stu-id="9ed67-130">NOTES</span></span>

## <span data-ttu-id="9ed67-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ed67-131">RELATED LINKS</span></span>
