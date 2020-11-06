---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 7b60c157f3e86e72461c82f34a2d23dcb5eb0b20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426317"
---
# <span data-ttu-id="a8be1-101">Set-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a8be1-101">Set-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="a8be1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a8be1-102">SYNOPSIS</span></span>
<span data-ttu-id="a8be1-103">Define as marcas para um PublicIpPrefix existente</span><span class="sxs-lookup"><span data-stu-id="a8be1-103">Sets the Tags for an existing PublicIpPrefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8be1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8be1-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8be1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a8be1-105">DESCRIPTION</span></span>
<span data-ttu-id="a8be1-106">O cmdlet **set-AzureRmPublicIpPrefix** define as marcas para um prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="a8be1-106">The **Set-AzureRmPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="a8be1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8be1-107">EXAMPLES</span></span>

### <span data-ttu-id="a8be1-108">Definir as marcas do prefixo de IP público</span><span class="sxs-lookup"><span data-stu-id="a8be1-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzureRmPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="a8be1-109">O primeiro comando obtém um prefixo de IP público existente, o segundo comando define a propriedade Tags e o terceiro comando atualiza o objeto existente.</span><span class="sxs-lookup"><span data-stu-id="a8be1-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="a8be1-110">OS</span><span class="sxs-lookup"><span data-stu-id="a8be1-110">PARAMETERS</span></span>

### <span data-ttu-id="a8be1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8be1-111">-AsJob</span></span>
<span data-ttu-id="a8be1-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a8be1-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8be1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8be1-113">-DefaultProfile</span></span>
<span data-ttu-id="a8be1-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a8be1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8be1-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a8be1-115">-PublicIpPrefix</span></span>
<span data-ttu-id="a8be1-116">O PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a8be1-116">The PublicIpPrefix</span></span>

```yaml
Type: PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8be1-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a8be1-117">-Confirm</span></span>
<span data-ttu-id="a8be1-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8be1-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8be1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8be1-119">-WhatIf</span></span>
<span data-ttu-id="a8be1-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a8be1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8be1-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a8be1-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8be1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8be1-122">CommonParameters</span></span>
<span data-ttu-id="a8be1-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8be1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a8be1-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8be1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8be1-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a8be1-125">INPUTS</span></span>

### <span data-ttu-id="a8be1-126">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a8be1-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="a8be1-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a8be1-127">OUTPUTS</span></span>

### <span data-ttu-id="a8be1-128">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a8be1-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="a8be1-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a8be1-129">NOTES</span></span>

## <span data-ttu-id="a8be1-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8be1-130">RELATED LINKS</span></span>
