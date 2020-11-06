---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 4e51cd90e490442c36b5864e53b4bb7a36e41e80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429722"
---
# <span data-ttu-id="f947a-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="f947a-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="f947a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f947a-102">SYNOPSIS</span></span>
<span data-ttu-id="f947a-103">Configurar as configurações de notificação do Azure site Recovery (notificação por email) para o cofre.</span><span class="sxs-lookup"><span data-stu-id="f947a-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f947a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f947a-104">SYNTAX</span></span>

### <span data-ttu-id="f947a-105">Definir (padrão)</span><span class="sxs-lookup"><span data-stu-id="f947a-105">Set (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f947a-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="f947a-106">EmailToSubscriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f947a-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="f947a-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f947a-108">Desabilita</span><span class="sxs-lookup"><span data-stu-id="f947a-108">Disable</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f947a-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f947a-109">DESCRIPTION</span></span>
<span data-ttu-id="f947a-110">O cmdlet **set-AzureRmRecoveryServicesAsrNotificationSetting** configura as configurações de notificação do Azure site Recovery (notificação por email) para o cofre.</span><span class="sxs-lookup"><span data-stu-id="f947a-110">The **Set-AzureRmRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="f947a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f947a-111">EXAMPLES</span></span>

### <span data-ttu-id="f947a-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f947a-112">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="f947a-113">Desative a notificação.</span><span class="sxs-lookup"><span data-stu-id="f947a-113">Disable notification.</span></span>

### <span data-ttu-id="f947a-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f947a-114">Example 2</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="f947a-115">Defina a notificação para o (s) endereço (s) de email personalizado e para o proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="f947a-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="f947a-116">OS</span><span class="sxs-lookup"><span data-stu-id="f947a-116">PARAMETERS</span></span>

### <span data-ttu-id="f947a-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f947a-117">-Confirm</span></span>
<span data-ttu-id="f947a-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f947a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f947a-119">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f947a-119">-CustomEmailAddress</span></span>
<span data-ttu-id="f947a-120">Alerta/notificação enviada para emails.</span><span class="sxs-lookup"><span data-stu-id="f947a-120">Alert / Notification sent to emails.</span></span>

```yaml
Type: String[]
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f947a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f947a-121">-DefaultProfile</span></span>
<span data-ttu-id="f947a-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f947a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f947a-123">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="f947a-123">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="f947a-124">Parâmetro switch especifica habilitar notificação para o proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="f947a-124">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableEmailToSubcriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f947a-125">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="f947a-125">-DisableNotification</span></span>
<span data-ttu-id="f947a-126">Sinalizar para desabilitar todas as notificações.</span><span class="sxs-lookup"><span data-stu-id="f947a-126">Flag to disable all notification.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f947a-127">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="f947a-127">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="f947a-128">Switch parâmetro especifica habilitar a notificação para o proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="f947a-128">Switch paramter specifies enable notification to subscription owner.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EmailToSubscriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f947a-129">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="f947a-129">-LocaleID</span></span>
<span data-ttu-id="f947a-130">Idioma de email do alerta/notifcation para o usuário (códigos de cultura com suporte da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="f947a-130">Email language of alert /notifcation to user(supported culture codes from microsoft).</span></span> 

```yaml
Type: String
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f947a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f947a-131">-WhatIf</span></span>
<span data-ttu-id="f947a-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f947a-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f947a-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f947a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f947a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f947a-134">CommonParameters</span></span>
<span data-ttu-id="f947a-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f947a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f947a-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f947a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f947a-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f947a-137">INPUTS</span></span>

### <span data-ttu-id="f947a-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f947a-138">None</span></span>

## <span data-ttu-id="f947a-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f947a-139">OUTPUTS</span></span>

### <span data-ttu-id="f947a-140">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRAlertSetting, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f947a-140">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f947a-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f947a-141">NOTES</span></span>

## <span data-ttu-id="f947a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f947a-142">RELATED LINKS</span></span>
