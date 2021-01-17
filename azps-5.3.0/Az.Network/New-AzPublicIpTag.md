---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 5d7d73b3c7f49babc9e80929dab7b3fa2adad20a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427548"
---
# <span data-ttu-id="f88ab-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="f88ab-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="f88ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f88ab-102">SYNOPSIS</span></span>
<span data-ttu-id="f88ab-103">Cria uma marca de IP.</span><span class="sxs-lookup"><span data-stu-id="f88ab-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="f88ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f88ab-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f88ab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f88ab-105">DESCRIPTION</span></span>
<span data-ttu-id="f88ab-106">O cmdlet **New-AzPublicIpTag** cria uma marca de IP.</span><span class="sxs-lookup"><span data-stu-id="f88ab-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="f88ab-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f88ab-107">EXAMPLES</span></span>

### <span data-ttu-id="f88ab-108">Exemplo 1: criar uma nova marca de IP</span><span class="sxs-lookup"><span data-stu-id="f88ab-108">Example 1: Create a new IP Tag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="f88ab-109">Esse comando cria uma nova marca de IP com o TagType como "FirstPartyUsage" e marca como "/SQL".</span><span class="sxs-lookup"><span data-stu-id="f88ab-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="f88ab-110">Isso é usado na criação do publicIpAddress com essas marcas específicas para alocação.</span><span class="sxs-lookup"><span data-stu-id="f88ab-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="f88ab-111">OS</span><span class="sxs-lookup"><span data-stu-id="f88ab-111">PARAMETERS</span></span>

### <span data-ttu-id="f88ab-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f88ab-112">-DefaultProfile</span></span>
<span data-ttu-id="f88ab-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f88ab-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f88ab-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="f88ab-114">-IpTagType</span></span>
<span data-ttu-id="f88ab-115">IpTag digite o exemplo: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="f88ab-115">IpTag type Example:FirstPartyUsage</span></span>

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

### <span data-ttu-id="f88ab-116">-Marca</span><span class="sxs-lookup"><span data-stu-id="f88ab-116">-Tag</span></span>
<span data-ttu-id="f88ab-117">Valor IpTag exemplo:/SQL</span><span class="sxs-lookup"><span data-stu-id="f88ab-117">IpTag value Example:/Sql</span></span>

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

### <span data-ttu-id="f88ab-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f88ab-118">-Confirm</span></span>
<span data-ttu-id="f88ab-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f88ab-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f88ab-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f88ab-120">-WhatIf</span></span>
<span data-ttu-id="f88ab-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f88ab-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f88ab-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f88ab-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f88ab-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f88ab-123">CommonParameters</span></span>
<span data-ttu-id="f88ab-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f88ab-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f88ab-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f88ab-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f88ab-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f88ab-126">INPUTS</span></span>

### <span data-ttu-id="f88ab-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f88ab-127">System.String</span></span>

## <span data-ttu-id="f88ab-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f88ab-128">OUTPUTS</span></span>

### <span data-ttu-id="f88ab-129">Microsoft. Azure. Commands. Network. Models. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="f88ab-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="f88ab-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f88ab-130">NOTES</span></span>

## <span data-ttu-id="f88ab-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f88ab-131">RELATED LINKS</span></span>
