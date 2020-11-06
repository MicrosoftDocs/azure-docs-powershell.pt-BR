---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
ms.openlocfilehash: 08e68a878267f706c280c8d461e8c904141cd06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430843"
---
# <span data-ttu-id="db500-101">Get-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="db500-101">Get-AzureRmSignalR</span></span>

## <span data-ttu-id="db500-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db500-102">SYNOPSIS</span></span>
<span data-ttu-id="db500-103">Obter um serviço de sinalizador específico ou todos os serviços de sinal de acesso em um grupo de recursos ou uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="db500-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db500-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db500-104">SYNTAX</span></span>

### <span data-ttu-id="db500-105">ListSignalRServiceParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="db500-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db500-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="db500-106">ResourceGroupParameterSet</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db500-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db500-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db500-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db500-108">DESCRIPTION</span></span>
<span data-ttu-id="db500-109">Obter um serviço de sinalizador específico ou todos os serviços de sinal de acesso em um grupo de recursos ou uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="db500-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="db500-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db500-110">EXAMPLES</span></span>

### <span data-ttu-id="db500-111">Obter todos os serviços do Signalr na assinatura</span><span class="sxs-lookup"><span data-stu-id="db500-111">Get all SignalR services in the subscription</span></span>
```powershell
PS C:\> Get-AzureRmSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="db500-112">Obter todos os serviços de sinal de acesso em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="db500-112">Get all SignalR services in a resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="db500-113">Obter um serviço de sinal específico</span><span class="sxs-lookup"><span data-stu-id="db500-113">Get a specific SignalR service</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="db500-114">Obter um serviço de sinalizador específico do grupo de recursos padrão</span><span class="sxs-lookup"><span data-stu-id="db500-114">Get a specific SignalR service from the default resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="db500-115">O grupo de recursos padrão pode ser definido por `Set-AzureRmDefault -ResourceGroupName myResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="db500-115">The default resource group can be set by `Set-AzureRmDefault -ResourceGroupName myResourceGroup`.</span></span>

## <span data-ttu-id="db500-116">OS</span><span class="sxs-lookup"><span data-stu-id="db500-116">PARAMETERS</span></span>

### <span data-ttu-id="db500-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db500-117">-DefaultProfile</span></span>
<span data-ttu-id="db500-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db500-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db500-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="db500-119">-Name</span></span>
<span data-ttu-id="db500-120">Nome do serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="db500-120">SignalR service name.</span></span>

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

### <span data-ttu-id="db500-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db500-121">-ResourceGroupName</span></span>
<span data-ttu-id="db500-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="db500-122">Resource group name.</span></span>

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

### <span data-ttu-id="db500-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db500-123">-ResourceId</span></span>
<span data-ttu-id="db500-124">A ID de recurso do serviço Signalr.</span><span class="sxs-lookup"><span data-stu-id="db500-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="db500-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db500-125">CommonParameters</span></span>
<span data-ttu-id="db500-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db500-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db500-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db500-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db500-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db500-128">INPUTS</span></span>

### <span data-ttu-id="db500-129">System. String</span><span class="sxs-lookup"><span data-stu-id="db500-129">System.String</span></span>
<span data-ttu-id="db500-130">Parâmetros: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="db500-130">Parameters: ResourceId (ByValue)</span></span>

## <span data-ttu-id="db500-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db500-131">OUTPUTS</span></span>

### <span data-ttu-id="db500-132">Microsoft. Azure. Commands. Signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="db500-132">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="db500-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db500-133">NOTES</span></span>

## <span data-ttu-id="db500-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db500-134">RELATED LINKS</span></span>
