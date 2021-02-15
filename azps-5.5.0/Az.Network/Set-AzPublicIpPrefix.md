---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 4244f8c97090009272933d73a64323e4af5dfbbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114079"
---
# <span data-ttu-id="20a40-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20a40-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="20a40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20a40-102">SYNOPSIS</span></span>
<span data-ttu-id="20a40-103">Define as Marcas de um PublicIpPrefix existente</span><span class="sxs-lookup"><span data-stu-id="20a40-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="20a40-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20a40-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20a40-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="20a40-105">DESCRIPTION</span></span>
<span data-ttu-id="20a40-106">O **cmdlet Set-AzPublicIpPrefix define** as Marcas de um prefixo IP público.</span><span class="sxs-lookup"><span data-stu-id="20a40-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="20a40-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="20a40-107">EXAMPLES</span></span>

### <span data-ttu-id="20a40-108">Definir as marcas para prefixo ip público</span><span class="sxs-lookup"><span data-stu-id="20a40-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="20a40-109">O primeiro comando obtém um Prefixo IP público existente, o segundo comando define a Propriedade marcas e o terceiro comando atualiza o objeto existente.</span><span class="sxs-lookup"><span data-stu-id="20a40-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="20a40-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20a40-110">PARAMETERS</span></span>

### <span data-ttu-id="20a40-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20a40-111">-AsJob</span></span>
<span data-ttu-id="20a40-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="20a40-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20a40-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a40-113">-DefaultProfile</span></span>
<span data-ttu-id="20a40-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20a40-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20a40-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20a40-115">-PublicIpPrefix</span></span>
<span data-ttu-id="20a40-116">A PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20a40-116">The PublicIpPrefix</span></span>

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

### <span data-ttu-id="20a40-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="20a40-117">-Confirm</span></span>
<span data-ttu-id="20a40-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20a40-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20a40-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20a40-119">-WhatIf</span></span>
<span data-ttu-id="20a40-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="20a40-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20a40-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20a40-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20a40-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a40-122">CommonParameters</span></span>
<span data-ttu-id="20a40-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20a40-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a40-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20a40-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a40-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="20a40-125">INPUTS</span></span>

### <span data-ttu-id="20a40-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20a40-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="20a40-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="20a40-127">OUTPUTS</span></span>

### <span data-ttu-id="20a40-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20a40-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="20a40-129">Notas</span><span class="sxs-lookup"><span data-stu-id="20a40-129">NOTES</span></span>

## <span data-ttu-id="20a40-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20a40-130">RELATED LINKS</span></span>

[<span data-ttu-id="20a40-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20a40-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="20a40-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20a40-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="20a40-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20a40-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
