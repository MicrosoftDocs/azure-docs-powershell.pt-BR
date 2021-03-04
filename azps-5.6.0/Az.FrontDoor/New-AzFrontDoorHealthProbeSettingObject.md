---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 4d65985d724033244f761748634adb3b2002a199
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887763"
---
# <span data-ttu-id="b68ae-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="b68ae-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="b68ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b68ae-102">SYNOPSIS</span></span>
<span data-ttu-id="b68ae-103">Criar um objeto PSHealthProbeSetting para criação do Front Door</span><span class="sxs-lookup"><span data-stu-id="b68ae-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="b68ae-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b68ae-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b68ae-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b68ae-105">DESCRIPTION</span></span>
<span data-ttu-id="b68ae-106">Criar um objeto PSHealthProbeSetting para criação do Front Door</span><span class="sxs-lookup"><span data-stu-id="b68ae-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="b68ae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b68ae-107">EXAMPLES</span></span>

### <span data-ttu-id="b68ae-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b68ae-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
HealthProbeMethod : Head
EnabledState      : Enabled
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="b68ae-109">Observação: a configuração HealthProbeMethod não é sensível a minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b68ae-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="b68ae-110">Criar um objeto PSHealthProbeSetting para criação do Front Door</span><span class="sxs-lookup"><span data-stu-id="b68ae-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="b68ae-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b68ae-111">PARAMETERS</span></span>

### <span data-ttu-id="b68ae-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b68ae-112">-DefaultProfile</span></span>
<span data-ttu-id="b68ae-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b68ae-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b68ae-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="b68ae-114">-EnabledState</span></span>
<span data-ttu-id="b68ae-115">Se as sondas de saúde devem ser feitas em relação a back-ends definidos em backendPools.</span><span class="sxs-lookup"><span data-stu-id="b68ae-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="b68ae-116">As sondas de saúde só poderão ser desabilitadas se houver um único back-end habilitado no pool de back-back-back habilitado único.</span><span class="sxs-lookup"><span data-stu-id="b68ae-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b68ae-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="b68ae-117">-HealthProbeMethod</span></span>
<span data-ttu-id="b68ae-118">Configura qual método HTTP usar para sondar os backends definidos em backendPools.</span><span class="sxs-lookup"><span data-stu-id="b68ae-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b68ae-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b68ae-119">-IntervalInSeconds</span></span>
<span data-ttu-id="b68ae-120">O número de segundos entre as sondas de saúde.</span><span class="sxs-lookup"><span data-stu-id="b68ae-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="b68ae-121">O valor padrão é 30</span><span class="sxs-lookup"><span data-stu-id="b68ae-121">Default value is 30</span></span>

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

### <span data-ttu-id="b68ae-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b68ae-122">-Name</span></span>
<span data-ttu-id="b68ae-123">Nome da configuração da sonda de saúde.</span><span class="sxs-lookup"><span data-stu-id="b68ae-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="b68ae-124">-Path</span><span class="sxs-lookup"><span data-stu-id="b68ae-124">-Path</span></span>
<span data-ttu-id="b68ae-125">O caminho a ser usado para a sonda de saúde.</span><span class="sxs-lookup"><span data-stu-id="b68ae-125">The path to use for the health probe.</span></span>
<span data-ttu-id="b68ae-126">O padrão é /</span><span class="sxs-lookup"><span data-stu-id="b68ae-126">Default is /</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b68ae-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b68ae-127">-Protocol</span></span>
<span data-ttu-id="b68ae-128">Esquema de protocolo a ser usado para esta sonda O valor padrão é HTTP</span><span class="sxs-lookup"><span data-stu-id="b68ae-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b68ae-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b68ae-129">CommonParameters</span></span>
<span data-ttu-id="b68ae-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b68ae-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b68ae-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b68ae-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b68ae-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b68ae-132">INPUTS</span></span>

### <span data-ttu-id="b68ae-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b68ae-133">None</span></span>
## <span data-ttu-id="b68ae-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b68ae-134">OUTPUTS</span></span>

### <span data-ttu-id="b68ae-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="b68ae-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="b68ae-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="b68ae-136">NOTES</span></span>

## <span data-ttu-id="b68ae-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b68ae-137">RELATED LINKS</span></span>

<span data-ttu-id="b68ae-138">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="b68ae-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
