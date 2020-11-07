---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 9f5c09e87e8d02276352cd10c2a7aba937822af2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941020"
---
# <span data-ttu-id="f14c5-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="f14c5-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="f14c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f14c5-102">SYNOPSIS</span></span>
<span data-ttu-id="f14c5-103">Criar objeto de destino de saída do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="f14c5-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="f14c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f14c5-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f14c5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f14c5-105">DESCRIPTION</span></span>
<span data-ttu-id="f14c5-106">O cmdlet New-AzNetworkWatcherConnectionMonitorOutputObject cria o objeto de destino de saída do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="f14c5-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="f14c5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f14c5-107">EXAMPLES</span></span>

### <span data-ttu-id="f14c5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f14c5-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -ResourcWorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="f14c5-109">Digite: "espaço de trabalho" WorkspaceSettings: {"WorkspaceResourceId": "MyWSResourceId"}</span><span class="sxs-lookup"><span data-stu-id="f14c5-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="f14c5-110">OS</span><span class="sxs-lookup"><span data-stu-id="f14c5-110">PARAMETERS</span></span>

### <span data-ttu-id="f14c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f14c5-111">-DefaultProfile</span></span>
<span data-ttu-id="f14c5-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f14c5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f14c5-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="f14c5-113">-OutputType</span></span>
<span data-ttu-id="f14c5-114">Tipo de destino de saída do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="f14c5-114">Connection monitor output destination type.</span></span> <span data-ttu-id="f14c5-115">No momento, \" só \" há suporte para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f14c5-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="f14c5-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="f14c5-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="f14c5-117">ID do recurso espaço de trabalho de análise de log.</span><span class="sxs-lookup"><span data-stu-id="f14c5-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="f14c5-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f14c5-118">-Confirm</span></span>
<span data-ttu-id="f14c5-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f14c5-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f14c5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f14c5-120">-WhatIf</span></span>
<span data-ttu-id="f14c5-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f14c5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f14c5-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f14c5-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f14c5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f14c5-123">CommonParameters</span></span>
<span data-ttu-id="f14c5-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f14c5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f14c5-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f14c5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f14c5-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f14c5-126">INPUTS</span></span>

### <span data-ttu-id="f14c5-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f14c5-127">None</span></span>

## <span data-ttu-id="f14c5-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f14c5-128">OUTPUTS</span></span>

### <span data-ttu-id="f14c5-129">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="f14c5-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="f14c5-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f14c5-130">NOTES</span></span>

## <span data-ttu-id="f14c5-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f14c5-131">RELATED LINKS</span></span>
