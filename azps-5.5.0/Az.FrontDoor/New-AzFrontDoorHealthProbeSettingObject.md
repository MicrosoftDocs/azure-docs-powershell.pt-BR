---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 850db31354ebe4a717a5064c7fed56dc94bf1f0d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111883"
---
# <span data-ttu-id="4bbaa-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="4bbaa-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="4bbaa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4bbaa-102">SYNOPSIS</span></span>
<span data-ttu-id="4bbaa-103">Criar um objeto PSHealthProbeSetting para criação da Porta da Frente</span><span class="sxs-lookup"><span data-stu-id="4bbaa-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="4bbaa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4bbaa-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bbaa-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4bbaa-105">DESCRIPTION</span></span>
<span data-ttu-id="4bbaa-106">Criar um objeto PSHealthProbeSetting para criação da Porta da Frente</span><span class="sxs-lookup"><span data-stu-id="4bbaa-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="4bbaa-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4bbaa-107">EXAMPLES</span></span>

### <span data-ttu-id="4bbaa-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4bbaa-108">Example 1</span></span>
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

<span data-ttu-id="4bbaa-109">Observação: a configuração HealthProbeMethod não é sensível a minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="4bbaa-110">Criar um objeto PSHealthProbeSetting para criação da Porta da Frente</span><span class="sxs-lookup"><span data-stu-id="4bbaa-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="4bbaa-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4bbaa-111">PARAMETERS</span></span>

### <span data-ttu-id="4bbaa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bbaa-112">-DefaultProfile</span></span>
<span data-ttu-id="4bbaa-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bbaa-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="4bbaa-114">-EnabledState</span></span>
<span data-ttu-id="4bbaa-115">Se você quer habilitar testes de saúde em relação a back-ends definidos em backendPools.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="4bbaa-116">Problemas de saúde só poderão ser desabilitados se houver um único back-end habilitado em um único pool de back-end habilitado.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

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

### <span data-ttu-id="4bbaa-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="4bbaa-117">-HealthProbeMethod</span></span>
<span data-ttu-id="4bbaa-118">Configura qual método HTTP usar para desempencar os back-ends definidos em backendPools.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

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

### <span data-ttu-id="4bbaa-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="4bbaa-119">-IntervalInSeconds</span></span>
<span data-ttu-id="4bbaa-120">O número de segundos entre problemas de saúde.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="4bbaa-121">O valor padrão é 30</span><span class="sxs-lookup"><span data-stu-id="4bbaa-121">Default value is 30</span></span>

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

### <span data-ttu-id="4bbaa-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4bbaa-122">-Name</span></span>
<span data-ttu-id="4bbaa-123">Nome da configuração de problemas de saúde.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="4bbaa-124">-Caminho</span><span class="sxs-lookup"><span data-stu-id="4bbaa-124">-Path</span></span>
<span data-ttu-id="4bbaa-125">O caminho a ser usado para a saúde.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-125">The path to use for the health probe.</span></span>
<span data-ttu-id="4bbaa-126">O padrão é/</span><span class="sxs-lookup"><span data-stu-id="4bbaa-126">Default is /</span></span>

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

### <span data-ttu-id="4bbaa-127">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="4bbaa-127">-Protocol</span></span>
<span data-ttu-id="4bbaa-128">O esquema de protocolo a ser usado para esse valor padrão padrão é HTTP</span><span class="sxs-lookup"><span data-stu-id="4bbaa-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="4bbaa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bbaa-129">CommonParameters</span></span>
<span data-ttu-id="4bbaa-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bbaa-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bbaa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bbaa-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="4bbaa-132">INPUTS</span></span>

### <span data-ttu-id="4bbaa-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4bbaa-133">None</span></span>
## <span data-ttu-id="4bbaa-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="4bbaa-134">OUTPUTS</span></span>

### <span data-ttu-id="4bbaa-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="4bbaa-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="4bbaa-136">Notas</span><span class="sxs-lookup"><span data-stu-id="4bbaa-136">NOTES</span></span>

## <span data-ttu-id="4bbaa-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4bbaa-137">RELATED LINKS</span></span>

<span data-ttu-id="4bbaa-138">[Novo-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="4bbaa-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
