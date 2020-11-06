---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: c27d4d88dd4c2fdf86db5ca39d608add2feb845f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426295"
---
# <span data-ttu-id="edb0d-101">New-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="edb0d-101">New-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="edb0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="edb0d-102">SYNOPSIS</span></span>
<span data-ttu-id="edb0d-103">Adiciona um servidor vCenter para descobrir itens protegidos.</span><span class="sxs-lookup"><span data-stu-id="edb0d-103">Adds a vCenter server to discover protectable items from.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edb0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="edb0d-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount>
 -Port <Int32> -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="edb0d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="edb0d-105">DESCRIPTION</span></span>
<span data-ttu-id="edb0d-106">O cmdlet **New-AzureRmRecoveryServicesAsrvCenter** adiciona um servidor vCenter para descobrir itens protegidos.</span><span class="sxs-lookup"><span data-stu-id="edb0d-106">The **New-AzureRmRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="edb0d-107">Esse cmdlet registra o servidor do vCenter para descoberta com o servidor de configuração.</span><span class="sxs-lookup"><span data-stu-id="edb0d-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="edb0d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="edb0d-108">EXAMPLES</span></span>

### <span data-ttu-id="edb0d-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="edb0d-109">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="edb0d-110">Adiciona um servidor vCenter para descobrir itens protegidos.</span><span class="sxs-lookup"><span data-stu-id="edb0d-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="edb0d-111">OS</span><span class="sxs-lookup"><span data-stu-id="edb0d-111">PARAMETERS</span></span>

### <span data-ttu-id="edb0d-112">-Conta</span><span class="sxs-lookup"><span data-stu-id="edb0d-112">-Account</span></span>
<span data-ttu-id="edb0d-113">Conta de logon do usuário creadential.</span><span class="sxs-lookup"><span data-stu-id="edb0d-113">User login creadential Account.</span></span>

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

### <span data-ttu-id="edb0d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb0d-114">-DefaultProfile</span></span>
<span data-ttu-id="edb0d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="edb0d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edb0d-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="edb0d-116">-Fabric</span></span>
<span data-ttu-id="edb0d-117">Malha ASR correspondente ao servidor de configuração.</span><span class="sxs-lookup"><span data-stu-id="edb0d-117">ASR fabric corresponding to the Configuration server.</span></span>

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

### <span data-ttu-id="edb0d-118">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="edb0d-118">-IpOrHostName</span></span>
<span data-ttu-id="edb0d-119">Endereço IPv4 ou FQDN do servidor vCenter.</span><span class="sxs-lookup"><span data-stu-id="edb0d-119">IPv4 address or FQDN of the vCenter server.</span></span>

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

### <span data-ttu-id="edb0d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="edb0d-120">-Name</span></span>
<span data-ttu-id="edb0d-121">Um nome amigável para o servidor vCenter.</span><span class="sxs-lookup"><span data-stu-id="edb0d-121">A friendly name for the vCenter server.</span></span>

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

### <span data-ttu-id="edb0d-122">-Porta</span><span class="sxs-lookup"><span data-stu-id="edb0d-122">-Port</span></span>
<span data-ttu-id="edb0d-123">A porta TCP no servidor vCenter a ser usada para descoberta.</span><span class="sxs-lookup"><span data-stu-id="edb0d-123">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="edb0d-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="edb0d-124">-Confirm</span></span>
<span data-ttu-id="edb0d-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edb0d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edb0d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edb0d-126">-WhatIf</span></span>
<span data-ttu-id="edb0d-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="edb0d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edb0d-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="edb0d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edb0d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb0d-129">CommonParameters</span></span>
<span data-ttu-id="edb0d-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edb0d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb0d-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edb0d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb0d-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="edb0d-132">INPUTS</span></span>

### <span data-ttu-id="edb0d-133">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="edb0d-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="edb0d-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="edb0d-134">OUTPUTS</span></span>

### <span data-ttu-id="edb0d-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="edb0d-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="edb0d-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="edb0d-136">NOTES</span></span>

## <span data-ttu-id="edb0d-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="edb0d-137">RELATED LINKS</span></span>
