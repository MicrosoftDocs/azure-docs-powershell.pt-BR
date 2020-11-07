---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: d1ff0baeff3bf4b5747ff1d024b0de6e5184688a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942760"
---
# <span data-ttu-id="b8e87-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="b8e87-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="b8e87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8e87-102">SYNOPSIS</span></span>
<span data-ttu-id="b8e87-103">Remover ASN par</span><span class="sxs-lookup"><span data-stu-id="b8e87-103">Remove Peer Asn</span></span>

## <span data-ttu-id="b8e87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8e87-104">SYNTAX</span></span>

### <span data-ttu-id="b8e87-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="b8e87-105">Default (Default)</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8e87-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b8e87-106">ByName</span></span>
```
Remove-AzPeerAsn [-Name] <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8e87-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8e87-107">DESCRIPTION</span></span>
<span data-ttu-id="b8e87-108">Remova um PeerAsn da assinatura.</span><span class="sxs-lookup"><span data-stu-id="b8e87-108">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="b8e87-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8e87-109">EXAMPLES</span></span>

### <span data-ttu-id="b8e87-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8e87-110">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="b8e87-111">Remove o peer ASN</span><span class="sxs-lookup"><span data-stu-id="b8e87-111">Removes the Peer Asn</span></span>

## <span data-ttu-id="b8e87-112">OS</span><span class="sxs-lookup"><span data-stu-id="b8e87-112">PARAMETERS</span></span>

### <span data-ttu-id="b8e87-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8e87-113">-AsJob</span></span>
<span data-ttu-id="b8e87-114">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="b8e87-114">Run in the background.</span></span>

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

### <span data-ttu-id="b8e87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8e87-115">-DefaultProfile</span></span>
<span data-ttu-id="b8e87-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8e87-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8e87-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b8e87-117">-Force</span></span>
<span data-ttu-id="b8e87-118">{{Descrição da força de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="b8e87-118">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="b8e87-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8e87-119">-InputObject</span></span>
<span data-ttu-id="b8e87-120">O objeto PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="b8e87-120">The PeerAsn object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8e87-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8e87-121">-Name</span></span>
<span data-ttu-id="b8e87-122">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="b8e87-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e87-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8e87-123">-PassThru</span></span>
<span data-ttu-id="b8e87-124">Retornar true se concluir</span><span class="sxs-lookup"><span data-stu-id="b8e87-124">Return true if complete</span></span>

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

### <span data-ttu-id="b8e87-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b8e87-125">-Confirm</span></span>
<span data-ttu-id="b8e87-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8e87-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8e87-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8e87-127">-WhatIf</span></span>
<span data-ttu-id="b8e87-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8e87-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8e87-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8e87-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8e87-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8e87-130">CommonParameters</span></span>
<span data-ttu-id="b8e87-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8e87-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8e87-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8e87-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8e87-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8e87-133">INPUTS</span></span>

### <span data-ttu-id="b8e87-134">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="b8e87-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="b8e87-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8e87-135">OUTPUTS</span></span>

### <span data-ttu-id="b8e87-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b8e87-136">System.Boolean</span></span>

## <span data-ttu-id="b8e87-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8e87-137">NOTES</span></span>

## <span data-ttu-id="b8e87-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8e87-138">RELATED LINKS</span></span>
