---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114092"
---
# <span data-ttu-id="fd36a-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="fd36a-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="fd36a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd36a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd36a-103">Salva um Firewall modificado.</span><span class="sxs-lookup"><span data-stu-id="fd36a-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="fd36a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd36a-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd36a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd36a-105">DESCRIPTION</span></span>
<span data-ttu-id="fd36a-106">O **cmdlet Set-AzIpGroup** atualiza um Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="fd36a-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="fd36a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fd36a-107">EXAMPLES</span></span>

### <span data-ttu-id="fd36a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fd36a-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="fd36a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd36a-109">PARAMETERS</span></span>

### <span data-ttu-id="fd36a-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd36a-110">-AsJob</span></span>
<span data-ttu-id="fd36a-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fd36a-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd36a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd36a-112">-DefaultProfile</span></span>
<span data-ttu-id="fd36a-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd36a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd36a-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="fd36a-114">-IpGroup</span></span>
<span data-ttu-id="fd36a-115">O IpGroup</span><span class="sxs-lookup"><span data-stu-id="fd36a-115">The IpGroup</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd36a-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fd36a-116">-Confirm</span></span>
<span data-ttu-id="fd36a-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd36a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd36a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd36a-118">-WhatIf</span></span>
<span data-ttu-id="fd36a-119">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fd36a-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd36a-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd36a-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd36a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd36a-121">CommonParameters</span></span>
<span data-ttu-id="fd36a-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd36a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd36a-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd36a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd36a-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="fd36a-124">INPUTS</span></span>

### <span data-ttu-id="fd36a-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="fd36a-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="fd36a-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="fd36a-126">OUTPUTS</span></span>

### <span data-ttu-id="fd36a-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="fd36a-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="fd36a-128">Notas</span><span class="sxs-lookup"><span data-stu-id="fd36a-128">NOTES</span></span>

## <span data-ttu-id="fd36a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd36a-129">RELATED LINKS</span></span>
