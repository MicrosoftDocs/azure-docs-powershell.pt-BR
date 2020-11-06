---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 298443c4b962a2be6c5cf3849657d0fe8bbaf978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427456"
---
# <span data-ttu-id="d3228-101">Update-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="d3228-101">Update-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="d3228-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3228-102">SYNOPSIS</span></span>
<span data-ttu-id="d3228-103">Atualizar detalhes da descoberta para um vCenter registrado.</span><span class="sxs-lookup"><span data-stu-id="d3228-103">Update discovery details for a registered vCenter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3228-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3228-104">SYNTAX</span></span>

### <span data-ttu-id="d3228-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="d3228-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3228-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d3228-106">ByResourceId</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3228-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3228-107">DESCRIPTION</span></span>
<span data-ttu-id="d3228-108">O cmdlet **Update-AzureRmRecoveryServicesAsrvCenter** é atualizado para obter detalhes de descoberta de um vCenter registrado.</span><span class="sxs-lookup"><span data-stu-id="d3228-108">The **Update-AzureRmRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="d3228-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3228-109">EXAMPLES</span></span>

### <span data-ttu-id="d3228-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d3228-110">Example 1</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="d3228-111">Atualizar detalhes da descoberta para um vCenter registrado.</span><span class="sxs-lookup"><span data-stu-id="d3228-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="d3228-112">OS</span><span class="sxs-lookup"><span data-stu-id="d3228-112">PARAMETERS</span></span>

### <span data-ttu-id="d3228-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="d3228-113">-Account</span></span>
<span data-ttu-id="d3228-114">conta de credenciais de logon do vCenter.</span><span class="sxs-lookup"><span data-stu-id="d3228-114">vCenter login credentials account.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3228-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d3228-115">-Confirm</span></span>
<span data-ttu-id="d3228-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3228-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3228-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3228-117">-DefaultProfile</span></span>
<span data-ttu-id="d3228-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3228-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3228-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3228-119">-InputObject</span></span>
<span data-ttu-id="d3228-120">O objeto do servidor do vCenter para o qual atualizar os detalhes da descoberta.</span><span class="sxs-lookup"><span data-stu-id="d3228-120">The vCenter server object to update discovery details for.</span></span>

```yaml
Type: ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3228-121">-Porta</span><span class="sxs-lookup"><span data-stu-id="d3228-121">-Port</span></span>
<span data-ttu-id="d3228-122">A porta TCP no servidor vCenter a ser usada para descoberta.</span><span class="sxs-lookup"><span data-stu-id="d3228-122">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: Int32
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3228-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3228-123">-ResourceId</span></span>
<span data-ttu-id="d3228-124">Especifica o ResourceId do vCenter.</span><span class="sxs-lookup"><span data-stu-id="d3228-124">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3228-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3228-125">-WhatIf</span></span>
<span data-ttu-id="d3228-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d3228-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3228-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d3228-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3228-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3228-128">CommonParameters</span></span>
<span data-ttu-id="d3228-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3228-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3228-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3228-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3228-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3228-131">INPUTS</span></span>

### <span data-ttu-id="d3228-132">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="d3228-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="d3228-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3228-133">OUTPUTS</span></span>

### <span data-ttu-id="d3228-134">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d3228-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d3228-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3228-135">NOTES</span></span>

## <span data-ttu-id="d3228-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3228-136">RELATED LINKS</span></span>