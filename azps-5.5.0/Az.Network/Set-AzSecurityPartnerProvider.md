---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 07a29a17a1a7c17a0bbf7b202b019e7d833a5050
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118258"
---
# <span data-ttu-id="1d888-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1d888-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="1d888-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1d888-102">SYNOPSIS</span></span>
<span data-ttu-id="1d888-103">Salva um Azure SecurityPartnerProvider modificado.</span><span class="sxs-lookup"><span data-stu-id="1d888-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="1d888-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d888-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d888-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d888-105">DESCRIPTION</span></span>
<span data-ttu-id="1d888-106">O cmdlet **Set-AzSecurityPartnerProvider** atualiza um Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1d888-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="1d888-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1d888-107">EXAMPLES</span></span>

### <span data-ttu-id="1d888-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1d888-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="1d888-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d888-109">PARAMETERS</span></span>

### <span data-ttu-id="1d888-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d888-110">-AsJob</span></span>
<span data-ttu-id="1d888-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1d888-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d888-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d888-112">-DefaultProfile</span></span>
<span data-ttu-id="1d888-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1d888-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d888-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1d888-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="1d888-115">O SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1d888-115">The SecurityPartnerProvider</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d888-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1d888-116">-Confirm</span></span>
<span data-ttu-id="1d888-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d888-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d888-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d888-118">-WhatIf</span></span>
<span data-ttu-id="1d888-119">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1d888-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d888-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1d888-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d888-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d888-121">CommonParameters</span></span>
<span data-ttu-id="1d888-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d888-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d888-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d888-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d888-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="1d888-124">INPUTS</span></span>

### <span data-ttu-id="1d888-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1d888-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="1d888-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="1d888-126">OUTPUTS</span></span>

### <span data-ttu-id="1d888-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1d888-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="1d888-128">Notas</span><span class="sxs-lookup"><span data-stu-id="1d888-128">NOTES</span></span>

## <span data-ttu-id="1d888-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d888-129">RELATED LINKS</span></span>
