---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: bd470a027285f66f15c831950639edaeb750c302
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943532"
---
# <span data-ttu-id="65204-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="65204-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="65204-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65204-102">SYNOPSIS</span></span>
<span data-ttu-id="65204-103">Configurar as configurações de notificação do Azure site Recovery (notificação por email) para o cofre.</span><span class="sxs-lookup"><span data-stu-id="65204-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="65204-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65204-104">SYNTAX</span></span>

### <span data-ttu-id="65204-105">Definir (padrão)</span><span class="sxs-lookup"><span data-stu-id="65204-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65204-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="65204-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65204-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="65204-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65204-108">Desabilita</span><span class="sxs-lookup"><span data-stu-id="65204-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65204-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65204-109">DESCRIPTION</span></span>
<span data-ttu-id="65204-110">O cmdlet **set-AzRecoveryServicesAsrNotificationSetting** configura as configurações de notificação do Azure site Recovery (notificação por email) para o cofre.</span><span class="sxs-lookup"><span data-stu-id="65204-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="65204-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65204-111">EXAMPLES</span></span>

### <span data-ttu-id="65204-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="65204-112">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="65204-113">Desative a notificação.</span><span class="sxs-lookup"><span data-stu-id="65204-113">Disable notification.</span></span>

### <span data-ttu-id="65204-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="65204-114">Example 2</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="65204-115">Defina a notificação para o (s) endereço (s) de email personalizado e para o proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="65204-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="65204-116">OS</span><span class="sxs-lookup"><span data-stu-id="65204-116">PARAMETERS</span></span>

### <span data-ttu-id="65204-117">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="65204-117">-CustomEmailAddress</span></span>
<span data-ttu-id="65204-118">Alerta/notificação enviada para emails.</span><span class="sxs-lookup"><span data-stu-id="65204-118">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="65204-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65204-119">-DefaultProfile</span></span>
<span data-ttu-id="65204-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65204-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65204-121">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="65204-121">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="65204-122">Parâmetro switch especifica habilitar notificação para o proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="65204-122">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="65204-123">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="65204-123">-DisableNotification</span></span>
<span data-ttu-id="65204-124">Sinalizar para desabilitar todas as notificações.</span><span class="sxs-lookup"><span data-stu-id="65204-124">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="65204-125">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="65204-125">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="65204-126">Parâmetro switch especifica habilitar notificação para o proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="65204-126">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="65204-127">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="65204-127">-LocaleID</span></span>
<span data-ttu-id="65204-128">Idioma de email do alerta/Notification para o usuário (códigos de cultura com suporte da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="65204-128">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="65204-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="65204-129">-Confirm</span></span>
<span data-ttu-id="65204-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65204-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65204-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65204-131">-WhatIf</span></span>
<span data-ttu-id="65204-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="65204-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65204-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65204-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65204-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65204-134">CommonParameters</span></span>
<span data-ttu-id="65204-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65204-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65204-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65204-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65204-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65204-137">INPUTS</span></span>

### <span data-ttu-id="65204-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="65204-138">None</span></span>

## <span data-ttu-id="65204-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65204-139">OUTPUTS</span></span>

### <span data-ttu-id="65204-140">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="65204-140">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="65204-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65204-141">NOTES</span></span>

## <span data-ttu-id="65204-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65204-142">RELATED LINKS</span></span>
