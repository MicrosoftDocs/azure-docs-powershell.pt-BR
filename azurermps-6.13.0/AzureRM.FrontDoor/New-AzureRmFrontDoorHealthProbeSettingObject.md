---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: dcaf61b9001093d25f351d03e8e50da4c4ca22ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430289"
---
# <span data-ttu-id="b5ae3-101">New-AzureRmFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="b5ae3-101">New-AzureRmFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="b5ae3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ae3-103">Criar um objeto PSHealthProbeSetting para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="b5ae3-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5ae3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5ae3-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5ae3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b5ae3-105">DESCRIPTION</span></span>
<span data-ttu-id="b5ae3-106">Criar um objeto PSHealthProbeSetting para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="b5ae3-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="b5ae3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b5ae3-107">EXAMPLES</span></span>

### <span data-ttu-id="b5ae3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b5ae3-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="b5ae3-109">Criar um objeto PSHealthProbeSetting para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="b5ae3-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="b5ae3-110">OS</span><span class="sxs-lookup"><span data-stu-id="b5ae3-110">PARAMETERS</span></span>

### <span data-ttu-id="b5ae3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ae3-111">-DefaultProfile</span></span>
<span data-ttu-id="b5ae3-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b5ae3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5ae3-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b5ae3-113">-IntervalInSeconds</span></span>
<span data-ttu-id="b5ae3-114">O número de segundos entre testes de integridade.</span><span class="sxs-lookup"><span data-stu-id="b5ae3-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="b5ae3-115">O valor padrão é 30</span><span class="sxs-lookup"><span data-stu-id="b5ae3-115">Default value is 30</span></span>

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

### <span data-ttu-id="b5ae3-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5ae3-116">-Name</span></span>
<span data-ttu-id="b5ae3-117">nome da configuração de investigação de integridade.</span><span class="sxs-lookup"><span data-stu-id="b5ae3-117">health probe setting name.</span></span>

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

### <span data-ttu-id="b5ae3-118">-Caminho</span><span class="sxs-lookup"><span data-stu-id="b5ae3-118">-Path</span></span>
<span data-ttu-id="b5ae3-119">O caminho a ser usado para a sondagem de integridade.</span><span class="sxs-lookup"><span data-stu-id="b5ae3-119">The path to use for the health probe.</span></span>
<span data-ttu-id="b5ae3-120">Padrão é/</span><span class="sxs-lookup"><span data-stu-id="b5ae3-120">Default is /</span></span>

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

### <span data-ttu-id="b5ae3-121">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="b5ae3-121">-Protocol</span></span>
<span data-ttu-id="b5ae3-122">O esquema de protocolo a ser usado para esse valor padrão de investigação é HTTP</span><span class="sxs-lookup"><span data-stu-id="b5ae3-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="b5ae3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ae3-123">CommonParameters</span></span>
<span data-ttu-id="b5ae3-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5ae3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ae3-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5ae3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ae3-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b5ae3-126">INPUTS</span></span>

### <span data-ttu-id="b5ae3-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b5ae3-127">None</span></span>

## <span data-ttu-id="b5ae3-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b5ae3-128">OUTPUTS</span></span>

### <span data-ttu-id="b5ae3-129">Microsoft. Azure. Commands. FrontDoor. Models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="b5ae3-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="b5ae3-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b5ae3-130">NOTES</span></span>

## <span data-ttu-id="b5ae3-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5ae3-131">RELATED LINKS</span></span>

<span data-ttu-id="b5ae3-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="b5ae3-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
