---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 5d7d73b3c7f49babc9e80929dab7b3fa2adad20a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114680"
---
# <span data-ttu-id="b9eea-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="b9eea-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="b9eea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9eea-102">SYNOPSIS</span></span>
<span data-ttu-id="b9eea-103">Cria uma marca IP.</span><span class="sxs-lookup"><span data-stu-id="b9eea-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="b9eea-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9eea-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9eea-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9eea-105">DESCRIPTION</span></span>
<span data-ttu-id="b9eea-106">O **cmdlet New-AzPublicIpTag** cria uma Marca IP.</span><span class="sxs-lookup"><span data-stu-id="b9eea-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="b9eea-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b9eea-107">EXAMPLES</span></span>

### <span data-ttu-id="b9eea-108">Exemplo 1: Criar uma nova marca IP</span><span class="sxs-lookup"><span data-stu-id="b9eea-108">Example 1: Create a new IP Tag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="b9eea-109">Esse comando cria uma nova Marca IP com o Tagtype, como "FirstPartyUsage" e uma marca como "/Sql".</span><span class="sxs-lookup"><span data-stu-id="b9eea-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="b9eea-110">Isso é usado na criação de publicIpAddress com essas marcas específicas para alocação.</span><span class="sxs-lookup"><span data-stu-id="b9eea-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="b9eea-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9eea-111">PARAMETERS</span></span>

### <span data-ttu-id="b9eea-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9eea-112">-DefaultProfile</span></span>
<span data-ttu-id="b9eea-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b9eea-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9eea-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="b9eea-114">-IpTagType</span></span>
<span data-ttu-id="b9eea-115">Exemplo de tipo IpTag:FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="b9eea-115">IpTag type Example:FirstPartyUsage</span></span>

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

### <span data-ttu-id="b9eea-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="b9eea-116">-Tag</span></span>
<span data-ttu-id="b9eea-117">Exemplo de valor IpTag:/Sql</span><span class="sxs-lookup"><span data-stu-id="b9eea-117">IpTag value Example:/Sql</span></span>

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

### <span data-ttu-id="b9eea-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b9eea-118">-Confirm</span></span>
<span data-ttu-id="b9eea-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9eea-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9eea-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9eea-120">-WhatIf</span></span>
<span data-ttu-id="b9eea-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b9eea-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9eea-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9eea-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9eea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9eea-123">CommonParameters</span></span>
<span data-ttu-id="b9eea-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9eea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9eea-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9eea-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9eea-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="b9eea-126">INPUTS</span></span>

### <span data-ttu-id="b9eea-127">System.String</span><span class="sxs-lookup"><span data-stu-id="b9eea-127">System.String</span></span>

## <span data-ttu-id="b9eea-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="b9eea-128">OUTPUTS</span></span>

### <span data-ttu-id="b9eea-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="b9eea-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="b9eea-130">Notas</span><span class="sxs-lookup"><span data-stu-id="b9eea-130">NOTES</span></span>

## <span data-ttu-id="b9eea-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9eea-131">RELATED LINKS</span></span>
