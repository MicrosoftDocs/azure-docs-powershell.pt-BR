---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: e9195a60b06f206a5b3133834f19cfdab68db31b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117413"
---
# <span data-ttu-id="dc09a-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="dc09a-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="dc09a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc09a-102">SYNOPSIS</span></span>
<span data-ttu-id="dc09a-103">Criar um objeto PSLoadBalancingSetting para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="dc09a-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="dc09a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc09a-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc09a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc09a-105">DESCRIPTION</span></span>
<span data-ttu-id="dc09a-106">Criar um objeto PSLoadBalancingSetting para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="dc09a-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="dc09a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc09a-107">EXAMPLES</span></span>

### <span data-ttu-id="dc09a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dc09a-108">Example 1</span></span>
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

<span data-ttu-id="dc09a-109">Criar um objeto PSLoadBalancingSetting para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="dc09a-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="dc09a-110">OS</span><span class="sxs-lookup"><span data-stu-id="dc09a-110">PARAMETERS</span></span>

### <span data-ttu-id="dc09a-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="dc09a-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="dc09a-112">A latência adicional em milissegundos para testes se enquadram no Bucket de latência mais baixa.</span><span class="sxs-lookup"><span data-stu-id="dc09a-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="dc09a-113">O valor padrão é 0</span><span class="sxs-lookup"><span data-stu-id="dc09a-113">Default value is 0</span></span>

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

### <span data-ttu-id="dc09a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc09a-114">-DefaultProfile</span></span>
<span data-ttu-id="dc09a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc09a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc09a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc09a-116">-Name</span></span>
<span data-ttu-id="dc09a-117">nome da configuração de investigação de integridade.</span><span class="sxs-lookup"><span data-stu-id="dc09a-117">health probe setting name.</span></span>

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

### <span data-ttu-id="dc09a-118">-Exemplo</span><span class="sxs-lookup"><span data-stu-id="dc09a-118">-SampleSize</span></span>
<span data-ttu-id="dc09a-119">O número de amostras a serem consideradas para decisões de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="dc09a-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="dc09a-120">O valor padrão é 4</span><span class="sxs-lookup"><span data-stu-id="dc09a-120">Default value is 4</span></span>

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

### <span data-ttu-id="dc09a-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="dc09a-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="dc09a-122">O número de amostras dentro do período de amostra que deve conseguir valor padrão é 2</span><span class="sxs-lookup"><span data-stu-id="dc09a-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="dc09a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc09a-123">CommonParameters</span></span>
<span data-ttu-id="dc09a-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc09a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc09a-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc09a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc09a-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc09a-126">INPUTS</span></span>

### <span data-ttu-id="dc09a-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="dc09a-127">None</span></span>

## <span data-ttu-id="dc09a-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc09a-128">OUTPUTS</span></span>

### <span data-ttu-id="dc09a-129">Microsoft. Azure. Commands. FrontDoor. Models. PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="dc09a-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="dc09a-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc09a-130">NOTES</span></span>

## <span data-ttu-id="dc09a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc09a-131">RELATED LINKS</span></span>

<span data-ttu-id="dc09a-132">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="dc09a-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
