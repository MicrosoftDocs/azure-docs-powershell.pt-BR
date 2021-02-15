---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: b47db38e49bdc066fed9637e65d87693738a4776
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118210"
---
# <span data-ttu-id="fdb3a-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="fdb3a-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="fdb3a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fdb3a-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb3a-103">Remover o Peer Asn</span><span class="sxs-lookup"><span data-stu-id="fdb3a-103">Remove Peer Asn</span></span>

## <span data-ttu-id="fdb3a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fdb3a-104">SYNTAX</span></span>

### <span data-ttu-id="fdb3a-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="fdb3a-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb3a-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="fdb3a-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb3a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fdb3a-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdb3a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fdb3a-108">DESCRIPTION</span></span>
<span data-ttu-id="fdb3a-109">Remover um PeerAsn da assinatura.</span><span class="sxs-lookup"><span data-stu-id="fdb3a-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="fdb3a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fdb3a-110">EXAMPLES</span></span>

### <span data-ttu-id="fdb3a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fdb3a-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="fdb3a-112">Remove o Peer Asn</span><span class="sxs-lookup"><span data-stu-id="fdb3a-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="fdb3a-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fdb3a-113">PARAMETERS</span></span>

### <span data-ttu-id="fdb3a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdb3a-114">-AsJob</span></span>
<span data-ttu-id="fdb3a-115">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="fdb3a-115">Run in the background.</span></span>

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

### <span data-ttu-id="fdb3a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb3a-116">-DefaultProfile</span></span>
<span data-ttu-id="fdb3a-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb3a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdb3a-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="fdb3a-118">-Force</span></span>
<span data-ttu-id="fdb3a-119">{{ Fill Force Description }}</span><span class="sxs-lookup"><span data-stu-id="fdb3a-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="fdb3a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdb3a-120">-InputObject</span></span>
<span data-ttu-id="fdb3a-121">O objeto PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="fdb3a-121">The PeerAsn object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb3a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="fdb3a-122">-Name</span></span>
<span data-ttu-id="fdb3a-123">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="fdb3a-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb3a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdb3a-124">-PassThru</span></span>
<span data-ttu-id="fdb3a-125">Retornar verdadeiro se concluído</span><span class="sxs-lookup"><span data-stu-id="fdb3a-125">Return true if complete</span></span>

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

### <span data-ttu-id="fdb3a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdb3a-126">-ResourceId</span></span>
<span data-ttu-id="fdb3a-127">O nome da cadeia de caracteres de ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="fdb3a-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb3a-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fdb3a-128">-Confirm</span></span>
<span data-ttu-id="fdb3a-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdb3a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdb3a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdb3a-130">-WhatIf</span></span>
<span data-ttu-id="fdb3a-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fdb3a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdb3a-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fdb3a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdb3a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb3a-133">CommonParameters</span></span>
<span data-ttu-id="fdb3a-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdb3a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb3a-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fdb3a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb3a-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="fdb3a-136">INPUTS</span></span>

### <span data-ttu-id="fdb3a-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="fdb3a-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="fdb3a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fdb3a-138">System.String</span></span>

## <span data-ttu-id="fdb3a-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="fdb3a-139">OUTPUTS</span></span>

### <span data-ttu-id="fdb3a-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fdb3a-140">System.Boolean</span></span>

## <span data-ttu-id="fdb3a-141">Notas</span><span class="sxs-lookup"><span data-stu-id="fdb3a-141">NOTES</span></span>

## <span data-ttu-id="fdb3a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fdb3a-142">RELATED LINKS</span></span>
