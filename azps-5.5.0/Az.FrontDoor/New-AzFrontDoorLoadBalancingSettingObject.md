---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: e9195a60b06f206a5b3133834f19cfdab68db31b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126958"
---
# <span data-ttu-id="6bbd5-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="6bbd5-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="6bbd5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6bbd5-102">SYNOPSIS</span></span>
<span data-ttu-id="6bbd5-103">Criar um objeto PSLoad ComncingSetting para criação de Porta Da Frente</span><span class="sxs-lookup"><span data-stu-id="6bbd5-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="6bbd5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6bbd5-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bbd5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6bbd5-105">DESCRIPTION</span></span>
<span data-ttu-id="6bbd5-106">Criar um objeto PSLoad ComncingSetting para criação de Porta Da Frente</span><span class="sxs-lookup"><span data-stu-id="6bbd5-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="6bbd5-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6bbd5-107">EXAMPLES</span></span>

### <span data-ttu-id="6bbd5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6bbd5-108">Example 1</span></span>
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

<span data-ttu-id="6bbd5-109">Criar um objeto PSLoad ComncingSetting para criação de Porta Da Frente</span><span class="sxs-lookup"><span data-stu-id="6bbd5-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="6bbd5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6bbd5-110">PARAMETERS</span></span>

### <span data-ttu-id="6bbd5-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="6bbd5-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="6bbd5-112">A latência adicional em milissegundos para que as sondas caiam no bucket de latência mais baixa.</span><span class="sxs-lookup"><span data-stu-id="6bbd5-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="6bbd5-113">O valor padrão é 0</span><span class="sxs-lookup"><span data-stu-id="6bbd5-113">Default value is 0</span></span>

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

### <span data-ttu-id="6bbd5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bbd5-114">-DefaultProfile</span></span>
<span data-ttu-id="6bbd5-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6bbd5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bbd5-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="6bbd5-116">-Name</span></span>
<span data-ttu-id="6bbd5-117">nome da configuração de problemas de saúde.</span><span class="sxs-lookup"><span data-stu-id="6bbd5-117">health probe setting name.</span></span>

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

### <span data-ttu-id="6bbd5-118">-ExemploSize</span><span class="sxs-lookup"><span data-stu-id="6bbd5-118">-SampleSize</span></span>
<span data-ttu-id="6bbd5-119">O número de amostras a considerar para decisões de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="6bbd5-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="6bbd5-120">O valor padrão é 4</span><span class="sxs-lookup"><span data-stu-id="6bbd5-120">Default value is 4</span></span>

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

### <span data-ttu-id="6bbd5-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="6bbd5-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="6bbd5-122">O número de amostras dentro do período de exemplo que deve ser bem-sucedido O valor padrão é 2</span><span class="sxs-lookup"><span data-stu-id="6bbd5-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="6bbd5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bbd5-123">CommonParameters</span></span>
<span data-ttu-id="6bbd5-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bbd5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bbd5-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bbd5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bbd5-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="6bbd5-126">INPUTS</span></span>

### <span data-ttu-id="6bbd5-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6bbd5-127">None</span></span>

## <span data-ttu-id="6bbd5-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="6bbd5-128">OUTPUTS</span></span>

### <span data-ttu-id="6bbd5-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoad QuencingSetting</span><span class="sxs-lookup"><span data-stu-id="6bbd5-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="6bbd5-130">Notas</span><span class="sxs-lookup"><span data-stu-id="6bbd5-130">NOTES</span></span>

## <span data-ttu-id="6bbd5-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6bbd5-131">RELATED LINKS</span></span>

<span data-ttu-id="6bbd5-132">[Novo-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="6bbd5-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
