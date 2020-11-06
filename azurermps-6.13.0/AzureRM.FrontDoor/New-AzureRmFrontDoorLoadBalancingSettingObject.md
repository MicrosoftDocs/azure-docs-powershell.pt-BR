---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: de13a33aeaf60dbd83fcacebb8380bee27c18c46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428480"
---
# <span data-ttu-id="ceed7-101">New-AzureRmFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="ceed7-101">New-AzureRmFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="ceed7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ceed7-102">SYNOPSIS</span></span>
<span data-ttu-id="ceed7-103">Criar um objeto PSLoadBalancingSetting para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="ceed7-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ceed7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ceed7-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceed7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ceed7-105">DESCRIPTION</span></span>
<span data-ttu-id="ceed7-106">Criar um objeto PSLoadBalancingSetting para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="ceed7-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="ceed7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ceed7-107">EXAMPLES</span></span>

### <span data-ttu-id="ceed7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ceed7-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="ceed7-109">Criar um objeto PSLoadBalancingSetting para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="ceed7-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="ceed7-110">OS</span><span class="sxs-lookup"><span data-stu-id="ceed7-110">PARAMETERS</span></span>

### <span data-ttu-id="ceed7-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="ceed7-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="ceed7-112">A latência adicional em milissegundos para testes se enquadram no Bucket de latência mais baixa.</span><span class="sxs-lookup"><span data-stu-id="ceed7-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="ceed7-113">O valor padrão é 0</span><span class="sxs-lookup"><span data-stu-id="ceed7-113">Default value is 0</span></span>

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

### <span data-ttu-id="ceed7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceed7-114">-DefaultProfile</span></span>
<span data-ttu-id="ceed7-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ceed7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceed7-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ceed7-116">-Name</span></span>
<span data-ttu-id="ceed7-117">nome da configuração de investigação de integridade.</span><span class="sxs-lookup"><span data-stu-id="ceed7-117">health probe setting name.</span></span>

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

### <span data-ttu-id="ceed7-118">-Exemplo</span><span class="sxs-lookup"><span data-stu-id="ceed7-118">-SampleSize</span></span>
<span data-ttu-id="ceed7-119">O número de amostras a serem consideradas para decisões de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="ceed7-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="ceed7-120">O valor padrão é 4</span><span class="sxs-lookup"><span data-stu-id="ceed7-120">Default value is 4</span></span>

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

### <span data-ttu-id="ceed7-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="ceed7-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="ceed7-122">O número de amostras dentro do período de amostra que deve conseguir valor padrão é 2</span><span class="sxs-lookup"><span data-stu-id="ceed7-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="ceed7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceed7-123">CommonParameters</span></span>
<span data-ttu-id="ceed7-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceed7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceed7-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceed7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceed7-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ceed7-126">INPUTS</span></span>

### <span data-ttu-id="ceed7-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ceed7-127">None</span></span>

## <span data-ttu-id="ceed7-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ceed7-128">OUTPUTS</span></span>

### <span data-ttu-id="ceed7-129">Microsoft. Azure. Commands. FrontDoor. Models. PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="ceed7-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="ceed7-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ceed7-130">NOTES</span></span>

## <span data-ttu-id="ceed7-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ceed7-131">RELATED LINKS</span></span>

<span data-ttu-id="ceed7-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="ceed7-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
