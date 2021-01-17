---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: e71795c04d421ad0c6772ddd23724b5d53d38e86
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427987"
---
# <span data-ttu-id="5e717-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="5e717-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="5e717-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e717-102">SYNOPSIS</span></span>
<span data-ttu-id="5e717-103">Obter as teclas de acesso de um serviço de sinal de acesso.</span><span class="sxs-lookup"><span data-stu-id="5e717-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="5e717-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e717-104">SYNTAX</span></span>

### <span data-ttu-id="5e717-105">ResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5e717-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e717-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e717-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e717-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e717-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e717-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e717-108">DESCRIPTION</span></span>
<span data-ttu-id="5e717-109">Obter as teclas de acesso de um serviço de sinal de acesso.</span><span class="sxs-lookup"><span data-stu-id="5e717-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="5e717-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e717-110">EXAMPLES</span></span>

### <span data-ttu-id="5e717-111">Obter teclas de acesso de um serviço de sinal específico</span><span class="sxs-lookup"><span data-stu-id="5e717-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="5e717-112">Obter teclas de acesso de um objeto de serviço de sinal de sinal no pipe</span><span class="sxs-lookup"><span data-stu-id="5e717-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="5e717-113">OS</span><span class="sxs-lookup"><span data-stu-id="5e717-113">PARAMETERS</span></span>

### <span data-ttu-id="5e717-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e717-114">-DefaultProfile</span></span>
<span data-ttu-id="5e717-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e717-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e717-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e717-116">-InputObject</span></span>
<span data-ttu-id="5e717-117">O objeto de recurso Signalr.</span><span class="sxs-lookup"><span data-stu-id="5e717-117">The SignalR resource object.</span></span>

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

### <span data-ttu-id="5e717-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e717-118">-Name</span></span>
<span data-ttu-id="5e717-119">Nome do serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="5e717-119">SignalR service name.</span></span>

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

### <span data-ttu-id="5e717-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e717-120">-ResourceGroupName</span></span>
<span data-ttu-id="5e717-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5e717-121">Resource group name.</span></span>

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

### <span data-ttu-id="5e717-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e717-122">-ResourceId</span></span>
<span data-ttu-id="5e717-123">A ID de recurso do serviço Signalr.</span><span class="sxs-lookup"><span data-stu-id="5e717-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="5e717-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e717-124">CommonParameters</span></span>
<span data-ttu-id="5e717-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e717-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e717-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e717-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e717-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e717-127">INPUTS</span></span>

### <span data-ttu-id="5e717-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5e717-128">System.String</span></span>
### <span data-ttu-id="5e717-129">Microsoft. Azure. Commands. Signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="5e717-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="5e717-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e717-130">OUTPUTS</span></span>

### <span data-ttu-id="5e717-131">Microsoft. Azure. Commands. Signalr. Models. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="5e717-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>
## <span data-ttu-id="5e717-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e717-132">NOTES</span></span>

## <span data-ttu-id="5e717-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e717-133">RELATED LINKS</span></span>
