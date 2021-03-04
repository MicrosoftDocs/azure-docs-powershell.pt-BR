---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: d19455e4b467846ce38541ca3b0ec02f586cf226
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887640"
---
# <span data-ttu-id="96a91-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="96a91-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="96a91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96a91-102">SYNOPSIS</span></span>
<span data-ttu-id="96a91-103">Atualize os detalhes da descoberta para um vCenter registrado.</span><span class="sxs-lookup"><span data-stu-id="96a91-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="96a91-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="96a91-104">SYNTAX</span></span>

### <span data-ttu-id="96a91-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="96a91-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96a91-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="96a91-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96a91-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="96a91-107">DESCRIPTION</span></span>
<span data-ttu-id="96a91-108">O cmdlet **Update-AzRecoveryServicesAsrvCenter** atualiza detalhes de descoberta para um vCenter registrado.</span><span class="sxs-lookup"><span data-stu-id="96a91-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="96a91-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96a91-109">EXAMPLES</span></span>

### <span data-ttu-id="96a91-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="96a91-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="96a91-111">Atualize os detalhes da descoberta para um vCenter registrado.</span><span class="sxs-lookup"><span data-stu-id="96a91-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="96a91-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="96a91-112">PARAMETERS</span></span>

### <span data-ttu-id="96a91-113">-Account</span><span class="sxs-lookup"><span data-stu-id="96a91-113">-Account</span></span>
<span data-ttu-id="96a91-114">Conta de credenciais de logon do vCenter.</span><span class="sxs-lookup"><span data-stu-id="96a91-114">vCenter login credentials account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96a91-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a91-115">-DefaultProfile</span></span>
<span data-ttu-id="96a91-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="96a91-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96a91-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96a91-117">-InputObject</span></span>
<span data-ttu-id="96a91-118">O objeto do servidor vCenter para atualizar os detalhes da descoberta.</span><span class="sxs-lookup"><span data-stu-id="96a91-118">The vCenter server object to update discovery details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96a91-119">-Port</span><span class="sxs-lookup"><span data-stu-id="96a91-119">-Port</span></span>
<span data-ttu-id="96a91-120">A porta TCP no servidor vCenter a ser usada para descoberta.</span><span class="sxs-lookup"><span data-stu-id="96a91-120">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96a91-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96a91-121">-ResourceId</span></span>
<span data-ttu-id="96a91-122">Especifica o resourceId do vCenter.</span><span class="sxs-lookup"><span data-stu-id="96a91-122">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96a91-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96a91-123">-Confirm</span></span>
<span data-ttu-id="96a91-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96a91-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96a91-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96a91-125">-WhatIf</span></span>
<span data-ttu-id="96a91-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="96a91-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96a91-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96a91-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96a91-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a91-128">CommonParameters</span></span>
<span data-ttu-id="96a91-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96a91-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a91-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96a91-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a91-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96a91-131">INPUTS</span></span>

### <span data-ttu-id="96a91-132">System.String</span><span class="sxs-lookup"><span data-stu-id="96a91-132">System.String</span></span>

### <span data-ttu-id="96a91-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="96a91-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="96a91-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="96a91-134">OUTPUTS</span></span>

### <span data-ttu-id="96a91-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="96a91-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="96a91-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="96a91-136">NOTES</span></span>

## <span data-ttu-id="96a91-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96a91-137">RELATED LINKS</span></span>
