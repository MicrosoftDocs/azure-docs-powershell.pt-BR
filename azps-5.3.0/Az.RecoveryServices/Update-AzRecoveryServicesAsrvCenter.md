---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 9e4ee275bf003dfa011eba4f00aad0029b5152de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427442"
---
# <span data-ttu-id="23d54-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="23d54-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="23d54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23d54-102">SYNOPSIS</span></span>
<span data-ttu-id="23d54-103">Atualizar detalhes da descoberta para um vCenter registrado.</span><span class="sxs-lookup"><span data-stu-id="23d54-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="23d54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23d54-104">SYNTAX</span></span>

### <span data-ttu-id="23d54-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="23d54-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23d54-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="23d54-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23d54-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23d54-107">DESCRIPTION</span></span>
<span data-ttu-id="23d54-108">O cmdlet **Update-AzRecoveryServicesAsrvCenter** é atualizado para obter detalhes de descoberta de um vCenter registrado.</span><span class="sxs-lookup"><span data-stu-id="23d54-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="23d54-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23d54-109">EXAMPLES</span></span>

### <span data-ttu-id="23d54-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="23d54-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="23d54-111">Atualizar detalhes da descoberta para um vCenter registrado.</span><span class="sxs-lookup"><span data-stu-id="23d54-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="23d54-112">OS</span><span class="sxs-lookup"><span data-stu-id="23d54-112">PARAMETERS</span></span>

### <span data-ttu-id="23d54-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="23d54-113">-Account</span></span>
<span data-ttu-id="23d54-114">conta de credenciais de logon do vCenter.</span><span class="sxs-lookup"><span data-stu-id="23d54-114">vCenter login credentials account.</span></span>

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

### <span data-ttu-id="23d54-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d54-115">-DefaultProfile</span></span>
<span data-ttu-id="23d54-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23d54-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23d54-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23d54-117">-InputObject</span></span>
<span data-ttu-id="23d54-118">O objeto do servidor do vCenter para o qual atualizar os detalhes da descoberta.</span><span class="sxs-lookup"><span data-stu-id="23d54-118">The vCenter server object to update discovery details for.</span></span>

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

### <span data-ttu-id="23d54-119">-Porta</span><span class="sxs-lookup"><span data-stu-id="23d54-119">-Port</span></span>
<span data-ttu-id="23d54-120">A porta TCP no servidor vCenter a ser usada para descoberta.</span><span class="sxs-lookup"><span data-stu-id="23d54-120">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="23d54-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23d54-121">-ResourceId</span></span>
<span data-ttu-id="23d54-122">Especifica o ResourceId do vCenter.</span><span class="sxs-lookup"><span data-stu-id="23d54-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="23d54-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="23d54-123">-Confirm</span></span>
<span data-ttu-id="23d54-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23d54-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23d54-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23d54-125">-WhatIf</span></span>
<span data-ttu-id="23d54-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="23d54-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23d54-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23d54-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23d54-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d54-128">CommonParameters</span></span>
<span data-ttu-id="23d54-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23d54-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d54-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23d54-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d54-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23d54-131">INPUTS</span></span>

### <span data-ttu-id="23d54-132">System. String</span><span class="sxs-lookup"><span data-stu-id="23d54-132">System.String</span></span>

### <span data-ttu-id="23d54-133">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="23d54-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="23d54-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23d54-134">OUTPUTS</span></span>

### <span data-ttu-id="23d54-135">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="23d54-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="23d54-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23d54-136">NOTES</span></span>

## <span data-ttu-id="23d54-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23d54-137">RELATED LINKS</span></span>
