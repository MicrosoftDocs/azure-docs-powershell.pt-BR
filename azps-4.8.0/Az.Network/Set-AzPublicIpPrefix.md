---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 4244f8c97090009272933d73a64323e4af5dfbbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110420"
---
# <span data-ttu-id="fec05-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fec05-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="fec05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fec05-102">SYNOPSIS</span></span>
<span data-ttu-id="fec05-103">Define as marcas para um PublicIpPrefix existente</span><span class="sxs-lookup"><span data-stu-id="fec05-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="fec05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fec05-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fec05-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fec05-105">DESCRIPTION</span></span>
<span data-ttu-id="fec05-106">O cmdlet **set-AzPublicIpPrefix** define as marcas para um prefixo de IP público.</span><span class="sxs-lookup"><span data-stu-id="fec05-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="fec05-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fec05-107">EXAMPLES</span></span>

### <span data-ttu-id="fec05-108">Definir as marcas do prefixo de IP público</span><span class="sxs-lookup"><span data-stu-id="fec05-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="fec05-109">O primeiro comando obtém um prefixo de IP público existente, o segundo comando define a propriedade Tags e o terceiro comando atualiza o objeto existente.</span><span class="sxs-lookup"><span data-stu-id="fec05-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="fec05-110">OS</span><span class="sxs-lookup"><span data-stu-id="fec05-110">PARAMETERS</span></span>

### <span data-ttu-id="fec05-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fec05-111">-AsJob</span></span>
<span data-ttu-id="fec05-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fec05-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fec05-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fec05-113">-DefaultProfile</span></span>
<span data-ttu-id="fec05-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fec05-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fec05-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fec05-115">-PublicIpPrefix</span></span>
<span data-ttu-id="fec05-116">O PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fec05-116">The PublicIpPrefix</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fec05-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fec05-117">-Confirm</span></span>
<span data-ttu-id="fec05-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fec05-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fec05-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fec05-119">-WhatIf</span></span>
<span data-ttu-id="fec05-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fec05-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fec05-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fec05-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fec05-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec05-122">CommonParameters</span></span>
<span data-ttu-id="fec05-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fec05-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec05-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fec05-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec05-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fec05-125">INPUTS</span></span>

### <span data-ttu-id="fec05-126">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fec05-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="fec05-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fec05-127">OUTPUTS</span></span>

### <span data-ttu-id="fec05-128">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fec05-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="fec05-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fec05-129">NOTES</span></span>

## <span data-ttu-id="fec05-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fec05-130">RELATED LINKS</span></span>

[<span data-ttu-id="fec05-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fec05-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="fec05-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fec05-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="fec05-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fec05-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
