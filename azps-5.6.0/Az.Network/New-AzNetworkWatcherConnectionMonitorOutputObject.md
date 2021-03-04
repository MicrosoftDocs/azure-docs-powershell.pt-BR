---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 895659481999ab5801538bec3b88765e1d48aeca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886198"
---
# <span data-ttu-id="11aa0-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="11aa0-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="11aa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="11aa0-103">Criar objeto de destino de saída do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="11aa0-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="11aa0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="11aa0-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11aa0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="11aa0-105">DESCRIPTION</span></span>
<span data-ttu-id="11aa0-106">O New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet cria o objeto de destino de saída do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="11aa0-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="11aa0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11aa0-107">EXAMPLES</span></span>

### <span data-ttu-id="11aa0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="11aa0-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -WorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="11aa0-109">Tipo : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span><span class="sxs-lookup"><span data-stu-id="11aa0-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="11aa0-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="11aa0-110">PARAMETERS</span></span>

### <span data-ttu-id="11aa0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11aa0-111">-DefaultProfile</span></span>
<span data-ttu-id="11aa0-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11aa0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11aa0-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="11aa0-113">-OutputType</span></span>
<span data-ttu-id="11aa0-114">Tipo de destino de saída do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="11aa0-114">Connection monitor output destination type.</span></span> <span data-ttu-id="11aa0-115">Atualmente, apenas \" o Workspace \" é suportado.</span><span class="sxs-lookup"><span data-stu-id="11aa0-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="11aa0-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="11aa0-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="11aa0-117">ID do recurso do espaço de trabalho de análise de log.</span><span class="sxs-lookup"><span data-stu-id="11aa0-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="11aa0-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11aa0-118">-Confirm</span></span>
<span data-ttu-id="11aa0-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11aa0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11aa0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11aa0-120">-WhatIf</span></span>
<span data-ttu-id="11aa0-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="11aa0-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11aa0-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11aa0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11aa0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11aa0-123">CommonParameters</span></span>
<span data-ttu-id="11aa0-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11aa0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11aa0-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11aa0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11aa0-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11aa0-126">INPUTS</span></span>

### <span data-ttu-id="11aa0-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="11aa0-127">None</span></span>

## <span data-ttu-id="11aa0-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="11aa0-128">OUTPUTS</span></span>

### <span data-ttu-id="11aa0-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="11aa0-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="11aa0-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="11aa0-130">NOTES</span></span>

## <span data-ttu-id="11aa0-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11aa0-131">RELATED LINKS</span></span>
