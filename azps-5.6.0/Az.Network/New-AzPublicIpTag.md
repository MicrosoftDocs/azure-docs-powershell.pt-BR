---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 2f46b13570ef1f538658dae6d02000848822c150
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885622"
---
# <span data-ttu-id="bd5f5-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="bd5f5-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="bd5f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd5f5-102">SYNOPSIS</span></span>
<span data-ttu-id="bd5f5-103">Cria uma marca IP.</span><span class="sxs-lookup"><span data-stu-id="bd5f5-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="bd5f5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bd5f5-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd5f5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bd5f5-105">DESCRIPTION</span></span>
<span data-ttu-id="bd5f5-106">O cmdlet **New-AzPublicIpTag** cria uma marca IP.</span><span class="sxs-lookup"><span data-stu-id="bd5f5-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="bd5f5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd5f5-107">EXAMPLES</span></span>

### <span data-ttu-id="bd5f5-108">Exemplo 1: Criar uma nova marca IP</span><span class="sxs-lookup"><span data-stu-id="bd5f5-108">Example 1: Create a new IP Tag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="bd5f5-109">Este comando cria uma nova Marca IP com o Tagtype como "FirstPartyUsage" e marca como "/Sql".</span><span class="sxs-lookup"><span data-stu-id="bd5f5-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="bd5f5-110">Isso é usado na criação publicIpAddress com essas marcas específicas para alocação.</span><span class="sxs-lookup"><span data-stu-id="bd5f5-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="bd5f5-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bd5f5-111">PARAMETERS</span></span>

### <span data-ttu-id="bd5f5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd5f5-112">-DefaultProfile</span></span>
<span data-ttu-id="bd5f5-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="bd5f5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd5f5-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="bd5f5-114">-IpTagType</span></span>
<span data-ttu-id="bd5f5-115">Tipo IpTag Exemplo:FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="bd5f5-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd5f5-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="bd5f5-116">-Tag</span></span>
<span data-ttu-id="bd5f5-117">Valor IpTag Example:/Sql</span><span class="sxs-lookup"><span data-stu-id="bd5f5-117">IpTag value Example:/Sql</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd5f5-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd5f5-118">-Confirm</span></span>
<span data-ttu-id="bd5f5-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd5f5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd5f5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd5f5-120">-WhatIf</span></span>
<span data-ttu-id="bd5f5-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bd5f5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd5f5-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bd5f5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd5f5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd5f5-123">CommonParameters</span></span>
<span data-ttu-id="bd5f5-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd5f5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd5f5-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd5f5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd5f5-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd5f5-126">INPUTS</span></span>

### <span data-ttu-id="bd5f5-127">System.String</span><span class="sxs-lookup"><span data-stu-id="bd5f5-127">System.String</span></span>

## <span data-ttu-id="bd5f5-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bd5f5-128">OUTPUTS</span></span>

### <span data-ttu-id="bd5f5-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="bd5f5-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="bd5f5-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="bd5f5-130">NOTES</span></span>

## <span data-ttu-id="bd5f5-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd5f5-131">RELATED LINKS</span></span>
