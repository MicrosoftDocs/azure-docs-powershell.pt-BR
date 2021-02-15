---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: ec1bba32027d3ec96aef61f3abec7d51cec5c35b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112825"
---
# <span data-ttu-id="fe651-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="fe651-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="fe651-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe651-102">SYNOPSIS</span></span>
<span data-ttu-id="fe651-103">Criar objeto de destino de saída do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fe651-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="fe651-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe651-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe651-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe651-105">DESCRIPTION</span></span>
<span data-ttu-id="fe651-106">O New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet cria o objeto de destino de saída do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fe651-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="fe651-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fe651-107">EXAMPLES</span></span>

### <span data-ttu-id="fe651-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fe651-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -WorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="fe651-109">Tipo : "espaço de trabalho" WorkspaceSettings: { "WorkspaceResourceId": "MyWSResourceId" }</span><span class="sxs-lookup"><span data-stu-id="fe651-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="fe651-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe651-110">PARAMETERS</span></span>

### <span data-ttu-id="fe651-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe651-111">-DefaultProfile</span></span>
<span data-ttu-id="fe651-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe651-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe651-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="fe651-113">-OutputType</span></span>
<span data-ttu-id="fe651-114">Tipo de destino de saída do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fe651-114">Connection monitor output destination type.</span></span> <span data-ttu-id="fe651-115">Atualmente, somente \" o Espaço de Trabalho tem \" suporte.</span><span class="sxs-lookup"><span data-stu-id="fe651-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="fe651-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="fe651-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="fe651-117">ID do recurso de espaço de trabalho de análise de log.</span><span class="sxs-lookup"><span data-stu-id="fe651-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="fe651-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fe651-118">-Confirm</span></span>
<span data-ttu-id="fe651-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe651-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe651-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe651-120">-WhatIf</span></span>
<span data-ttu-id="fe651-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fe651-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe651-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fe651-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe651-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe651-123">CommonParameters</span></span>
<span data-ttu-id="fe651-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe651-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe651-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe651-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe651-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="fe651-126">INPUTS</span></span>

### <span data-ttu-id="fe651-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fe651-127">None</span></span>

## <span data-ttu-id="fe651-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="fe651-128">OUTPUTS</span></span>

### <span data-ttu-id="fe651-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="fe651-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="fe651-130">Notas</span><span class="sxs-lookup"><span data-stu-id="fe651-130">NOTES</span></span>

## <span data-ttu-id="fe651-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe651-131">RELATED LINKS</span></span>
