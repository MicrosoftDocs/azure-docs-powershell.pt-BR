---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
ms.openlocfilehash: 3eaef21cc9652ee7e5e4c52a51bcc3ab8bd5b1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602714"
---
# <span data-ttu-id="467cd-101">Get-AzureRmSignalRKey</span><span class="sxs-lookup"><span data-stu-id="467cd-101">Get-AzureRmSignalRKey</span></span>

## <span data-ttu-id="467cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="467cd-102">SYNOPSIS</span></span>
<span data-ttu-id="467cd-103">Obter as teclas de acesso de um serviço de sinal de acesso.</span><span class="sxs-lookup"><span data-stu-id="467cd-103">Get the access keys of a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="467cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="467cd-104">SYNTAX</span></span>

### <span data-ttu-id="467cd-105">ResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="467cd-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="467cd-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="467cd-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="467cd-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="467cd-107">InputObjectParameterSet</span></span>
```
Get-AzureRmSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="467cd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="467cd-108">DESCRIPTION</span></span>
<span data-ttu-id="467cd-109">Obter as teclas de acesso de um serviço de sinal de acesso.</span><span class="sxs-lookup"><span data-stu-id="467cd-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="467cd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="467cd-110">EXAMPLES</span></span>

### <span data-ttu-id="467cd-111">Obter teclas de acesso de um serviço de sinal específico</span><span class="sxs-lookup"><span data-stu-id="467cd-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzureRmSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="467cd-112">Obter teclas de acesso de um objeto de serviço de sinal de sinal no pipe</span><span class="sxs-lookup"><span data-stu-id="467cd-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzureRmSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="467cd-113">OS</span><span class="sxs-lookup"><span data-stu-id="467cd-113">PARAMETERS</span></span>

### <span data-ttu-id="467cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="467cd-114">-DefaultProfile</span></span>
<span data-ttu-id="467cd-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="467cd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="467cd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="467cd-116">-InputObject</span></span>
<span data-ttu-id="467cd-117">O objeto de recurso Signalr.</span><span class="sxs-lookup"><span data-stu-id="467cd-117">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="467cd-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="467cd-118">-Name</span></span>
<span data-ttu-id="467cd-119">Nome do serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="467cd-119">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467cd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="467cd-120">-ResourceGroupName</span></span>
<span data-ttu-id="467cd-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="467cd-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467cd-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="467cd-122">-ResourceId</span></span>
<span data-ttu-id="467cd-123">A ID de recurso do serviço Signalr.</span><span class="sxs-lookup"><span data-stu-id="467cd-123">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="467cd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="467cd-124">CommonParameters</span></span>
<span data-ttu-id="467cd-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="467cd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="467cd-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="467cd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="467cd-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="467cd-127">INPUTS</span></span>

### <span data-ttu-id="467cd-128">System. String</span><span class="sxs-lookup"><span data-stu-id="467cd-128">System.String</span></span>
<span data-ttu-id="467cd-129">Parâmetros: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="467cd-129">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="467cd-130">Microsoft. Azure. Commands. Signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="467cd-130">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="467cd-131">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="467cd-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="467cd-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="467cd-132">OUTPUTS</span></span>

### <span data-ttu-id="467cd-133">Microsoft. Azure. Commands. Signalr. Models. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="467cd-133">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>

## <span data-ttu-id="467cd-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="467cd-134">NOTES</span></span>

## <span data-ttu-id="467cd-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="467cd-135">RELATED LINKS</span></span>
