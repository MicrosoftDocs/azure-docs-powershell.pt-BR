---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: 840c4db17e81f93fc40c86f7c22129b570583bd5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887760"
---
# <span data-ttu-id="eab01-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="eab01-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="eab01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eab01-102">SYNOPSIS</span></span>
<span data-ttu-id="eab01-103">Criar um objeto PSLoadBalancingSetting para criação do Front Door</span><span class="sxs-lookup"><span data-stu-id="eab01-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="eab01-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="eab01-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eab01-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="eab01-105">DESCRIPTION</span></span>
<span data-ttu-id="eab01-106">Criar um objeto PSLoadBalancingSetting para criação do Front Door</span><span class="sxs-lookup"><span data-stu-id="eab01-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="eab01-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eab01-107">EXAMPLES</span></span>

### <span data-ttu-id="eab01-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eab01-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="eab01-109">Criar um objeto PSLoadBalancingSetting para criação do Front Door</span><span class="sxs-lookup"><span data-stu-id="eab01-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="eab01-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="eab01-110">PARAMETERS</span></span>

### <span data-ttu-id="eab01-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="eab01-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="eab01-112">A latência adicional em milissegundos para que as sondas caiam no bucket de latência mais baixo.</span><span class="sxs-lookup"><span data-stu-id="eab01-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="eab01-113">O valor padrão é 0</span><span class="sxs-lookup"><span data-stu-id="eab01-113">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eab01-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eab01-114">-DefaultProfile</span></span>
<span data-ttu-id="eab01-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eab01-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eab01-116">-Name</span><span class="sxs-lookup"><span data-stu-id="eab01-116">-Name</span></span>
<span data-ttu-id="eab01-117">nome da configuração da sonda de saúde.</span><span class="sxs-lookup"><span data-stu-id="eab01-117">health probe setting name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eab01-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="eab01-118">-SampleSize</span></span>
<span data-ttu-id="eab01-119">O número de exemplos a considerar para decisões de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="eab01-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="eab01-120">O valor padrão é 4</span><span class="sxs-lookup"><span data-stu-id="eab01-120">Default value is 4</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eab01-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="eab01-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="eab01-122">O número de amostras dentro do período de exemplo que deve ser bem-sucedido Valor padrão é 2</span><span class="sxs-lookup"><span data-stu-id="eab01-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eab01-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eab01-123">CommonParameters</span></span>
<span data-ttu-id="eab01-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eab01-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eab01-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eab01-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eab01-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eab01-126">INPUTS</span></span>

### <span data-ttu-id="eab01-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="eab01-127">None</span></span>

## <span data-ttu-id="eab01-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="eab01-128">OUTPUTS</span></span>

### <span data-ttu-id="eab01-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="eab01-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="eab01-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="eab01-130">NOTES</span></span>

## <span data-ttu-id="eab01-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eab01-131">RELATED LINKS</span></span>

<span data-ttu-id="eab01-132">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="eab01-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
