---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: f739c5fa018a4d4f4ebf553c76dbacd35ee315c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117991"
---
# <span data-ttu-id="203a0-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="203a0-101">Get-AzSignalR</span></span>

## <span data-ttu-id="203a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="203a0-102">SYNOPSIS</span></span>
<span data-ttu-id="203a0-103">Obter um serviço de sinalizador específico ou todos os serviços de sinal de acesso em um grupo de recursos ou uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="203a0-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="203a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="203a0-104">SYNTAX</span></span>

### <span data-ttu-id="203a0-105">ListSignalRServiceParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="203a0-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="203a0-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="203a0-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="203a0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="203a0-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="203a0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="203a0-108">DESCRIPTION</span></span>
<span data-ttu-id="203a0-109">Obter um serviço de sinalizador específico ou todos os serviços de sinal de acesso em um grupo de recursos ou uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="203a0-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="203a0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="203a0-110">EXAMPLES</span></span>

### <span data-ttu-id="203a0-111">Obter todos os serviços do Signalr na assinatura</span><span class="sxs-lookup"><span data-stu-id="203a0-111">Get all SignalR services in the subscription</span></span>
```
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="203a0-112">Obter todos os serviços de sinal de acesso em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="203a0-112">Get all SignalR services in a resource group</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="203a0-113">Obter um serviço de sinal específico</span><span class="sxs-lookup"><span data-stu-id="203a0-113">Get a specific SignalR service</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="203a0-114">Obter um serviço de sinalizador específico do grupo de recursos padrão</span><span class="sxs-lookup"><span data-stu-id="203a0-114">Get a specific SignalR service from the default resource group</span></span>
```
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="203a0-115">O grupo de recursos padrão pode ser definido por \` set-AzDefault-ResourceGroupName MyResource Group \` .</span><span class="sxs-lookup"><span data-stu-id="203a0-115">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="203a0-116">OS</span><span class="sxs-lookup"><span data-stu-id="203a0-116">PARAMETERS</span></span>

### <span data-ttu-id="203a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="203a0-117">-DefaultProfile</span></span>
<span data-ttu-id="203a0-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="203a0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="203a0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="203a0-119">-Name</span></span>
<span data-ttu-id="203a0-120">Nome do serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="203a0-120">SignalR service name.</span></span>

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

### <span data-ttu-id="203a0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="203a0-121">-ResourceGroupName</span></span>
<span data-ttu-id="203a0-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="203a0-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListSignalRServiceParameterSet, ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="203a0-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="203a0-123">-ResourceId</span></span>
<span data-ttu-id="203a0-124">A ID de recurso do serviço Signalr.</span><span class="sxs-lookup"><span data-stu-id="203a0-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="203a0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="203a0-125">CommonParameters</span></span>
<span data-ttu-id="203a0-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="203a0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="203a0-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="203a0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="203a0-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="203a0-128">INPUTS</span></span>

### <span data-ttu-id="203a0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="203a0-129">System.String</span></span>
## <span data-ttu-id="203a0-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="203a0-130">OUTPUTS</span></span>

### <span data-ttu-id="203a0-131">Microsoft. Azure. Commands. Signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="203a0-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="203a0-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="203a0-132">NOTES</span></span>

## <span data-ttu-id="203a0-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="203a0-133">RELATED LINKS</span></span>
