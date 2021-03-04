---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 049e1667fec5aef4f12a9912a4b9669364095b0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891304"
---
# <span data-ttu-id="076a3-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="076a3-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="076a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="076a3-102">SYNOPSIS</span></span>
<span data-ttu-id="076a3-103">Configure as configurações de notificação de Recuperação de Site do Azure (notificação por email) para o cofre.</span><span class="sxs-lookup"><span data-stu-id="076a3-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="076a3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="076a3-104">SYNTAX</span></span>

### <span data-ttu-id="076a3-105">Set (Default)</span><span class="sxs-lookup"><span data-stu-id="076a3-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="076a3-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="076a3-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="076a3-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="076a3-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="076a3-108">Desabilitar</span><span class="sxs-lookup"><span data-stu-id="076a3-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="076a3-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="076a3-109">DESCRIPTION</span></span>
<span data-ttu-id="076a3-110">O cmdlet **Set-AzRecoveryServicesAsrNotificationSetting** configura as configurações de notificação de Recuperação de Site do Azure (notificação de email) para o cofre.</span><span class="sxs-lookup"><span data-stu-id="076a3-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="076a3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="076a3-111">EXAMPLES</span></span>

### <span data-ttu-id="076a3-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="076a3-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="076a3-113">Desabilitar a notificação.</span><span class="sxs-lookup"><span data-stu-id="076a3-113">Disable notification.</span></span>

### <span data-ttu-id="076a3-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="076a3-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="076a3-115">De definir a notificação para endereços de email personalizados e para o proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="076a3-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="076a3-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="076a3-116">Example 3</span></span>

<span data-ttu-id="076a3-117">Configure as configurações de notificação de Recuperação de Site do Azure (notificação por email) para o cofre.</span><span class="sxs-lookup"><span data-stu-id="076a3-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="076a3-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="076a3-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="076a3-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="076a3-119">PARAMETERS</span></span>

### <span data-ttu-id="076a3-120">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="076a3-120">-CustomEmailAddress</span></span>
<span data-ttu-id="076a3-121">Alerta/Notificação enviada para emails.</span><span class="sxs-lookup"><span data-stu-id="076a3-121">Alert / Notification sent to emails.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="076a3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="076a3-122">-DefaultProfile</span></span>
<span data-ttu-id="076a3-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="076a3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="076a3-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="076a3-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="076a3-125">O parâmetro Switch especifica habilitar a notificação para o proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="076a3-125">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEmailToSubcriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="076a3-126">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="076a3-126">-DisableNotification</span></span>
<span data-ttu-id="076a3-127">Sinalizador para desabilitar toda a notificação.</span><span class="sxs-lookup"><span data-stu-id="076a3-127">Flag to disable all notification.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="076a3-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="076a3-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="076a3-129">O parâmetro Switch especifica habilitar a notificação para o proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="076a3-129">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmailToSubscriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="076a3-130">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="076a3-130">-LocaleID</span></span>
<span data-ttu-id="076a3-131">Idioma de email de alerta/notificação para o usuário(códigos de cultura com suporte da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="076a3-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

```yaml
Type: System.String
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="076a3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="076a3-132">-Confirm</span></span>
<span data-ttu-id="076a3-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="076a3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="076a3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="076a3-134">-WhatIf</span></span>
<span data-ttu-id="076a3-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="076a3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="076a3-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="076a3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="076a3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="076a3-137">CommonParameters</span></span>
<span data-ttu-id="076a3-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="076a3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="076a3-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="076a3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="076a3-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="076a3-140">INPUTS</span></span>

### <span data-ttu-id="076a3-141">Nenhum</span><span class="sxs-lookup"><span data-stu-id="076a3-141">None</span></span>

## <span data-ttu-id="076a3-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="076a3-142">OUTPUTS</span></span>

### <span data-ttu-id="076a3-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="076a3-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="076a3-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="076a3-144">NOTES</span></span>

## <span data-ttu-id="076a3-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="076a3-145">RELATED LINKS</span></span>
