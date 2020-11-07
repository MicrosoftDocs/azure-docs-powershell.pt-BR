---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: d6e26eb293a2b87fccc0749b6d5c53d15d7d860f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773423"
---
# <span data-ttu-id="897af-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="897af-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="897af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="897af-102">SYNOPSIS</span></span>
<span data-ttu-id="897af-103">Atualizar detalhes da descoberta para um vCenter registrado.</span><span class="sxs-lookup"><span data-stu-id="897af-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="897af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="897af-104">SYNTAX</span></span>

### <span data-ttu-id="897af-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="897af-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="897af-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="897af-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="897af-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="897af-107">DESCRIPTION</span></span>
<span data-ttu-id="897af-108">O cmdlet **Update-AzRecoveryServicesAsrvCenter** é atualizado para obter detalhes de descoberta de um vCenter registrado.</span><span class="sxs-lookup"><span data-stu-id="897af-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="897af-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="897af-109">EXAMPLES</span></span>

### <span data-ttu-id="897af-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="897af-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="897af-111">Atualizar detalhes da descoberta para um vCenter registrado.</span><span class="sxs-lookup"><span data-stu-id="897af-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="897af-112">OS</span><span class="sxs-lookup"><span data-stu-id="897af-112">PARAMETERS</span></span>

### <span data-ttu-id="897af-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="897af-113">-Account</span></span>
<span data-ttu-id="897af-114">conta de credenciais de logon do vCenter.</span><span class="sxs-lookup"><span data-stu-id="897af-114">vCenter login credentials account.</span></span>

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

### <span data-ttu-id="897af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="897af-115">-DefaultProfile</span></span>
<span data-ttu-id="897af-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="897af-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="897af-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="897af-117">-InputObject</span></span>
<span data-ttu-id="897af-118">O objeto do servidor do vCenter para o qual atualizar os detalhes da descoberta.</span><span class="sxs-lookup"><span data-stu-id="897af-118">The vCenter server object to update discovery details for.</span></span>

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

### <span data-ttu-id="897af-119">-Porta</span><span class="sxs-lookup"><span data-stu-id="897af-119">-Port</span></span>
<span data-ttu-id="897af-120">A porta TCP no servidor vCenter a ser usada para descoberta.</span><span class="sxs-lookup"><span data-stu-id="897af-120">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="897af-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="897af-121">-ResourceId</span></span>
<span data-ttu-id="897af-122">Especifica o ResourceId do vCenter.</span><span class="sxs-lookup"><span data-stu-id="897af-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="897af-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="897af-123">-Confirm</span></span>
<span data-ttu-id="897af-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="897af-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="897af-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="897af-125">-WhatIf</span></span>
<span data-ttu-id="897af-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="897af-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="897af-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="897af-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="897af-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="897af-128">CommonParameters</span></span>
<span data-ttu-id="897af-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="897af-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="897af-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="897af-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="897af-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="897af-131">INPUTS</span></span>

### <span data-ttu-id="897af-132">System. String</span><span class="sxs-lookup"><span data-stu-id="897af-132">System.String</span></span>

### <span data-ttu-id="897af-133">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="897af-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="897af-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="897af-134">OUTPUTS</span></span>

### <span data-ttu-id="897af-135">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="897af-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="897af-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="897af-136">NOTES</span></span>

## <span data-ttu-id="897af-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="897af-137">RELATED LINKS</span></span>