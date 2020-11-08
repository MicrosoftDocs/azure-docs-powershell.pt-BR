---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 850db31354ebe4a717a5064c7fed56dc94bf1f0d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114944"
---
# <span data-ttu-id="f90a9-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="f90a9-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="f90a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f90a9-102">SYNOPSIS</span></span>
<span data-ttu-id="f90a9-103">Criar um objeto PSHealthProbeSetting para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="f90a9-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="f90a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f90a9-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f90a9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f90a9-105">DESCRIPTION</span></span>
<span data-ttu-id="f90a9-106">Criar um objeto PSHealthProbeSetting para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="f90a9-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="f90a9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f90a9-107">EXAMPLES</span></span>

### <span data-ttu-id="f90a9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f90a9-108">Example 1</span></span>
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

<span data-ttu-id="f90a9-109">Observação: a configuração HealthProbeMethod não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f90a9-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="f90a9-110">Criar um objeto PSHealthProbeSetting para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="f90a9-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="f90a9-111">OS</span><span class="sxs-lookup"><span data-stu-id="f90a9-111">PARAMETERS</span></span>

### <span data-ttu-id="f90a9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f90a9-112">-DefaultProfile</span></span>
<span data-ttu-id="f90a9-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f90a9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f90a9-114">-Enabledstate</span><span class="sxs-lookup"><span data-stu-id="f90a9-114">-EnabledState</span></span>
<span data-ttu-id="f90a9-115">Se devem ser habilitados testes de integridade a serem feitos em backends definidos em backendPools.</span><span class="sxs-lookup"><span data-stu-id="f90a9-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="f90a9-116">Os testes de integridade só podem ser desabilitados se houver um único backend habilitado em um único pool de back-end habilitado.</span><span class="sxs-lookup"><span data-stu-id="f90a9-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

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

### <span data-ttu-id="f90a9-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="f90a9-117">-HealthProbeMethod</span></span>
<span data-ttu-id="f90a9-118">Configura qual método HTTP usar para testar os backends definidos em backendPools.</span><span class="sxs-lookup"><span data-stu-id="f90a9-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

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

### <span data-ttu-id="f90a9-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="f90a9-119">-IntervalInSeconds</span></span>
<span data-ttu-id="f90a9-120">O número de segundos entre testes de integridade.</span><span class="sxs-lookup"><span data-stu-id="f90a9-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="f90a9-121">O valor padrão é 30</span><span class="sxs-lookup"><span data-stu-id="f90a9-121">Default value is 30</span></span>

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

### <span data-ttu-id="f90a9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f90a9-122">-Name</span></span>
<span data-ttu-id="f90a9-123">Nome da configuração de investigação de integridade.</span><span class="sxs-lookup"><span data-stu-id="f90a9-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="f90a9-124">-Caminho</span><span class="sxs-lookup"><span data-stu-id="f90a9-124">-Path</span></span>
<span data-ttu-id="f90a9-125">O caminho a ser usado para a sondagem de integridade.</span><span class="sxs-lookup"><span data-stu-id="f90a9-125">The path to use for the health probe.</span></span>
<span data-ttu-id="f90a9-126">Padrão é/</span><span class="sxs-lookup"><span data-stu-id="f90a9-126">Default is /</span></span>

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

### <span data-ttu-id="f90a9-127">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="f90a9-127">-Protocol</span></span>
<span data-ttu-id="f90a9-128">O esquema de protocolo a ser usado para esse valor padrão de investigação é HTTP</span><span class="sxs-lookup"><span data-stu-id="f90a9-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="f90a9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f90a9-129">CommonParameters</span></span>
<span data-ttu-id="f90a9-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f90a9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f90a9-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f90a9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f90a9-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f90a9-132">INPUTS</span></span>

### <span data-ttu-id="f90a9-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f90a9-133">None</span></span>
## <span data-ttu-id="f90a9-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f90a9-134">OUTPUTS</span></span>

### <span data-ttu-id="f90a9-135">Microsoft. Azure. Commands. FrontDoor. Models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="f90a9-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="f90a9-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f90a9-136">NOTES</span></span>

## <span data-ttu-id="f90a9-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f90a9-137">RELATED LINKS</span></span>

<span data-ttu-id="f90a9-138">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="f90a9-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
