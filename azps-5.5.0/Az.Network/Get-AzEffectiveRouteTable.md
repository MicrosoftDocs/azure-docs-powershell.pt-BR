---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: e7d65e7797fb606306f0f0cc1e7c394fcf3d1d3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114708"
---
# <span data-ttu-id="edd71-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="edd71-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="edd71-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="edd71-102">SYNOPSIS</span></span>
<span data-ttu-id="edd71-103">Obtém a tabela de rota eficaz de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="edd71-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="edd71-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="edd71-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edd71-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="edd71-105">DESCRIPTION</span></span>
<span data-ttu-id="edd71-106">O cmdlet **Get-AzEffectiveRouteTable** retorna a tabela de rota efetiva aplicada em uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="edd71-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="edd71-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="edd71-107">EXAMPLES</span></span>

### <span data-ttu-id="edd71-108">Exemplo 1: Obter a tabela de rota eficaz em uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="edd71-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="edd71-109">Esse comando obtém a tabela de rota eficaz associada à interface de rede chamada MyNetworkInterface no grupo de recursos chamado MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="edd71-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="edd71-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="edd71-110">PARAMETERS</span></span>

### <span data-ttu-id="edd71-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="edd71-111">-AsJob</span></span>
<span data-ttu-id="edd71-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="edd71-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="edd71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd71-113">-DefaultProfile</span></span>
<span data-ttu-id="edd71-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="edd71-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edd71-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="edd71-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="edd71-116">Especificou o nome de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="edd71-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="edd71-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edd71-117">-ResourceGroupName</span></span>
<span data-ttu-id="edd71-118">Especifica o grupo de recursos de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="edd71-118">Specifies the resource group of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edd71-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd71-119">CommonParameters</span></span>
<span data-ttu-id="edd71-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edd71-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd71-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edd71-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd71-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="edd71-122">INPUTS</span></span>

### <span data-ttu-id="edd71-123">System.String</span><span class="sxs-lookup"><span data-stu-id="edd71-123">System.String</span></span>

## <span data-ttu-id="edd71-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="edd71-124">OUTPUTS</span></span>

### <span data-ttu-id="edd71-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="edd71-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="edd71-126">Notas</span><span class="sxs-lookup"><span data-stu-id="edd71-126">NOTES</span></span>

## <span data-ttu-id="edd71-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="edd71-127">RELATED LINKS</span></span>

[<span data-ttu-id="edd71-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="edd71-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


