---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 696c5812a4b8eece62261208c501727aa48c2262
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942685"
---
# <span data-ttu-id="f2e74-101">New-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="f2e74-101">New-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="f2e74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2e74-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e74-103">Adiciona um servidor vCenter para descobrir itens protegidos.</span><span class="sxs-lookup"><span data-stu-id="f2e74-103">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="f2e74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2e74-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount> -Port <Int32>
 -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2e74-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2e74-105">DESCRIPTION</span></span>
<span data-ttu-id="f2e74-106">O cmdlet **New-AzRecoveryServicesAsrvCenter** adiciona um servidor vCenter para descobrir itens protegidos.</span><span class="sxs-lookup"><span data-stu-id="f2e74-106">The **New-AzRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="f2e74-107">Esse cmdlet registra o servidor do vCenter para descoberta com o servidor de configuração.</span><span class="sxs-lookup"><span data-stu-id="f2e74-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="f2e74-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2e74-108">EXAMPLES</span></span>

### <span data-ttu-id="f2e74-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f2e74-109">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="f2e74-110">Adiciona um servidor vCenter para descobrir itens protegidos.</span><span class="sxs-lookup"><span data-stu-id="f2e74-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="f2e74-111">OS</span><span class="sxs-lookup"><span data-stu-id="f2e74-111">PARAMETERS</span></span>

### <span data-ttu-id="f2e74-112">-Conta</span><span class="sxs-lookup"><span data-stu-id="f2e74-112">-Account</span></span>
<span data-ttu-id="f2e74-113">Conta de credenciais de logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="f2e74-113">User login credential Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e74-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2e74-114">-DefaultProfile</span></span>
<span data-ttu-id="f2e74-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2e74-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2e74-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="f2e74-116">-Fabric</span></span>
<span data-ttu-id="f2e74-117">Malha ASR correspondente ao servidor de configuração.</span><span class="sxs-lookup"><span data-stu-id="f2e74-117">ASR fabric corresponding to the Configuration server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2e74-118">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="f2e74-118">-IpOrHostName</span></span>
<span data-ttu-id="f2e74-119">Endereço IPv4 ou FQDN do servidor vCenter.</span><span class="sxs-lookup"><span data-stu-id="f2e74-119">IPv4 address or FQDN of the vCenter server.</span></span>

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

### <span data-ttu-id="f2e74-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2e74-120">-Name</span></span>
<span data-ttu-id="f2e74-121">Um nome amigável para o servidor vCenter.</span><span class="sxs-lookup"><span data-stu-id="f2e74-121">A friendly name for the vCenter server.</span></span>

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

### <span data-ttu-id="f2e74-122">-Porta</span><span class="sxs-lookup"><span data-stu-id="f2e74-122">-Port</span></span>
<span data-ttu-id="f2e74-123">A porta TCP no servidor vCenter a ser usada para descoberta.</span><span class="sxs-lookup"><span data-stu-id="f2e74-123">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e74-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f2e74-124">-Confirm</span></span>
<span data-ttu-id="f2e74-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2e74-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2e74-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2e74-126">-WhatIf</span></span>
<span data-ttu-id="f2e74-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2e74-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2e74-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2e74-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2e74-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e74-129">CommonParameters</span></span>
<span data-ttu-id="f2e74-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2e74-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e74-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2e74-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e74-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2e74-132">INPUTS</span></span>

### <span data-ttu-id="f2e74-133">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="f2e74-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="f2e74-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2e74-134">OUTPUTS</span></span>

### <span data-ttu-id="f2e74-135">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f2e74-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f2e74-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2e74-136">NOTES</span></span>

## <span data-ttu-id="f2e74-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2e74-137">RELATED LINKS</span></span>
