---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 60eaa3b5482d6d1c13236560f797383d68d97b44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596423"
---
# <span data-ttu-id="3a1e2-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="3a1e2-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="3a1e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a1e2-102">SYNOPSIS</span></span>
<span data-ttu-id="3a1e2-103">Criar um objeto PSHealthProbeSetting para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="3a1e2-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="3a1e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a1e2-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a1e2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a1e2-105">DESCRIPTION</span></span>
<span data-ttu-id="3a1e2-106">Criar um objeto PSHealthProbeSetting para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="3a1e2-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="3a1e2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a1e2-107">EXAMPLES</span></span>

### <span data-ttu-id="3a1e2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3a1e2-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="3a1e2-109">Criar um objeto PSHealthProbeSetting para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="3a1e2-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="3a1e2-110">OS</span><span class="sxs-lookup"><span data-stu-id="3a1e2-110">PARAMETERS</span></span>

### <span data-ttu-id="3a1e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a1e2-111">-DefaultProfile</span></span>
<span data-ttu-id="3a1e2-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a1e2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a1e2-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="3a1e2-113">-IntervalInSeconds</span></span>
<span data-ttu-id="3a1e2-114">O número de segundos entre testes de integridade.</span><span class="sxs-lookup"><span data-stu-id="3a1e2-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="3a1e2-115">O valor padrão é 30</span><span class="sxs-lookup"><span data-stu-id="3a1e2-115">Default value is 30</span></span>

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

### <span data-ttu-id="3a1e2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a1e2-116">-Name</span></span>
<span data-ttu-id="3a1e2-117">nome da configuração de investigação de integridade.</span><span class="sxs-lookup"><span data-stu-id="3a1e2-117">health probe setting name.</span></span>

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

### <span data-ttu-id="3a1e2-118">-Caminho</span><span class="sxs-lookup"><span data-stu-id="3a1e2-118">-Path</span></span>
<span data-ttu-id="3a1e2-119">O caminho a ser usado para a sondagem de integridade.</span><span class="sxs-lookup"><span data-stu-id="3a1e2-119">The path to use for the health probe.</span></span>
<span data-ttu-id="3a1e2-120">Padrão é/</span><span class="sxs-lookup"><span data-stu-id="3a1e2-120">Default is /</span></span>

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

### <span data-ttu-id="3a1e2-121">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="3a1e2-121">-Protocol</span></span>
<span data-ttu-id="3a1e2-122">O esquema de protocolo a ser usado para esse valor padrão de investigação é HTTP</span><span class="sxs-lookup"><span data-stu-id="3a1e2-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="3a1e2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a1e2-123">CommonParameters</span></span>
<span data-ttu-id="3a1e2-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a1e2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a1e2-125">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a1e2-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a1e2-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a1e2-126">INPUTS</span></span>

### <span data-ttu-id="3a1e2-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3a1e2-127">None</span></span>

## <span data-ttu-id="3a1e2-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a1e2-128">OUTPUTS</span></span>

### <span data-ttu-id="3a1e2-129">Microsoft. Azure. Commands. FrontDoor. Models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="3a1e2-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="3a1e2-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a1e2-130">NOTES</span></span>

## <span data-ttu-id="3a1e2-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a1e2-131">RELATED LINKS</span></span>

<span data-ttu-id="3a1e2-132">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="3a1e2-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
