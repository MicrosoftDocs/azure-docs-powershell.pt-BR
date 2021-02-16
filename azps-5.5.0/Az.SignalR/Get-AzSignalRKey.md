---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: e71795c04d421ad0c6772ddd23724b5d53d38e86
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113977"
---
# <span data-ttu-id="ccf25-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="ccf25-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="ccf25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ccf25-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf25-103">Obter as teclas de acesso de um serviço de Sinalização.</span><span class="sxs-lookup"><span data-stu-id="ccf25-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="ccf25-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccf25-104">SYNTAX</span></span>

### <span data-ttu-id="ccf25-105">ResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ccf25-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ccf25-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccf25-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccf25-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccf25-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccf25-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ccf25-108">DESCRIPTION</span></span>
<span data-ttu-id="ccf25-109">Obter as teclas de acesso de um serviço de Sinalização.</span><span class="sxs-lookup"><span data-stu-id="ccf25-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="ccf25-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ccf25-110">EXAMPLES</span></span>

### <span data-ttu-id="ccf25-111">Obter chaves de acesso de um serviço de Sinalização específico</span><span class="sxs-lookup"><span data-stu-id="ccf25-111">Get access keys of a specific SignalR service</span></span>
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

### <span data-ttu-id="ccf25-112">Obter teclas de acesso de um objeto de serviço de Sinalização no cano</span><span class="sxs-lookup"><span data-stu-id="ccf25-112">Get access keys from a SignalR service object in pipe</span></span>

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

## <span data-ttu-id="ccf25-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccf25-113">PARAMETERS</span></span>

### <span data-ttu-id="ccf25-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf25-114">-DefaultProfile</span></span>
<span data-ttu-id="ccf25-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ccf25-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccf25-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccf25-116">-InputObject</span></span>
<span data-ttu-id="ccf25-117">O objeto de recurso signalr.</span><span class="sxs-lookup"><span data-stu-id="ccf25-117">The SignalR resource object.</span></span>

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

### <span data-ttu-id="ccf25-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ccf25-118">-Name</span></span>
<span data-ttu-id="ccf25-119">Nome do serviço de Sinalização.</span><span class="sxs-lookup"><span data-stu-id="ccf25-119">SignalR service name.</span></span>

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

### <span data-ttu-id="ccf25-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccf25-120">-ResourceGroupName</span></span>
<span data-ttu-id="ccf25-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ccf25-121">Resource group name.</span></span>

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

### <span data-ttu-id="ccf25-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccf25-122">-ResourceId</span></span>
<span data-ttu-id="ccf25-123">A ID do recurso de serviço de Sinalização.</span><span class="sxs-lookup"><span data-stu-id="ccf25-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="ccf25-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf25-124">CommonParameters</span></span>
<span data-ttu-id="ccf25-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccf25-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf25-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ccf25-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf25-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="ccf25-127">INPUTS</span></span>

### <span data-ttu-id="ccf25-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ccf25-128">System.String</span></span>
### <span data-ttu-id="ccf25-129">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="ccf25-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="ccf25-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="ccf25-130">OUTPUTS</span></span>

### <span data-ttu-id="ccf25-131">Microsoft.Azure.Commands.Signalr.Models.PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="ccf25-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>
## <span data-ttu-id="ccf25-132">Notas</span><span class="sxs-lookup"><span data-stu-id="ccf25-132">NOTES</span></span>

## <span data-ttu-id="ccf25-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ccf25-133">RELATED LINKS</span></span>
